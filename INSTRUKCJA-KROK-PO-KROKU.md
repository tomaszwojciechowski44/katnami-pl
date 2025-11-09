# 🚀 Instrukcja KROK PO KROKU — Pierwsze 48 godzin

**Czas: 1-2 godziny łącznie (możesz rozłożyć na kilka dni)**

---

## ⚡ DZIEŃ 1: Backup produkcji (10-15 minut)

### Krok 1: Zaloguj się do panelu hostingu

1. Otwórz przeglądarkę (Chrome/Firefox/Edge)
2. Wpisz adres: **www.katnami.pl** (lub adres panelu CyberFolks)
3. Zaloguj się używając:
   - **Login:** kata.hapon@gmail.com (lub nazwa użytkownika)
   - **Hasło:** TWOJE NOWE HASŁO (zmień stare natychmiast!)
4. Kliknij **Zaloguj**

---

### Krok 2: Backup bazy danych (5 minut)

1. W panelu znajdź sekcję **"Bazy danych"** lub **"MySQL"**
2. Kliknij **phpMyAdmin** (ikona lub link)
3. W lewej kolumnie zobaczysz listę baz danych
4. Kliknij na bazę WordPress (nazwa prawdopodobnie: `katnami_db`, `katnami_wordpress`, lub podobna)
5. U góry zobaczysz zakładki: Przeglądaj, Struktura, SQL, **Eksport**...
6. Kliknij zakładkę **Eksport**
7. Wybierz opcję:
   - **Metoda eksportu:** Szybki (Quick)
   - **Format:** SQL
8. Kliknij przycisk **Wykonaj** (Go/Execute)
9. Przeglądarka pobierze plik `.sql` (np. `katnami_db.sql`)
10. **Zapisz plik jako:** `katnami-backup-2025-01-09.sql` w folderze `C:\Users\tomiz\Desktop\backup-katnami\`

✅ **Checkpoint:** Masz plik `.sql` zapisany lokalnie

---

### Krok 3: Backup plików WordPress (5-10 minut)

1. Wróć do głównego panelu hostingu
2. Znajdź sekcję **"Menedżer plików"** lub **"File Manager"**
3. Kliknij **Menedżer plików**
4. Zobaczysz strukturę katalogów. Znajdź katalog ze stroną WordPress:
   - Prawdopodobnie: `/public_html/` lub `/www/` lub `/domains/katnami.pl/public_html/`
5. Kliknij **prawym przyciskiem myszy** na katalog (lub zaznacz i użyj przycisku u góry)
6. Wybierz **"Kompresuj"** lub **"Compress"** lub **"Spakuj"**
7. Wybierz format: **ZIP**
8. Kliknij **OK** / **Kompresuj**
9. Poczekaj (może zająć 2-5 minut — strona WordPress jest duża!)
10. Po spakowaniu zobaczysz plik `.zip` w tym samym katalogu
11. Kliknij **prawym przyciskiem** na plik `.zip` → **Pobierz** (Download)
12. **Zapisz jako:** `katnami-files-2025-01-09.zip` w folderze `C:\Users\tomiz\Desktop\backup-katnami\`

✅ **Checkpoint:** Masz plik `.zip` zapisany lokalnie

---

### Krok 4: Zapisz backupy w chmurze (5 minut)

1. Otwórz **Google Drive** (lub Dropbox/OneDrive)
2. Utwórz folder: **"Backup katnami.pl 2025"**
3. Wgraj oba pliki:
   - `katnami-backup-2025-01-09.sql`
   - `katnami-files-2025-01-09.zip`
4. Sprawdź, czy pliki są wgrane (odśwież stronę)

✅ **DZIEŃ 1 UKOŃCZONY!** Masz bezpieczny backup produkcji. 🎉

---

## 🏗️ DZIEŃ 2: Staging — Metoda najprostsza (30-60 minut)

### Krok 1: Zainstaluj wtyczkę na produkcji (5 minut)

1. Otwórz WordPress admin produkcyjny:
   - Adres: **https://katnami.pl/wp-admin**
   - Login: Twój login WP
   - Hasło: TWOJE NOWE HASŁO
2. W lewym menu kliknij **Wtyczki** → **Dodaj nową**
3. W polu wyszukiwania wpisz: **All-in-One WP Migration**
4. Znajdź wtyczkę (autor: ServMask)
5. Kliknij **Instaluj teraz**
6. Po instalacji kliknij **Aktywuj**

✅ **Checkpoint:** Wtyczka jest aktywna (zobaczysz ją w menu po lewej stronie)

---

### Krok 2: Eksportuj stronę (10-15 minut)

1. W lewym menu kliknij **All-in-One WP Migration** → **Export**
2. Kliknij zielony przycisk **EXPORT TO** → wybierz **File**
3. Poczekaj (może zająć 5-15 minut w zależności od wielkości strony)
4. Zobaczysz progress bar (pasek postępu)
5. Gdy eksport się skończy, zobaczysz komunikat i zielony przycisk **DOWNLOAD [nazwa-strony].wpress**
6. Kliknij **DOWNLOAD**
7. Przeglądarka pobierze plik `.wpress` (może być duży, np. 100-500 MB)
8. **Zapisz jako:** `katnami-export-2025-01-09.wpress` w folderze `C:\Users\tomiz\Desktop\backup-katnami\`

✅ **Checkpoint:** Masz plik `.wpress` zapisany lokalnie

---

### Krok 3: Utwórz subdomenę staging (10 minut)

1. Wróć do panelu hostingu CyberFolks
2. Znajdź sekcję **"Domeny"** → **"Subdomeny"**
3. Kliknij **Dodaj subdomenę** lub **Utwórz subdomenę**
4. Wypełnij formularz:
   - **Subdomena:** `staging`
   - **Domena główna:** `katnami.pl` (wybierz z listy)
   - **Katalog docelowy:** `/staging/` lub `/public_html/staging/` (zostaw domyślny lub zmień)
5. Kliknij **Utwórz** / **Dodaj**

✅ **Checkpoint:** Subdomena `staging.katnami.pl` jest utworzona

---

### Krok 4: Zainstaluj WordPress na staging (10-15 minut)

**Opcja A: Instalator 1-click (jeśli dostępny w panelu)**

1. W panelu hostingu znajdź sekcję **"Instalator aplikacji"** lub **"Softaculous"** lub **"WordPress Installer"**
2. Kliknij **WordPress**
3. Wypełnij formularz:
   - **Wybierz domenę:** `staging.katnami.pl`
   - **Katalog:** zostaw puste (jeśli chcesz zainstalować w katalogu głównym subdomeny)
   - **Tytuł witryny:** Katnami Staging
   - **Admin Username:** (wymyśl)
   - **Admin Password:** (silne hasło)
   - **Admin Email:** kata.hapon@gmail.com
4. Kliknij **Instaluj**
5. Poczekaj (2-5 minut)
6. Zapisz dane logowania (login + hasło)

**Opcja B: Ręcznie (jeśli brak instalatora)**

1. Pobierz WordPress z https://pl.wordpress.org/download/
2. Rozpakuj i wgraj pliki przez Menedżer plików do `/staging/`
3. Utwórz nową bazę danych w panelu (sekcja "Bazy danych")
4. Otwórz `https://staging.katnami.pl` w przeglądarce
5. Wypełnij formularz instalacji WordPress
6. Kliknij **Instaluj WordPress**

✅ **Checkpoint:** WordPress jest zainstalowany na `staging.katnami.pl` (możesz się zalogować)

---

### Krok 5: Zaimportuj stronę na staging (10-15 minut)

1. Zaloguj się do WordPress admin staging:
   - Adres: **https://staging.katnami.pl/wp-admin**
   - Login: admin staging
   - Hasło: hasło staging
2. W lewym menu kliknij **Wtyczki** → **Dodaj nową**
3. Wyszukaj: **All-in-One WP Migration**
4. Zainstaluj i aktywuj wtyczkę
5. W lewym menu kliknij **All-in-One WP Migration** → **Import**
6. Kliknij **IMPORT FROM** → wybierz **File**
7. Wybierz plik: `katnami-export-2025-01-09.wpress` (który pobrałaś w Kroku 2)
8. Kliknij **UPLOAD** / **Wgraj**
9. Poczekaj (może zająć 5-15 minut)
10. Zobaczysz progress bar
11. Gdy import się skończy, zobaczysz komunikat: **"Import complete. Please log in again."**
12. Zostaniesz wylogowana — to normalne!

✅ **Checkpoint:** Import zakończony

---

### Krok 6: Zaloguj się ponownie i wyłącz indeksowanie (5 minut)

1. Otwórz ponownie: **https://staging.katnami.pl/wp-admin**
2. Zaloguj się używając **STAREGO loginu/hasła z produkcji** (wtyczka skopiowała użytkowników)
3. W lewym menu kliknij **Ustawienia** → **Czytanie**
4. Przewiń w dół
5. Znajdź opcję: **"Widoczność dla wyszukiwarek"**
6. Zaznacz checkbox: **"Zniechęcaj wyszukiwarki do indeksowania tej witryny"**
7. Kliknij **Zapisz zmiany** (na dole strony)

✅ **Checkpoint:** Staging jest zabezpieczony (Google nie będzie indeksować)

---

### Krok 7: Sprawdź czy staging działa (2 minuty)

1. Otwórz nową kartę w przeglądarce
2. Wpisz: **https://staging.katnami.pl**
3. Strona powinna się załadować i wyglądać identycznie jak produkcja

✅ **DZIEŃ 2 UKOŃCZONY!** Masz działający staging! 🎉

---

## 🎨 DZIEŃ 3: Pierwsza zmiana — Hero section (15 minut)

### Krok 1: Znajdź stronę główną (3 minuty)

1. Zaloguj się do WordPress admin staging: **https://staging.katnami.pl/wp-admin**
2. W lewym menu kliknij **Strony** → **Wszystkie strony**
3. Znajdź stronę główną (Home) — prawdopodobnie:
   - Tytuł: "Home" lub "Strona główna"
   - Jeśli nie wiesz która: przejdź do **Ustawienia** → **Czytanie** → sprawdź "Twoja strona główna wyświetla" — tam zobaczysz wybraną stronę
4. Kliknij **Edytuj** na stronie głównej

✅ **Checkpoint:** Jesteś w edytorze strony głównej

---

### Krok 2: Zmień nagłówek główny (5 minut)

**Otwórz plik `TEXTS_CONTENT.md` w drugiej karcie przeglądarki (GitHub lub lokalnie)**

1. W edytorze znajdź **nagłówek główny** (duży tekst, najczęściej na górze strony)
2. Zaznacz stary tekst
3. **Skopiuj nowy tekst z `TEXTS_CONTENT.md` → sekcja "STRONA GŁÓWNA (Home)" → Hero Section → H1:**
   ```
   Fotografia ślubna z pasją | Reportaże, które opowiadają Waszą historię
   ```
4. Wklej nowy tekst w miejsce starego
5. Upewnij się, że formatowanie jest poprawne (H1 = Nagłówek 1)

✅ **Checkpoint:** Nagłówek zmieniony

---

### Krok 3: Zmień podnagłówek (3 minuty)

1. Znajdź podnagłówek (mniejszy tekst pod nagłówkiem głównym)
2. Zaznacz stary tekst
3. **Skopiuj nowy tekst z `TEXTS_CONTENT.md` → Podnagłówek:**
   ```
   Uwieczniam najważniejsze chwile — śluby, chrzty, komunie. Naturalne, pełne emocji zdjęcia reportażowe dla rodzin z [Twoje Miasto] i okolic.
   ```
4. Wklej nowy tekst
5. **WAŻNE:** Zmień `[Twoje Miasto]` na nazwę Twojego miasta (np. "Krakowa", "Warszawy", "Wrocławia")

✅ **Checkpoint:** Podnagłówek zmieniony

---

### Krok 4: Dodaj/zmień przyciski CTA (4 minuty)

1. Znajdź przyciski (jeśli są) lub dodaj nowe:
   - **Przycisk 1:** Tekst: **"Zobacz portfolio"** → Link: `/portfolio/`
   - **Przycisk 2:** Tekst: **"Sprawdź pakiety"** → Link: `/pakiety-cennik/`

**Jak dodać przycisk (Gutenberg/edytor bloków):**
- Kliknij `+` (dodaj blok)
- Wyszukaj "Przycisk" (Button)
- Wpisz tekst przycisku
- Kliknij na przycisk → w prawym panelu zmień "Link" na `/portfolio/` lub `/pakiety-cennik/`

**Jak dodać przycisk (Elementor/inny page builder):**
- Przeciągnij widget "Button"
- Edytuj tekst i link

✅ **Checkpoint:** Przyciski dodane/zmienione

---

### Krok 5: Zapisz i zobacz podgląd (2 minuty)

1. Kliknij **Aktualizuj** (przycisk w prawym górnym rogu)
2. Kliknij **Podgląd** → **Podgląd w nowej karcie**
3. Sprawdź, czy zmiany wyglądają dobrze
4. Sprawdź na telefonie (otwórz `https://staging.katnami.pl` na telefonie)

✅ **DZIEŃ 3 UKOŃCZONY!** Masz nowy hero section! 🎉

---

## 🎉 GRATULACJE!

Wykonałaś 3 najważniejsze kroki:
- ✅ Backup produkcji (bezpieczny)
- ✅ Staging (kopia do testów)
- ✅ Pierwsza zmiana (hero section)

---

## 📅 Co dalej? (Kolejne dni)

**Dzień 4-5:**
- Dodaj landing page `/fotografia-slubna/` (tekst w `TEXTS_CONTENT.md`)
- Dodaj 1 pełny reportaż do portfolio (30-50 zdjęć)

**Dzień 6-7:**
- Dodaj pakiety cenowe (tekst w `TEXTS_CONTENT.md`)
- Dodaj FAQ (tekst w `TEXTS_CONTENT.md`)

**Instagram (równolegle):**
- Zmień bio (tekst w `INSTAGRAM_STRATEGY.md`)
- Opublikuj 1 reel

---

## 💡 Wskazówki końcowe

- **Testuj zawsze na staging** — nigdy bezpośrednio na produkcji
- **Zapisuj często** — klikaj "Aktualizuj" co kilka minut
- **Miej backupy** — zawsze możesz przywrócić
- **Nie śpiesz się** — lepiej wolno i dobrze, niż szybko i źle
- **Użyj checklisty** — wydrukuj `CHECKLIST.md` i zaznaczaj postępy

---

## 📞 Jeśli coś pójdzie nie tak:

1. **Przywróć backup** (masz kopię z Dnia 1)
2. **Wróć do dokumentacji** (`MIGRATION_GUIDE.md`, `CONTENT_PLAN.md`)
3. **Sprawdź Google** — szukaj rozwiązania problemu
4. **Kontakt z supportem hostingu** — CyberFolks pomoże z technicznymi sprawami

---

**Powodzenia! Masz to! 🚀💪**

---

_Utworzone: 2025-01-09_  
_Wersja: 1.0_

