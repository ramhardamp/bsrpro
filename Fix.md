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

## Round 7 (License + verified claims, 2026-10-25) — sirf website/docs
Format: Issue -> Fix -> Logic. Android / extension / Digital Khata source me koi badlav nahi. `LICENSE` file jaan-bujhkar untouched (alag approval pending).
1. License claim (MIT / "100% Open Source") code headers + Shield `LICENSE.txt` + store listings se takra raha tha -> index, privacy, terms, README, PRIVACY, JSON-LD, docs/STORE_SUBMISSION se hataya; "Proprietary — All Rights Reserved" -> Source files me jo likha hai wahi site par; terms me product-wise table, Digital Khata = TBD.
2. "Zero data collection / 100% private / nothing sent to any server" -> scoped: Shield + Password Manager = developer ka koi server data nahi pata; Digital Khata alag (Firebase, EmailJS) -> Code evidence: Khata `dashboard.html` (Firestore, publicViews, EmailJS), PM breach check (`api.pwnedpasswords.com`), Shield filter lists.
3. Encryption claim ("encrypted storage", "heavily encrypted AES-256") -> Android: AES-256-GCM + PBKDF2-HMAC-SHA256 600,000, 16-byte salt (source se); extension vault encryption = TBD -> `chrome.storage.local` khud encrypted nahi hota, isliye unverified claim nahi.
4. Versions (v16.3.0, v19.9.1, v9.2.4, v5.43.8) -> text me `TBD by developer`; download URL / tag nahi badle -> Git tag verify nahi (zip me .git nahi).
5. "100K+ rules" (12+ jagah) -> hataya; "3 filter lists" (EasyList, EasyPrivacy, uBO Annoyances) -> `filter-sync.js` me 3 default URL.
6. Firefox/Edge store claim -> hataya, "Store links: TBD by developer" -> koi store URL nahi mila.
7. SECURITY.md (9.2.x, `yourusername` advisory link) -> nayi file, Android/Extension alag, TBD jahan verify nahi -> Single reference.
8. privacy.html: Android network + permissions section, naya Digital Khata section (verified + unverified alag), purane "Browser Sync / Breach Alert" par version-applicability note -> Shield 9.7.4 me `storage.sync` nahi, Breach Alert sirf haveibeenpwned.com kholta hai; repo 9.2.4 code alag.
9. `llms.txt` naya; `manifest.json` description se "zero data collection" hata; CONTRIBUTING clone URL (`yourusername`) theek kiya.

### Pending / unverified (next round — developer se)
- LICENSE file (abhi MIT) + copyright holder ka legal verification + contributors ki sahmati (`CONTRIBUTING.md:151` "contributions MIT me").
- Repo public/private ka nirnay; `index.html` "Source Code Available" line abhi waisi hi.
- Git release tag, APK SHA-256, signing cert fingerprint (CI me expected cert value hai, asli APK se match nahi kiya), built APK ki merged permissions.
- Digital Khata: Firestore rules, `publicViews` access, retention/deletion, Cloud Functions, login pages, native plugins (partial source — complete audit nahi).
- Extension vault encryption; Shield DoH behavior; Browser Sync / Breach Alert kis version par lagu.
- Developer list (code me): debug build release key se sign, `RootDetector` kahin use nahi, Lottie license list me nahi, manifest comment READ_CONTACTS, repo `src/chrome` 9.2.4 vs asli Shield 9.7.4.

## Round 8 (LICENSE lagu + bache hue sudhaar, 2026-10-25)
Developer ne explicit approval di: licence = Proprietary — All Rights Reserved. Format: Issue -> Fix -> Logic.
1. `LICENSE` MIT tha -> Proprietary license (effective 25 Oct 2026) -> Purane MIT copies wapas nahi liye ja sakte, isliye clause 2 me "retroactive nahi" saaf likha; contributors aur third-party ke alag clause.
2. `CONTRIBUTING.md` "contributions MIT me" -> ab: owner ko perpetual license (proprietary terms ke saath), contributor apna ownership rakhta hai; 25 Oct 2026 se pehle ke contributions MIT par hi rahe -> Bina CLA ke relicense ka risk band.
3. `terms.html` Khata row "TBD" -> "Proprietary (developer decision)"; "pending" wording `README.md` se hataya.
4. Naya `scripts/release-checksums.sh` + `SECURITY.md` me verify steps -> APK SHA-256 / cert fingerprint ab ek command se; asli values release page par developer dega (TBD).
5. Android (is zip me NAHI, alag patch `android-small-fixes.patch`): READ_CONTACTS manifest comment, "Licenses" screen me Lottie (Apache-2.0) -> Pehle attribution list adhoori thi.

### Abhi bhi pending (jaan-bujhkar nahi badla)
- Git release tag, APK SHA-256, signing fingerprint (asli APK/tag chahiye).
- Debug build release key se sign hota hai (`build.gradle.kts`): PASS15 me yeh update-in-place ke liye jaan-bujhkar hai; badalne se purane installs par update toot sakta hai -> developer nirnay.
- `RootDetector` kahin use nahi hota: banner jodna naya feature hai (Fix.md me nahi) -> developer batayein; website par root claim nahi hai.
- Digital Khata ke Firestore rules, `publicViews` access, retention/deletion, Cloud Functions.
- Extension vault encryption, Shield DoH, Sync/Breach Alert version applicability.
- Repo public/private ka nirnay; `index.html` "Source Code Available" line.

## Round 9 (src/ public repo se hataya, 2026-10-25)
Developer ka nirnay: extension source private repo me. Website/docs only. Format: Issue -> Fix -> Logic.
1. `src/` (Shield 9.2.4 source) public repo me tha -> public ZIP se hataya, `bsrpro-PRIVATE-repo-bundle.zip` me diya -> Proprietary license ke saath public source mel nahi khata.
2. `scripts/build.sh`, `scripts/validate.sh` `src/` ke bina nahi chalte -> private bundle me jaise-ke-taise gaye; public repo me naya `scripts/validate-site.sh` (required files, JSON/JSON-LD, local links, "open source / MIT / zero data / 100K+" jaise dave nahi, `src/` nahi) -> Test: private bundle me validator pass + `build.sh all` ka dist original repo se byte-identical; public validator galat input par FAIL hota hai.
3. `docs/ARCHITECTURE.md`, `docs/STORE_SUBMISSION.md` (internal paths, build steps) -> private bundle me; public `docs/` hataya.
4. `CONTRIBUTING.md` (src paths + build steps) -> chhoti public policy: bug report Issues/email, security SECURITY.md, code contribution sirf invitation par + contributor terms.
5. `README.md`: Project Structure, Architecture, "Building From Source", contributing quick-start hataye -> "What is in this repository" + Contributing; "Zero telemetry / No account required / Breach Alert (own API key)" ko scoped/version-dependent kiya.
6. `index.html`: "Source Code Available" (4 jagah), "Source code and documentation included" (3 jagah), "पूरा source code खुला है — GitHub पर देखें" -> hataye (source ab private hai).

### Pending (abhi bhi)
- GitHub links: site ke ~35 links `github.com/ramhardamp/babasitaram-pro` (releases, issues, SECURITY.md, LICENSE) ki taraf jaate hain. Us repo ko private karne se pehle Releases public repo me hone chahiye aur links badalne chahiye (alag script `switch-repo-links.sh` di gayi).
- Site ke canonical/og:url `ramhardamp.github.io/babasitaram-pro/` kehte hain, jabki app `ramhardamp.github.io/bsrpro/` use karta hai -> asli Pages URL developer confirm kare.
- README me Firefox (AMO) aur Edge store links hain (developer ke diye) — live hone ki jaanch nahi hui; index FAQ me store claim abhi bhi `TBD`.
- Git history: purani `src/` public history me rahegi (filter-repo ya nayi repo chahiye).

## Round 10 (Privacy Shield 9.7.7 facts, 2026-10-28)
Source: developer ka `PRIVACY_SHIELD_FACTS_9.7.7.md` (har jawab ke saath saboot). Maine 9.7.7 ka source khud nahi dekha — website par yahi likha hai ("developer's build record"). Format: Issue -> Fix -> Logic.
1. Shield version `TBD` tha -> index.html card par `v9.7.7`; privacy.html/PRIVACY.md/llms.txt/README me "build 9.7.7, release tag TBD" -> facts file sec 1, 4.
2. privacy.html + PRIVACY.md me purana text ("Cloud Sync" storage.sync, email Breach Alert with HIBP API key, DoH "browser routes DNS", uBlock list host `ublockorigin.com`) 9.7.7 se match nahi karta tha -> Sync: nahi hai (removed 9.7.0); Breach: sirf haveibeenpwned.com kholta hai, email collect/send nahi; DoH: default off, extension DNS khud set nahi karti; lists ke asli URL (easylist.to, raw.githubusercontent.com); IP/User-Agent host ko dikhta hai -> facts sec 5-8.
3. New Tab favicon: 9.7.7 se site ka apna `/favicon.ico` (pehle Google/DuckDuckGo) -> privacy.html me naya sub-section + third-party table row -> facts sec 5 #6.
4. "No analytics/telemetry" -> sirf "source code scan ka natija" likha (store listing alag) -> facts sec 10.
5. SECURITY.md: Shield ke verified network/sync/breach/DoH points + 9.7.7 Chrome/Firefox zip SHA-256 (developer record, build 2026-10-28; release page ki file se match zaroori).
6. CHANGELOG.md: Shield 9.6.13–9.7.7 ka entry (facts file ke release notes se); 9.2.5–9.6.12 `TBD`.
7. README: "every 12 hours" (saboot nahi) -> "on start-up and on a timer; interval TBD".

### Pending / jo facts file me SABOOT NAHI tha
- Git tag / release link / date; Edge zip (alag build nahi bana); Chrome Web Store / AMO / Edge live links aur status.
- Shield 9.7.7 `manifest.json` ki permission list (privacy.html ka permissions table general hai, note laga diya).
- index.html ke Shield download buttons abhi purane tag `release-9.6.29` par hain -> 9.7.7 release publish hone par developer tag/link badle (maine tag guess nahi kiya).
- Tests (developer record): unit 450 checks 0 fail; Chromium e2e suites pass; e2e_youtube 17/18, 17/18, 18/18 (P3 intermittent); real Firefox/Edge/Android/real YouTube/real EasyList download NAHI chale. Website par test-pass ka koi dava nahi joda.
