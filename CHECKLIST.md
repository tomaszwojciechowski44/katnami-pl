# ✅ Checklista wdrożenia — Katnami.pl

Wydrukuj i zaznaczaj postępy! 🖨️

---

## 🔐 BEZPIECZEŃSTWO (PILNE — zrób TERAZ)

- [ ] Zmieniłam hasło do panelu hostingu CyberFolks
- [ ] Zmieniłam hasło do WordPress admin
- [ ] Zmieniłam hasło do poczty e-mail (kontakt@katnami.pl)
- [ ] Nie publikuję haseł publicznie

---

## 📦 TYDZIEŃ 1: BACKUP I STAGING

### Backup produkcji
- [ ] Zalogowałam się do panelu CyberFolks
- [ ] Wyeksportowałam bazę danych (phpMyAdmin → Eksport → `.sql`)
- [ ] Spakowałam pliki WordPress do `.zip`
- [ ] Zapisałam backupy lokalnie (dysk + chmura)

### Staging
- [ ] Utworzyłam subdomenę `staging.katnami.pl` w panelu
- [ ] Zainstalowałam WordPress na staging
- [ ] Skopiowałam stronę na staging (All-in-One WP Migration lub ręcznie)
- [ ] Wyłączyłam indeksowanie staging (Ustawienia → Czytanie → zaznacz "Zniechęcaj wyszukiwarki")
- [ ] Zabezpieczyłam staging hasłem (opcjonalnie: Katalogi chronione)
- [ ] Sprawdziłam, że staging działa: `https://staging.katnami.pl`

---

## 🎨 TYDZIEŃ 2: TREŚCI I STRUKTURA

### Strona główna (Home)
- [ ] Zaktualizowałam hero section (nagłówek H1: "Fotografia ślubna z pasją...")
- [ ] Dodałam 2 CTA (Zobacz portfolio / Sprawdź pakiety)
- [ ] Dodałam sekcję "Usługi" (4 kafelki: ślub, reportaż, chrzest, komunia)
- [ ] Zaktualizowałam sekcję "O mnie" (krótki opis)
- [ ] Dodałam sekcję "Opinie" (3 cytaty klientów)

### Landing pages usług
- [ ] Utworzyłam `/fotografia-slubna/` (tekst z TEXTS_CONTENT.md)
- [ ] Utworzyłam `/reportaz-slubny/` (tekst z TEXTS_CONTENT.md)
- [ ] Utworzyłam `/fotografia-chrzcin/` (tekst z TEXTS_CONTENT.md)
- [ ] Utworzyłam `/fotografia-komunii/` (tekst z TEXTS_CONTENT.md)
- [ ] Dodałam meta title i description do każdej podstrony

### Portfolio
- [ ] Dodałam pełny reportaż #1 (30–50 zdjęć) — ślub
- [ ] Dodałam pełny reportaż #2 (30–50 zdjęć) — chrzest lub komunia
- [ ] Dodałam pełny reportaż #3 (30–50 zdjęć) — sesja narzeczeńska lub ślub
- [ ] Zoptymalizowałam alt teksty zdjęć (np. "fotografia ślubna [miasto] para młoda")
- [ ] Ustawiłam lazy loading (wtyczka lub ustawienia motywu)

### Pakiety i cennik
- [ ] Utworzyłam stronę `/pakiety-cennik/`
- [ ] Dodałam 3 pakiety ślubne (Basic, Standard, Premium)
- [ ] Dodałam pakiety chrzest/komunia
- [ ] Dodałam sekcję "Dodatki" (drugi fotograf, album, sesja)
- [ ] Dodałam CTA "Zarezerwuj termin"

### FAQ
- [ ] Utworzyłam stronę `/faq/`
- [ ] Dodałam 8–10 pytań i odpowiedzi (tekst z TEXTS_CONTENT.md)

### O mnie
- [ ] Utworzyłam stronę `/o-mnie/`
- [ ] Dodałam zdjęcie portretowe
- [ ] Dodałam opis (moja historia, styl, wartości)
- [ ] Dodałam liczby (X par, Y reportaży, Z lat doświadczenia)

### Opinie
- [ ] Utworzyłam stronę `/opinie/`
- [ ] Dodałam 3–5 opinii klientów (imiona, cytaty, daty)
- [ ] Dodałam link do Google Reviews

### Kontakt
- [ ] Utworzyłam stronę `/kontakt/`
- [ ] Dodałam formularz kontaktowy (Contact Form 7 / Gravity Forms)
- [ ] Dodałam dane kontaktowe (e-mail, telefon, Instagram)
- [ ] Przetestowałam formularz (wysłałam testową wiadomość)

---

## 🔍 TYDZIEŃ 3: SEO I KONWERSJE

### SEO techniczne
- [ ] Zainstalowałam wtyczkę SEO (Rank Math / Yoast SEO)
- [ ] Dodałam schema.org JSON-LD do `<head>` (plik `schema-org.html`)
- [ ] Zoptymalizowałam meta title i description na wszystkich stronach
- [ ] Dodałam alt teksty do wszystkich zdjęć
- [ ] Utworzyłam sitemap.xml (wtyczka SEO zrobi to automatycznie)
- [ ] Sprawdziłam szybkość strony (PageSpeed Insights)
- [ ] Zainstalowałam cache (WP Rocket / W3 Total Cache)
- [ ] Skompresowałam obrazy (Smush / ShortPixel)

### Google Analytics 4
- [ ] Utworzyłam konto GA4 (https://analytics.google.com)
- [ ] Skopiowałam Measurement ID (G-XXXXXXXXXX)
- [ ] Wkleiłam snippet GA4 do `<head>` (plik `google-analytics-ga4.html`)
- [ ] Dodałam zdarzenia konwersji (form_submit, cta_click, contact_click)
- [ ] Oznaczyłam zdarzenia jako konwersje w GA4 (Admin → Events → Mark as conversion)
- [ ] Przetestowałam w GA4 Realtime

### Google Search Console
- [ ] Utworzyłam konto Google Search Console
- [ ] Zweryfikowałam domenę katnami.pl
- [ ] Wysłałam sitemap.xml
- [ ] Sprawdziłam indeksowanie (Coverage report)

---

## 🌟 TYDZIEŃ 4: GOOGLE BUSINESS I OPINIE

### Google Business Profile
- [ ] Utworzyłam/zaktualizowałam profil Google Business
- [ ] Dodałam nazwę: "Katnami Fotografia"
- [ ] Dodałam kategorie: Fotograf ślubny, Fotograf
- [ ] Dodałam adres (jeśli biuro/studio) lub obszar obsługi
- [ ] Dodałam telefon, e-mail, stronę www
- [ ] Dodałam godziny otwarcia
- [ ] Dodałam opis (150–200 znaków)
- [ ] Wgrałam zdjęcia (logo, portret, portfolio — min. 10 zdjęć)
- [ ] Opublikowałam pierwszy post

### Opinie klientów
- [ ] Wysłałam link do opinii Google 3 ostatnim klientom
- [ ] Zebrałam min. 3 opinie (5 gwiazdek)
- [ ] Odpowiedziałam na każdą opinię (podziękowania)
- [ ] Dodałam widget opinii Google na stronie (opcjonalnie)

---

## 📱 TYDZIEŃ 5: INSTAGRAM

### Profil
- [ ] Zmieniłam nazwę profilu na "Katnami Fotografia Ślubna"
- [ ] Zaktualizowałam bio (tekst z INSTAGRAM_STRATEGY.md)
- [ ] Dodałam link do pakietów (lub Linktree)
- [ ] Zmieniłam zdjęcie profilowe (logo lub portret z aparatem)

### Wyróżnienia (Highlights)
- [ ] Utworzyłam wyróżnienie "Wesela"
- [ ] Utworzyłam wyróżnienie "Reportaże"
- [ ] Utworzyłam wyróżnienie "Chrzty"
- [ ] Utworzyłam wyróżnienie "Komunie"
- [ ] Utworzyłam wyróżnienie "Opinie"
- [ ] Utworzyłam wyróżnienie "Pakiety"
- [ ] Utworzyłam wyróżnienie "Porady"

### Treści (pierwsze 2 tygodnie)
- [ ] Opublikowałam reel #1: Timeline reportażu (60s)
- [ ] Opublikowałam reel #2: Before & After (30s)
- [ ] Opublikowałam reel #3: Porady dla par młodych (60s)
- [ ] Opublikowałam post #1: Karuzela z reportażu ślubnego (8 zdjęć)
- [ ] Opublikowałam post #2: Karuzela z chrztu/komunii (6 zdjęć)
- [ ] Opublikowałam post #3: Opinia klienta (grafika + cytat)

### Stories (codziennie)
- [ ] Publikuję stories 3–5x/tydzień (BTS, sneak peek, ankiety)
- [ ] Oznaczam lokalizacje (miejsca, sale weselne)
- [ ] Oznaczam vendorów (plannerzy, suknie, kwiaty)

### Współpraca
- [ ] Nawiązałam współpracę z 1 wedding plannerem
- [ ] Nawiązałam współpracę z 1 salą weselną
- [ ] Nawiązałam współpracę z 1 salonem sukien
- [ ] Zaplanowałam styled shoot (opcjonalnie)

---

## 🧪 TYDZIEŃ 6: TESTOWANIE

### Responsywność
- [ ] Przetestowałam stronę na telefonie (iPhone/Android)
- [ ] Przetestowałam stronę na tablecie
- [ ] Przetestowałam stronę na różnych przeglądarkach (Chrome, Safari, Firefox)

### Funkcjonalność
- [ ] Przetestowałam formularz kontaktowy (wysłanie zapytania)
- [ ] Przetestowałam wszystkie linki (portfolio, pakiety, kontakt)
- [ ] Przetestowałam CTA (kliknięcia, przekierowania)
- [ ] Sprawdziłam, czy nie ma błędów 404

### Szybkość
- [ ] Sprawdziłam PageSpeed Insights (mobile + desktop)
- [ ] Wynik mobile >70 (dobry), >90 (bardzo dobry)
- [ ] Wynik desktop >80 (dobry), >90 (bardzo dobry)
- [ ] Poprawiłam obrazy (kompresja, WebP)
- [ ] Włączyłam cache

---

## 🚀 TYDZIEŃ 7: WDROŻENIE NA PRODUKCJĘ

### Backup (jeszcze raz!)
- [ ] Zrobiłam backup staging (pliki + baza)
- [ ] Zrobiłam backup produkcji (pliki + baza)

### Migracja
- [ ] Wyeksportowałam stronę ze staging (All-in-One WP Migration)
- [ ] Zaimportowałam na produkcję
- [ ] Sprawdziłam, że wszystko działa (strona główna, portfolio, formularze)
- [ ] Poprawiłam linki (jeśli potrzeba)

### Weryfikacja
- [ ] Sprawdziłam wszystkie strony na produkcji
- [ ] Przetestowałam formularz kontaktowy
- [ ] Sprawdziłam GA4 (czy śledzi eventy)
- [ ] Wysłałam sitemap do Google Search Console
- [ ] Monitoruję przez pierwsze 48h (błędy, ruch)

---

## 📈 TYDZIEŃ 8: REKLAMY I PROMOCJA

### Facebook/Instagram Ads
- [ ] Utworzyłam konto Meta Business Suite
- [ ] Przygotowałam 3 kreacje (karuzela/wideo/zdjęcie)
- [ ] Ustawiłam targeting (lokalizacja, wiek 23–35, zainteresowania: wesela)
- [ ] Uruchomiłam testową kampanię (budżet 20–30 PLN/dzień)
- [ ] Monitoruję wyniki (CTR, konwersje, koszt)

### Google Ads
- [ ] Utworzyłam konto Google Ads
- [ ] Przygotowałam kampanię Search (frazy: "fotograf ślubny [miasto]")
- [ ] Dodałam rozszerzenia (telefon, lokalizacja, linki)
- [ ] Uruchomiłam testową kampanię (budżet 30–50 PLN/dzień)
- [ ] Monitoruję wyniki (CTR, konwersje, CPC)

### Email marketing (opcjonalnie)
- [ ] Utworzyłam listę mailingową (Mailchimp / Sendinblue)
- [ ] Dodałam formularz zapisu na stronie
- [ ] Wysłałam pierwszy newsletter (witamy, oferta, portfolio)

---

## 📊 MONITORING (MIESIĘCZNIE)

### Metryki strony
- [ ] Ruch organiczny (Google Analytics)
- [ ] Czas na stronie i bounce rate
- [ ] Konwersje (form_submit, contact_click)
- [ ] Pozycje w Google (Google Search Console)

### Metryki Instagram
- [ ] Liczba obserwujących (followers)
- [ ] Reach i zaangażowanie (engagement rate)
- [ ] Saves i profile visits
- [ ] Zapytania przez DM

### Metryki biznesowe
- [ ] Liczba zapytań (formularz + DM + telefon)
- [ ] Liczba rezerwacji
- [ ] Conversion rate (zapytania → rezerwacje)
- [ ] Źródła ruchu (Google, Instagram, polecenia)

---

## 🎯 CELE (3 MIESIĄCE)

- [ ] Ruch organiczny +30–50%
- [ ] Top 10 w Google dla "fotograf ślubny [miasto]"
- [ ] 5–10 zapytań/miesiąc
- [ ] 2–5 rezerwacji/miesiąc
- [ ] +500 followers Instagram
- [ ] 10+ opinii Google (5 gwiazdek)

---

## 🎉 GRATULACJE!

Jeśli zaznaczyłaś wszystko — stworzyłaś profesjonalną stronę, która będzie przyciągać klientów!

**Pamiętaj:**
- Publikuj regularnie na Instagram (3–5x/tydzień)
- Odpowiadaj na zapytania w 24h
- Zbieraj opinie od każdego klienta
- Monitoruj metryki i optymalizuj

**Sukces to konsekwencja małych kroków każdego dnia. Rób to i będzie działać! 🚀**

---

**Ostatnia aktualizacja:** 2025-01-09  
**Status:** ✅ Gotowe do użycia

