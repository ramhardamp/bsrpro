<div align="center">

# 🛡️ BABASITARAM PRO

### Ultimate Privacy Shield · BSRPRO Vault · Location Guard · Android

![License](https://img.shields.io/badge/license-MIT-ffcc00?style=for-the-badge)
![Platforms](https://img.shields.io/badge/platform-Chrome%20%7C%20Firefox%20%7C%20Edge%20%7C%20Android-green?style=for-the-badge)
![Open Source](https://img.shields.io/badge/Open%20Source-100%25-brightgreen?style=for-the-badge)

**Ad & tracker blocking · Encrypted password vault · OTP · Location spoofing · Focus Mode · Emergency Burn**

[📦 Releases](https://github.com/ramhardamp/babasitaram-pro/releases) · [🐛 Report Bug](https://github.com/ramhardamp/babasitaram-pro/issues) · [💡 Request Feature](https://github.com/ramhardamp/babasitaram-pro/issues) · [🌐 Website](https://ramhardamp.github.io/bsrpro/)

</div>

---

## 🌟 About BABASITARAM PRO

BABASITARAM PRO is a free, open-source privacy toolkit for browsers and Android. Its products help you block ads and trackers, manage encrypted credentials, control what location websites receive, and protect your browsing workflow.

| Product | Version | Purpose |
|---|---|---|
| 🛡️ Ultimate Privacy Shield | **v9.2.4** | Ad blocking, tracker protection, site locking, focus tools, and cleanup |
| 🔐 BABASITARAM PRO Password Manager / BSRPRO Vault | **v5.43.8** | Local password and OTP management for browsers |
| 📱 BSRPRO Vault Android App | **APK** | Encrypted password vault and Android autofill |
| 📍 Location Guard BSRPRO | **v1.2.2** | Replace the location returned by the browser Geolocation API |

> **Privacy note:** Products and versions can have different capabilities. Features below apply to the named product, not automatically to every app or extension.

## 🛡️ Ultimate Privacy Shield (v9.2.4)

<details open>
<summary><b>Ad blocking and browsing protection</b></summary>

- Ad and tracker blocking with EasyList, EasyPrivacy, and uBlock Origin annoyance filters.
- Custom element picker and site-specific CSS blocking rules.
- Per-site statistics and activity dashboard.
- Optional HTTPS and DNS-over-HTTPS settings where supported.
- Site lock, PIN protection, and protected/fireproof site lists.
- Cookie and browsing-data cleanup, plus **Emergency Burn**.
- Focus Mode, site time limits, and tab-oriented privacy features.
- Automatic filter-list updates where supported.

</details>

## 🔐 BSRPRO Vault — Password Manager

**आपके पासवर्ड, OTP और ज़रूरी जानकारी — एक सुरक्षित तिजोरी में।**

BSRPRO Vault is designed for Android and browser extensions, with locally encrypted vault data and portable backups.

### 🔒 Security features

| Feature | Description |
|---|---|
| AES-256-GCM | Encrypts vault contents on the device |
| PBKDF2 (600,000 rounds) | Derives an encryption key from the master password |
| Master password and biometrics | Unlock options on supported devices |
| Auto-lock | Configurable timeout (30 seconds to 15 minutes) |
| Failed-attempt lockout | Temporarily restricts repeated failed unlocks |
| Screenshot protection | Helps prevent screen capture in supported Android views |
| Clipboard auto-clear | Clears copied sensitive text after a delay |
| Root detection | Warns when Android device security may be weakened |
| Local vault | No developer-operated vault storage server |

### 📱 Android app features

1. **Autofill:** Username/password suggestions for apps and websites; inline suggestions where Android supports them.
2. **Separate app and website logins:** Organize entries by app or domain.
3. **Built-in TOTP / 2FA:** Add accounts with QR codes, view time-based codes, and copy OTPs.
4. **Password generator:** Generate strong random passwords.
5. **Vault Health:** Find weak or reused passwords and optionally check for exposed passwords using k-anonymity.
6. **More than passwords:** Encrypted notes, phone numbers, files, cards, identity details, and imported contacts.
7. **Organization:** Folders, categories, tags, favorites, sorting, and typo-tolerant search.
8. **Hidden Vault:** Additional PIN-protected area for private entries.
9. **Secure sharing and emergency access:** Options for selected entries; review their sharing mechanism before use.
10. **Recycle Bin:** Recover deleted entries during the configured retention period (described as 30 days).
11. **Activity history and recovery:** Local activity logs and a recovery-key export workflow.
12. **Convenience:** Home-screen widget, quick-settings tile, and Hindi/English help where available.

### 🌐 Chrome and Firefox password manager

- Login-field autofill and save/update prompts.
- Password entry search, edit, delete, and history.
- Built-in OTP management and QR export.
- PIN unlock and auto-lock.
- Vault Health, sharing, and emergency-access tools where supported.
- **BSRPRO.Vault** backup format for moving encrypted vault data between supported app and extension versions.

### 💾 Backup, restore, import, export

- Encrypted `.Vault` backup protected by the master password.
- Optional scheduled local backups to a folder you choose.
- Restore from a saved backup on a replacement device.
- CSV imports from supported browsers and password managers, including Chrome/Edge, Firefox, Bitwarden, LastPass, 1Password, Dashlane, NordPass, and KeePass; vCard contacts where supported.
- Import preview and duplicate detection.
- Exports in encrypted Vault format and supported CSV/JSON formats.

> **Security warning:** CSV and JSON exports may be unencrypted. Store them securely and delete unnecessary copies. Keep recovery keys and backups in a safe place.

### 🚀 तीन आसान कदम

1. ऐप इंस्टॉल करें और मज़बूत मास्टर पासवर्ड बनाएँ।
2. पासवर्ड जोड़ें या इम्पोर्ट करें और Android सेटिंग्स में BSRPRO Vault को Autofill Service चुनें।
3. ब्राउज़र एक्सटेंशन जोड़ें और ज़रूरत हो तो एन्क्रिप्टेड बैकअप से डेटा ट्रांसफ़र करें।

## 📍 Location Guard BSRPRO (v1.2.2)

Location Guard BSRPRO lets you choose a location for websites to receive **instead of the browser's real Geolocation API result**.

- **ON/OFF control:** Enable or disable location spoofing.
- **Choose coordinates:** Set a latitude, longitude, and accuracy value.
- **Map and place search:** Find a location on a map or search by name.
- **Local preferences:** The chosen location, place name, accuracy, and switch state are saved using `chrome.storage.local`.
- **No real-location collection:** The extension is designed not to read or store your actual GPS location.
- **No IP masking:** Websites may still estimate your approximate area from your IP address.
- **Page limitations:** Browser-internal pages are not affected; some websites may use other location signals.

### 🗺️ Map and search network requests

When you use the popup map or search, third-party services may receive the displayed map area, search text or selected coordinates, and standard network metadata such as your IP address:

| Service | Use |
|---|---|
| OpenStreetMap tiles | Default map tiles |
| CARTO / Esri | Fallback map tiles |
| OpenStreetMap Nominatim | Place search and reverse geocoding |

These requests go to the relevant providers, **not to the developer**. Location Guard does not use browser sync.

### 🔑 Location Guard permissions

| Access | Reason |
|---|---|
| `storage` | Save chosen coordinates and settings locally |
| Content script matching `<all_urls>` | Respond to website geolocation requests on supported pages |
| MAIN-world page script | Override the page's Geolocation API behavior |

Location Guard does not request `tabs`, `activeTab`, `scripting`, `cookies`, or `history` permissions according to the supplied extension description.

## 📥 Installation & downloads

### 📱 Android APK

[⬇️ Download Android APK (v1.0.0)](https://github.com/ramhardamp/babasitaram-pro/releases/download/1.0.0/BSRPRO-PM-Android.apk) · [📄 Release notes](https://github.com/ramhardamp/babasitaram-pro/releases/tag/1.0.0)

> Install APKs only from a release you trust. Confirm the latest available version and package details on the Releases page.

### 🦊 Firefox

- [Ultimate Privacy Shield](https://addons.mozilla.org/en-US/firefox/addon/ultimateprivacyshield/)
- [BABASITARAM Password Manager](https://addons.mozilla.org/en-US/firefox/addon/babasitaram-password-manager/)

### 🌐 Chrome / Chromium

Download the relevant extension ZIP from [GitHub Releases](https://github.com/ramhardamp/babasitaram-pro/releases), extract it, open `chrome://extensions`, enable **Developer mode**, then choose **Load unpacked** and select the extension folder. A verified Chrome Web Store URL can be added when available.

### 🟦 Microsoft Edge

[Ultimate Privacy Shield — Edge Add-ons](https://microsoftedge.microsoft.com/addons/detail/0RDCK99NZNZ1)

### 📍 Location Guard BSRPRO

Check [GitHub Releases](https://github.com/ramhardamp/babasitaram-pro/releases) for its browser package and installation instructions. A store link can be added once confirmed.

## 🔐 Privacy & security

- No developer-operated backend server for vault storage.
- Local settings are stored in browser storage or Android device storage, depending on the product.
- Browser sync is optional for supported extensions and is provided by the browser vendor; **Location Guard does not use it**.
- Some features contact third-party services directly: filter-list hosts, optional breach-check services, selected DNS providers, and Location Guard map/search providers.
- Location Guard does not conceal your IP address.
- Backup files and exported data are controlled by you; unencrypted exports require extra care.

**Privacy Policy:** [Read the policy](https://github.com/ramhardamp/babasitaram-pro/blob/main/privacy.html)

> The security and feature descriptions in this README reflect project-provided specifications. Review the implementation and current release before relying on a feature for sensitive data.

## 🏗️ Building from source

### Prerequisites

- Bash, ZIP, and Python 3
- Git Bash or WSL on Windows

```bash
git clone https://github.com/ramhardamp/babasitaram-pro.git
cd babasitaram-pro

# Build browser extension packages
bash scripts/build.sh chrome
bash scripts/build.sh firefox
bash scripts/build.sh all

# Validate
bash scripts/validate.sh
```

> Build commands above refer to the Ultimate Privacy Shield project layout. Android, Vault, and Location Guard may have separate build instructions.

### Browser architecture

The Chrome and Firefox builds use browser-specific background implementations to accommodate differences in Manifest V3 APIs. Filter-list parsing converts supported rules into browser blocking rules. Consult source files for current platform support and implementation details.

## 🤝 Contributing

Contributions are welcome. Read [CONTRIBUTING.md](CONTRIBUTING.md), review open [issues](https://github.com/ramhardamp/babasitaram-pro/issues), and run project validation before opening a pull request.

```bash
git checkout -b feature/your-feature-name
# Make changes
bash scripts/validate.sh
git commit -m "feat: describe your change"
git push origin feature/your-feature-name
```

## 📋 Changelog

- **Ultimate Privacy Shield v9.2.4:** Browser-specific background builds, DOM safety improvements, message handling, and compatibility updates.
- **Password Manager v5.43.8:** Current browser password-manager version supplied for this documentation update.
- **Location Guard BSRPRO v1.2.2:** Browser geolocation spoofing, map/place search, local preferences.
- **Android APK v1.0.0:** Initial Android release linked above; BSRPRO Vault feature set is documented separately.

See [CHANGELOG.md](CHANGELOG.md) for detailed release history.

## ❓ Frequently asked questions

**क्या मेरा Vault डेटा सर्वर पर जाता है?**  Vault को स्थानीय रूप से एन्क्रिप्टेड रखने के लिए डिज़ाइन किया गया है। कुछ वैकल्पिक सुविधाएँ सीधे तीसरे पक्ष की सेवाओं से संपर्क करती हैं।

**मास्टर पासवर्ड भूल जाएँ तो?**  पहले से बनाई गई रिकवरी की या बैकअप प्रक्रिया का उपयोग करें। रिकवरी सामग्री सुरक्षित रखें।

**फ़ोन बदलने पर क्या करें?**  अपना एन्क्रिप्टेड बैकअप नए डिवाइस पर लाएँ और सही मास्टर पासवर्ड से रीस्टोर करें।

**क्या Location Guard मेरा IP छिपाता है?**  नहीं। यह केवल समर्थित वेब पेजों पर Geolocation API का जवाब बदलता है।

**क्या ऐप मुफ़्त है?**  परियोजना का घोषित उद्देश्य मुफ़्त, ओपन-सोर्स उपयोग उपलब्ध कराना है।

## 💖 Support

BABASITARAM PRO is offered free of charge. Optional donations help support development and maintenance.

**UPI:** `Totalpay@upi`

<img src="./upi-qr.png" width="180" alt="UPI donation QR code" />

## 📄 License & acknowledgements

Licensed under the [MIT License](LICENSE).

Thanks to the maintainers and communities behind EasyList, EasyPrivacy, uBlock Origin filter assets, Have I Been Pwned, OpenStreetMap, CARTO, and Esri. Third-party services retain their own terms and privacy policies.

## 📬 Contact

**Developer:** VIKRAM SINGH RAJPUT  
**Email:** babasitarampro@gmail.com  
**GitHub:** [ramhardamp/babasitaram-pro](https://github.com/ramhardamp/babasitaram-pro)  
**Website:** [ramhardamp.github.io/bsrpro](https://ramhardamp.github.io/bsrpro/)

<div align="center">

Made with ❤️ and 🕉️ · **श्री राम जय राम जय जय राम**

⭐ Star the repository if you find it useful!

</div>
