# Instrukcja migracji strony katnami.pl na staging

## Bezpieczeństwo (PILNE)
1. **Natychmiast zmień wszystkie hasła** (panel CyberFolks, WordPress admin, poczta e-mail).
2. Nie publikuj haseł publicznie.
3. Wykonaj pełny backup przed rozpoczęciem.

## Metoda 1: Najprostsza (przez panel hostingu CyberFolks)

### Krok 1: Backup produkcji
1. Zaloguj się do panelu CyberFolks (www.katnami.pl).
2. Przejdź do sekcji **Bazy danych** → **phpMyAdmin**.
3. Wybierz bazę danych WordPress → **Eksport** → **Szybki** → **Wykonaj** → pobierz plik `.sql`.
4. Przejdź do **Menedżer plików** → wybierz katalog ze stroną → **Spakuj do .zip** → pobierz.

### Krok 2: Utwórz subdomenę staging
1. W panelu CyberFolks: **Domeny** → **Subdomeny** → dodaj `staging.katnami.pl`.
2. Ustaw katalog np. `/public_html/staging/`.
3. Zainstaluj WordPress (jeśli jest instalator) lub rozpakuj pliki ręcznie.

### Krok 3: Import na staging
1. **Pliki**: wgraj spakowane pliki do `/public_html/staging/` przez **Menedżer plików** i rozpakuj.
2. **Baza danych**: utwórz nową bazę dla staging w panelu (np. `katnami_staging`).
3. W **phpMyAdmin** wybierz nową bazę → **Import** → wybierz pobrany plik `.sql` → **Wykonaj**.
4. Edytuj plik `wp-config.php` na staging — zmień:
   ```php
   define('DB_NAME', 'katnami_staging');
   define('DB_USER', 'user_staging');
   define('DB_PASSWORD', 'pass_staging');
   ```

### Krok 4: Zamiana URL w bazie staging
1. W **phpMyAdmin** (baza staging) → **SQL** → wklej i wykonaj:
   ```sql
   UPDATE wp_options SET option_value = REPLACE(option_value, 'https://katnami.pl', 'https://staging.katnami.pl');
   UPDATE wp_posts SET guid = REPLACE(guid, 'https://katnami.pl', 'https://staging.katnami.pl');
   UPDATE wp_posts SET post_content = REPLACE(post_content, 'https://katnami.pl', 'https://staging.katnami.pl');
   UPDATE wp_postmeta SET meta_value = REPLACE(meta_value, 'https://katnami.pl', 'https://staging.katnami.pl');
   ```

### Krok 5: Wyłącz indeksowanie staging
1. Zaloguj się do WordPress staging (https://staging.katnami.pl/wp-admin).
2. **Ustawienia** → **Czytanie** → zaznacz **Zniechęcaj wyszukiwarki do indeksowania tej witryny** → **Zapisz**.

### Krok 6: Zabezpiecz staging (opcjonalnie)
1. W panelu CyberFolks: **Katalogi chronione hasłem** → wybierz `/public_html/staging/` → ustaw login/hasło.

---

## Metoda 2: Wtyczka All-in-One WP Migration (najprostsza dla początkujących)

### Krok 1: Eksport z produkcji
1. Zaloguj się do WordPress produkcyjnego (https://katnami.pl/wp-admin).
2. Zainstaluj wtyczkę **All-in-One WP Migration** (Wtyczki → Dodaj nową → wyszukaj).
3. **All-in-One WP Migration** → **Export** → **Export to File** → pobierz plik `.wpress`.

### Krok 2: Import na staging
1. Zainstaluj WordPress na subdomenie `staging.katnami.pl` (przez instalator w panelu).
2. Zainstaluj wtyczkę **All-in-One WP Migration** na staging.
3. **All-in-One WP Migration** → **Import** → wybierz pobrany plik `.wpress` → **Przywróć**.
4. Jeśli plik jest za duży: wgraj przez FTP/SFTP do `wp-content/ai1wm-backups/` i przywróć z listy backupów.

### Krok 3: Zabezpieczenie
1. Po imporcie zaloguj się do staging WP → **Ustawienia** → **Czytanie** → zaznacz **Zniechęcaj wyszukiwarki** → **Zapisz**.
2. Zmień hasło admina staging.

---

## Metoda 3: SSH / WP-CLI (dla zaawansowanych)

Jeśli masz dostęp SSH do serwera:

```bash
# Na produkcji
ssh user@katnami.pl
cd /var/www/katnami
wp db export /tmp/katnami.sql
tar --exclude='wp-config.php' -czf /tmp/katnami-files.tar.gz .
exit

# Kopiowanie na staging
scp user@katnami.pl:/tmp/katnami.sql user@staging.katnami.pl:/tmp/
scp user@katnami.pl:/tmp/katnami-files.tar.gz user@staging.katnami.pl:/tmp/

# Na staging
ssh user@staging.katnami.pl
cd /var/www/staging
tar -xzf /tmp/katnami-files.tar.gz
wp db import /tmp/katnami.sql
wp search-replace 'https://katnami.pl' 'https://staging.katnami.pl' --skip-columns=guid
wp option update blog_public 0
rm /tmp/katnami.sql /tmp/katnami-files.tar.gz
exit
```

---

## Po zakończeniu migracji

1. Sprawdź czy staging działa: https://staging.katnami.pl
2. Zaloguj się do panelu WP staging i przetestuj.
3. **Usuń wszystkie backupy z serwera** (pliki `.sql`, `.zip`, `.wpress`).
4. **Zmień hasła** (panel, WP admin, poczta) i nie publikuj ich.
5. Przejdź do następnego kroku: wdrożenie nowych treści (hero, usługi, portfolio).

---

## Checklist przed mergem na produkcję

- [ ] Staging działa poprawnie i jest zabezpieczony.
- [ ] Wszystkie nowe treści przetestowane (hero, podstrony usług, portfolio, pakiety).
- [ ] SEO: meta title/description, schema.org, alt teksty.
- [ ] Google Analytics 4 zainstalowane i konwersje skonfigurowane.
- [ ] Formularze działają (kontakt, rezerwacja).
- [ ] Responsywność mobile przetestowana.
- [ ] Backup produkcji zrobiony.
- [ ] Plan wdrożenia: DNS/redirect, czas przestoju minimalny.
- [ ] Po wdrożeniu: przetestować wszystkie linki i funkcje.

---

**Następny krok**: Po skonfigurowaniu staging wykonaj `git pull origin feature/staging-site` i wgraj nowe pliki/treści na staging.

