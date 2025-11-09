# Katnami.pl — Fotografia Ślubna | Reportaże | Chrzty | Komunie

Repozytorium strony [katnami.pl](https://katnami.pl) — profesjonalna fotografia ślubna, reportaże, chrzty i komunie.

---

## 📋 Dokumentacja projektu

### 🚀 Szybki start

1. **[MIGRATION_GUIDE.md](MIGRATION_GUIDE.md)** — Krok po kroku: jak skopiować stronę na staging (3 metody: panel hostingu, All-in-One WP Migration, SSH/WP-CLI)
2. **[CONTENT_PLAN.md](CONTENT_PLAN.md)** — Kompletny plan treści, struktury strony, SEO lokalnego, pakietów cenowych, FAQ, portfolio
3. **[TEXTS_CONTENT.md](TEXTS_CONTENT.md)** — Gotowe teksty do wklejenia na stronę (hero, landing pages, opisy usług, FAQ, blog)
4. **[INSTAGRAM_STRATEGY.md](INSTAGRAM_STRATEGY.md)** — Strategia Instagram: reels, posty, stories, współpraca, kalendarz treści, gotowe opisy
5. **[schema-org.html](schema-org.html)** — Schema.org JSON-LD (LocalBusiness, WeddingPhotographer) — SEO
6. **[google-analytics-ga4.html](google-analytics-ga4.html)** — Snippet GA4 + konfiguracja konwersji

---

## 🎯 Cel projektu

Zmiana profilu działalności: **sesje kobiece → fotografia ślubna / reportaże / chrzty / komunie**.

### Główne problemy do rozwiązania:
- ❌ Brak jasnej komunikacji nowej oferty
- ❌ Słabe SEO lokalne
- ❌ Portfolio bez pełnych reportaży
- ❌ Brak pakietów cenowych i CTA
- ❌ Mało dowodów społecznych (opinie)
- ❌ Instagram — mało reportaży i reels

### Rozwiązanie:
✅ Nowa strona z fokusem na fotografia ślubna, reportaże, chrzty, komunie  
✅ Landing pages dla każdej usługi (SEO lokalne)  
✅ Pełne portfolio reportażowe (30–50 zdjęć per reportaż)  
✅ 3 pakiety cenowe + dodatki  
✅ Formularz rezerwacji + GA4 konwersje  
✅ Schema.org + meta SEO  
✅ Strategia Instagram (reels, współpraca z vendorami)  

---

## 📂 Struktura repozytorium

```
katnami.pl/
├── README.md                   # Ten plik
├── MIGRATION_GUIDE.md          # Instrukcja migracji na staging
├── CONTENT_PLAN.md             # Plan treści i struktury strony
├── TEXTS_CONTENT.md            # Gotowe teksty do wklejenia
├── INSTAGRAM_STRATEGY.md       # Strategia social media
├── schema-org.html             # JSON-LD Schema.org
├── google-analytics-ga4.html   # GA4 snippet + konwersje
└── .gitignore
```

---

## 🛠️ Technologie i narzędzia

- **CMS:** WordPress
- **Hosting:** CyberFolks
- **Domena:** katnami.pl (produkcja), staging.katnami.pl (staging)
- **SEO:** Schema.org JSON-LD, meta tags, alt teksty
- **Analytics:** Google Analytics 4 (GA4)
- **Instagram:** @katnami_fotografia_kobieca
- **Wtyczki (rekomendowane):**
  - All-in-One WP Migration (migracja)
  - Contact Form 7 / Gravity Forms (formularze)
  - Rank Math / Yoast SEO (SEO)
  - WP Rocket / W3 Total Cache (cache)
  - Smush / ShortPixel (kompresja obrazów)
  - Insert Headers and Footers (GA4, schema.org)

---

## 📅 Plan wdrożenia (8 tygodni)

### Tydzień 1: Staging i backup
- [ ] Backup produkcji (pliki + baza)
- [ ] Utworzenie subdomeny staging.katnami.pl
- [ ] Migracja na staging (All-in-One WP Migration lub ręcznie)
- [ ] Zabezpieczenie staging (hasło, blog_public=0)
- [ ] Rotacja haseł (panel, WP, e-mail)

### Tydzień 2: Treści i SEO
- [ ] Zaktualizować hero i nagłówek główny
- [ ] Stworzyć 4 landing pages usług (ślub, reportaż, chrzest, komunia)
- [ ] Dodać 3 pełne reportaże do portfolio (30–50 zdjęć każdy)
- [ ] Przygotować 3 pakiety cenowe
- [ ] Napisać FAQ (8–10 pytań)
- [ ] Dodać stronę O mnie
- [ ] Dodać schema.org JSON-LD
- [ ] Optymalizować alt teksty i meta description

### Tydzień 3: Konwersje i narzędzia
- [ ] Zainstalować GA4 i skonfigurować konwersje
- [ ] Dodać formularz kontaktowy (Contact Form 7 / Gravity Forms)
- [ ] Opcjonalnie: integracja Calendly / Dubsado
- [ ] Dodać widget Live Chat (opcjonalnie)
- [ ] Przetestować formularz i płatności

### Tydzień 4: Opinie i Google
- [ ] Uzupełnić Google Business Profile
- [ ] Zebrać 3–5 opinii od klientów (Google Reviews)
- [ ] Dodać sekcję Opinie na stronie
- [ ] Opublikować 2 posty na blogu (SEO)

### Tydzień 5: Instagram i social media
- [ ] Zmienić bio i nazwę profilu Instagram
- [ ] Utworzyć wyróżnienia (Wesela, Chrzty, Reportaże, Opinie)
- [ ] Opublikować 3 reels (reportaże, behind the scenes)
- [ ] Zaplanować kalendarz treści (2 tygodnie w przód)
- [ ] Nawiązać współprace z 2–3 vendorami

### Tydzień 6: Testowanie i optymalizacja
- [ ] Przetestować responsywność (mobile, tablet)
- [ ] Sprawdzić szybkość strony (PageSpeed Insights)
- [ ] Przetestować wszystkie linki i formularze
- [ ] Poprawić błędy 404
- [ ] Dodać redirecty (jeśli zmieniono URL)

### Tydzień 7: Wdrożenie na produkcję
- [ ] Backup staging
- [ ] Backup produkcji (jeszcze raz)
- [ ] Zamienić produkcję na staging (import/migracja)
- [ ] Sprawdzić wszystkie funkcje na produkcji
- [ ] Wysłać sitemap do Google Search Console
- [ ] Monitorować pierwsze 48h (błędy, ruch)

### Tydzień 8: Reklamy i promocja
- [ ] Uruchomić Facebook/Instagram Ads (testowa kampania)
- [ ] Uruchomić Google Ads (Search)
- [ ] Monitorować wyniki (CTR, konwersje, koszt)
- [ ] Optymalizować kreacje i targeting

---

## 📊 Oczekiwane rezultaty (3 miesiące)

### SEO:
- Wzrost ruchu organicznego o 30–50%
- Top 10 w Google dla "fotograf ślubny [miasto]"
- Top 5 dla long-tail ("reportaż ślubny [miejsce]")

### Konwersje:
- 5–10 zapytań/miesiąc z formularza
- 2–5 rezerwacji/miesiąc
- Współczynnik konwersji 3–5%

### Social media:
- +500 followers na Instagram (3 miesiące)
- Zaangażowanie (likes, komentarze) +50%
- 10–20 zapytań z DM/miesiąc

### Opinie:
- 10+ opinii Google (5 gwiazdek)
- 5+ referencji na stronie

---

## 🔐 Bezpieczeństwo

⚠️ **WAŻNE:**
- Natychmiast zmień wszystkie hasła (panel hostingu, WordPress, e-mail)
- Nie publikuj haseł publicznie
- Wykonuj regularne backupy (pliki + baza)
- Używaj silnych haseł i 2FA (gdzie dostępne)
- Zabezpiecz staging (basic auth lub hasło)

---

## 📞 Kontakt

- **Strona:** [katnami.pl](https://katnami.pl)
- **E-mail:** kontakt@katnami.pl
- **Instagram:** [@katnami_fotografia_kobieca](https://www.instagram.com/katnami_fotografia_kobieca/)

---

## 📝 Licencja

Wszystkie treści, zdjęcia i materiały są własnością Katnami Fotografia. Nie kopiuj bez zgody.

---

## 🚀 Następne kroki

1. Przeczytaj **[MIGRATION_GUIDE.md](MIGRATION_GUIDE.md)** i wybierz metodę migracji na staging.
2. Wykonaj backup produkcji (pliki + baza).
3. Skopiuj stronę na staging zgodnie z instrukcją.
4. Zacznij wdrażać zmiany według **[CONTENT_PLAN.md](CONTENT_PLAN.md)**.
5. Użyj gotowych tekstów z **[TEXTS_CONTENT.md](TEXTS_CONTENT.md)**.
6. Wdróż strategię Instagram z **[INSTAGRAM_STRATEGY.md](INSTAGRAM_STRATEGY.md)**.
7. Dodaj schema.org i GA4 (pliki HTML w repo).
8. Testuj na stagingu → merge na produkcję.

**Powodzenia! 🎉**

