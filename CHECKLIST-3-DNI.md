# ✅ Checklista PIERWSZE 3 DNI (wydrukuj!)

Zaznaczaj ✅ gdy wykonane

---

## 📦 DZIEŃ 1: BACKUP (10-15 min)

### Backup bazy danych
- [ ] Zalogowałam się do panelu CyberFolks (www.katnami.pl)
- [ ] Otworzyłam phpMyAdmin
- [ ] Wybrałam bazę WordPress
- [ ] Kliknęłam **Eksport** → **Szybki** → **Wykonaj**
- [ ] Pobrałam plik `.sql`
- [ ] Zapisałam jako: `katnami-backup-2025-01-09.sql`

### Backup plików
- [ ] Otworzyłam Menedżer plików w panelu
- [ ] Znalazłam katalog WordPress (`/public_html/` lub `/www/`)
- [ ] Spakowałam katalog do `.zip`
- [ ] Pobrałam plik `.zip`
- [ ] Zapisałam jako: `katnami-files-2025-01-09.zip`

### Backup w chmurze
- [ ] Wgrałam oba pliki na Google Drive / Dropbox
- [ ] Sprawdziłam, że są wgrane

**✅ DZIEŃ 1 GOTOWY!**

---

## 🏗️ DZIEŃ 2: STAGING (30-60 min)

### Instalacja wtyczki na produkcji
- [ ] Zalogowałam się do WordPress admin: `https://katnami.pl/wp-admin`
- [ ] Przejdę do **Wtyczki** → **Dodaj nową**
- [ ] Wyszukałam: **All-in-One WP Migration**
- [ ] Zainstalowałam i aktywowałam

### Eksport strony
- [ ] Kliknęłam **All-in-One WP Migration** → **Export**
- [ ] Kliknęłam **EXPORT TO** → **File**
- [ ] Poczekałam (5-15 min)
- [ ] Pobrałam plik `.wpress`
- [ ] Zapisałam jako: `katnami-export-2025-01-09.wpress`

### Utworzenie subdomeny
- [ ] Wróciłam do panelu CyberFolks
- [ ] Przejdę do **Domeny** → **Subdomeny**
- [ ] Dodałam subdomenę: `staging.katnami.pl`
- [ ] Zapisałam

### Instalacja WordPress na staging
- [ ] Użyłam instalatora 1-click (jeśli dostępny) LUB wgrałam ręcznie
- [ ] WordPress zainstalowany na `staging.katnami.pl`
- [ ] Zapisałam login i hasło staging

### Import na staging
- [ ] Zalogowałam się do WordPress staging: `https://staging.katnami.pl/wp-admin`
- [ ] Zainstalowałam wtyczkę **All-in-One WP Migration**
- [ ] Kliknęłam **All-in-One WP Migration** → **Import**
- [ ] Wybrałam plik `.wpress`
- [ ] Poczekałam (5-15 min)
- [ ] Import zakończony (zostałam wylogowana)

### Wyłączenie indeksowania
- [ ] Zalogowałam się ponownie (stary login/hasło produkcji)
- [ ] Przejdę do **Ustawienia** → **Czytanie**
- [ ] Zaznaczyłam: **"Zniechęcaj wyszukiwarki do indeksowania"**
- [ ] Zapisałam zmiany

### Sprawdzenie
- [ ] Otworzyłam: `https://staging.katnami.pl`
- [ ] Strona działa! ✅

**✅ DZIEŃ 2 GOTOWY!**

---

## 🎨 DZIEŃ 3: PIERWSZA ZMIANA (15 min)

### Znalezienie strony głównej
- [ ] Zalogowałam się do WordPress staging
- [ ] Przejdę do **Strony** → **Wszystkie strony**
- [ ] Znalazłam stronę główną (Home)
- [ ] Kliknęłam **Edytuj**

### Zmiana nagłówka
- [ ] Otworzyłam plik `TEXTS_CONTENT.md` (GitHub lub lokalnie)
- [ ] Skopiowałam nowy nagłówek H1:
      ```
      Fotografia ślubna z pasją | Reportaże, które opowiadają Waszą historię
      ```
- [ ] Wkleiłam w miejsce starego nagłówka
- [ ] Sprawdziłam formatowanie (H1)

### Zmiana podnagłówka
- [ ] Skopiowałam podnagłówek z `TEXTS_CONTENT.md`:
      ```
      Uwieczniam najważniejsze chwile — śluby, chrzty, komunie. 
      Naturalne, pełne emocji zdjęcia reportażowe dla rodzin z [Twoje Miasto] i okolic.
      ```
- [ ] Wkleiłam w miejsce starego podnagłówka
- [ ] Zmieniłam `[Twoje Miasto]` na nazwę mojego miasta

### Przyciski CTA
- [ ] Dodałam/zmieniłam przycisk 1: **"Zobacz portfolio"** → link: `/portfolio/`
- [ ] Dodałam/zmieniłam przycisk 2: **"Sprawdź pakiety"** → link: `/pakiety-cennik/`

### Zapisanie i podgląd
- [ ] Kliknęłam **Aktualizuj**
- [ ] Kliknęłam **Podgląd** → sprawdziłam zmiany
- [ ] Sprawdziłam na telefonie

**✅ DZIEŃ 3 GOTOWY!**

---

## 🎉 GRATULACJE!

Wykonałaś 3 najważniejsze kroki:
- ✅ Backup produkcji
- ✅ Staging (kopia do testów)
- ✅ Pierwsza zmiana (hero section)

---

## 📅 CO DALEJ? (Dzień 4-7)

- [ ] Dodać landing page `/fotografia-slubna/`
- [ ] Dodać 1 pełny reportaż do portfolio
- [ ] Dodać pakiety cenowe
- [ ] Dodać FAQ
- [ ] Zmienić bio Instagram
- [ ] Opublikować 1 reel

**Szczegóły w plikach:**
- `TEXTS_CONTENT.md` — gotowe teksty
- `INSTAGRAM_STRATEGY.md` — strategia Instagram
- `CHECKLIST.md` — pełna checklista (wszystkie tygodnie)

---

**Masz to! Konsekwencja = rezultaty! 🚀💪**

---

_Data: 2025-01-09_  
_Czas łączny: ~1-2 godziny (3 dni)_

