# Fix.md — Website Audit & Fix Log (v2026-10-16)

Format: Issue -> Fix -> Logic

## Done
1. Unverified numbers (500K+, 3.2K stars, 4.9★) -> hataye, "Free / MIT / ₹0" lagaya -> Sirf verifiable claims rakhe.
2. Version mismatch (v1.0.0 vs link V16.3.0) -> card, table, README sab v16.3.0 -> Ek source of truth (release tag).
3. Google Fonts -> hataya, system font stack -> "Zero data collection" claim ke saath consistent, faster load.
4. Share tags -> og:image absolute (og-image.png 1200x630), og:url, twitter large card -> WhatsApp/Twitter preview.
5. JSON-LD -> extension + Android MobileApplication, price INR.
6. Screenshots -> real gallery (filter tabs + lightbox), folder `screenshots/` (naming guide us folder ki README me).
7. Naya "APK Install & Verify" section (sha256 steps, unknown-sources guide).
8. A11y -> <main>, skip-link #main, aria-pressed, aria-expanded, html lang switch.
9. Pages -> privacy.html (PRIVACY.md se), 404.html, .well-known/security.txt, sitemap update.
10. Icons -> icon128 compress (47KB -> 12KB), icon192/512 + manifest PWA icons; duplicate assets/qr-code.png hataya.
11. TODO comments hataye.

## Pending (aapki taraf se / next round)
- Chrome Web Store link (abhi koi URL nahi mila) — footer/products me add karni hai.
- Real screenshots upload karein.
- APK SHA-256 checksum GitHub Release notes me daalein.
- Real downloads/rating numbers (agar chahiye) store link ke saath.
- Custom domain, CSS/JS ko alag files me nikalna (110 inline styles), Digital Khata ka alag page.
- 404.html GitHub Pages par root me automatically kaam karega.

## Round 2 (Legal + Developer)
1. Footer -> 5-column professional footer (Brand, Products, Resources, Legal, Contact) + dynamic copyright year.
2. Copyright -> "(c) 2026 Vikram Singh Rajput"; name/logo/branding all rights reserved, code MIT (dono alag clearly likha).
3. Trademark disclaimer (Firefox/Chrome/Edge/Android/UPI apps) + "as is" no-warranty line.
4. Naya Developer & Contact section (#contact) -> Vikram Singh Rajput, babasitarampro@gmail.com, Issues, GitHub; nav me "संपर्क".
5. terms.html (Terms, Disclaimer, Liability, Donations, Copyright report) + sub-pages me footer; sitemap update.
6. LICENSE holder -> "Vikram Singh Rajput and BABASITARAM PRO Contributors"; SECURITY.md ka placeholder email -> babasitarampro@gmail.com.
7. JSON-LD author me name + email + GitHub.
Note: Terms/Disclaimer general template hain — publish se pehle kisi lawyer se check karwa lein.

## Round 3 (Password Manager screenshots)
1. Issue: gallery me Password Manager ka alag option nahi tha (sirf Android/Extension) -> Fix: 3 tabs (🔐 Password Manager, 🛡️ Privacy Shield, 📒 Digital Khata) + "All".
2. Password Manager ke 8 slots (6 phone + 2 browser) + `SHOTS` config list: ek line = ek naya screenshot.
3. Sirf upload hui images dikhti hain; khaali category ka tab chhup jata hai (koi adhoora/placeholder box nahi). Koi bhi image na ho to "Screenshots coming soon".
4. Format auto-detect (png/webp/jpg), phone/wide alag shape, lightbox me prev/next + arrow keys, Hindi/English captions.

## Round 4 (UI polish + extension screenshot size)
1. Issue: screenshots crop hoke mobile shape me dikh rahe the -> Fix: asli aspect ratio, koi crop nahi. Extension = browser-window frame (1280x800), phone = phone frame, `popup` = chhota frame.
2. Skip-link ka top-left par dikhta cyan block fix; hero badge ab center me (full-width stretch nahi).
3. Polish: smooth scroll, nav-offset anchors, focus-visible ring, card hover, reduced-motion support, frames/shadows.

## Round 5 (teeno products ke screenshots)
1. Issue: sirf ek product ke screenshots dikh rahe the -> Karan: gallery sirf fixed naam (pm-01/ext-01/khata-01) dhoondhti thi aur jis category me naam match nahi hota tha uska tab chhupa deti thi.
2. Fix: auto-discover (har product ke kai prefix: pm/pm-web/android, ext/shield, khata), .png/.jpg/.jpeg/.webp/.PNG/.JPG, gap allowed, optional screenshots.json kisi bhi file naam ke liye.
3. Teeno product tabs hamesha dikhte hain + image count; khaali tab me "coming soon". Frame image ke size se auto (landscape = browser, portrait = phone).
4. Test: android-01.png, android-02.jpg, ext-01.PNG, ext-02.png, khata-01.jpg, khata-03.png (gap) — teeno tabs me sahi dikhe, JS error 0.

## Round 6 (4 products)
1. Issue: Password Manager ek tab me tha, jabki 4 products hain -> Fix: 4 tabs: Password Manager ऐप, Password Manager एक्सटेंशन, Privacy Shield, Digital Khata.
2. Prefix: pm-app/pm/android = ऐप; pm-ext/pm-web = एक्सटेंशन; ext/shield = Privacy Shield; khata = Digital Khata.
3. Sirf `pm-NN` naam ho to portrait = ऐप, landscape = एक्सटेंशन (auto).
