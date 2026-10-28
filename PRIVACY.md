Last updated: 25 October 2026 · Version: TBD by developer

Applies to:

BABASITARAM PRO — Ultimate Privacy Shield (build 9.7.7; release tag: TBD by developer)
BABASITARAM PRO Password Manager (version: TBD by developer)
BSRPRO Digital Khata (version: TBD by developer) — separate data flow, see privacy.html
BABASITARAM PRO Android App (APK)
Developer: VIKRAM SINGH RAJPUT

---

## 🔒 Our Commitment

**BABASITARAM PRO does not operate any backend server, and the developer does not collect, receive, or have access to any of your data.**

All settings, preferences, and statistics are stored **locally on your device** using the browser's built-in storage APIs (`chrome.storage.local`). This data never leaves your device unless you explicitly export it yourself.

We do **not** collect:
- ❌ Personal information (name, email, address, etc.)
- ❌ Browsing history
- ❌ Usage statistics
- ❌ Analytics or telemetry
- ❌ Cookies or credentials
- ❌ Health, financial, or authentication data
- ❌ Location data

**Privacy Shield and Password Manager: no account is required. Digital Khata requires an account (Firebase Authentication); see privacy.html.**

---

## 📌 What Data Is Stored, And Where

The following data is stored **locally on your device** using `chrome.storage.local`:

| Data Type | Purpose |
|---|---|
| **Settings & Preferences** | To remember your chosen configuration (ad blocker, HTTPS, etc.) |
| **Whitelist / Fireproof Sites** | To protect specific sites from cleaning |
| **Vault Sites** | To password-protect sensitive sites |
| **PIN (hashed)** | To unlock the Vault — stored locally, never transmitted |
| **Custom Block Rules** | To remember element picker and CSS rules |
| **Time Limits** | To track daily time spent per domain |
| **Activity Logs** | To show recent activity in the popup |
| **Statistics** | To display ads blocked, trackers blocked, etc. |

This data **never leaves your device** unless you explicitly use the **Export Backup** feature (Settings → Export Backup). Even then, the exported file is saved on your own device and is not transmitted to us.

---

## ☁️ Browser Sync

**Privacy Shield 9.7.7 has no Cloud Sync / browser sync.** Its code does not use `chrome.storage.sync` and its manifest has no sync permission. Cloud Sync was removed in version 9.7.0; all Privacy Shield data stays in local storage. Versions older than 9.7.0: TBD by developer. Password Manager sync behaviour: TBD by developer.

---

## 🌐 Network Requests Privacy Shield Makes (build 9.7.7)

*Source: the developer's build record for 9.7.7 (scan of the 9.7.7 source for `fetch`, XMLHttpRequest, `sendBeacon`, WebSocket, EventSource, `new Image`, `setUninstallURL`). The 9.7.7 source itself was not re-reviewed for this website update.*

### 1. Filter List Updates (Automatic)
Downloaded when the extension starts and on a timer:

- **EasyList** — `https://easylist.to/easylist/easylist.txt`
- **EasyPrivacy** — `https://easylist.to/easylist/easyprivacy.txt`
- **uBlock Origin Annoyances** — `https://raw.githubusercontent.com/uBlockOrigin/uAssets/master/filters/annoyances.txt`

Plain GET downloads. No data about you or your browsing is sent in the request, but the hosts (easylist.to, GitHub) can see your IP address and browser User-Agent, as with any download.

### 2. New Tab saved-site logos
From 9.7.7 the logo of a saved site comes from that site's own `/favicon.ico` (or a letter avatar). Earlier versions used Google and DuckDuckGo icon services, which received each saved site's domain; removed in 9.7.7.

### 3. Breach Check (link only)
- The "Open haveibeenpwned.com" button only opens the website in a tab.
- The extension does not collect or send any email and has no API key. No HIBP API request is made.
- An email-based "Breach Alert" is **not** part of 9.7.7 (older versions: TBD by developer).

### 4. DNS-over-HTTPS setting
- Default **off**. Choices: Off, Cloudflare, Google, Quad9.
- **The extension does not set your DNS itself.** It saves your choice and opens your browser's own settings page (Chrome: `chrome://settings/security`; Firefox: `about:preferences#privacy`). You then choose "Use secure DNS" in the browser.

### 5. Links that open only when you click
haveibeenpwned.com (breach button), `ramhardamp.github.io/bsrpro` (developer page) and your chosen search engine from the New Tab search box.

### No analytics or telemetry
The 9.7.7 code scan found no analytics, telemetry or crash-report endpoint (no `sendBeacon`, WebSocket, EventSource or `setUninstallURL`) and no external fonts, scripts, stylesheets or images in the extension pages. This is a statement about the source code scan; store listings are separate.

---

## 🔑 Permissions Explained

*General description. The exact permission list of build 9.7.7 is in its `manifest.json` (list for this build: TBD by developer).*

| Permission | Why It's Needed |
|---|---|
| `storage` | To save your settings/lists locally |
| `tabs` | To know the current tab's URL for per-site features |
| `cookies`, `browsingData`, `history` | Used only for Cookie Cleaner, Emergency Burn, and Fireproof features — all local, user-initiated |
| `declarativeNetRequest` | To block ads/trackers at the network layer |
| `webNavigation` | To detect page navigation for site-specific features |
| `idle` | To trigger auto-cleanup when the browser is idle |
| `alarms` | To schedule periodic filter list updates and nightly cleanup |
| `contextMenus` | To add right-click menu items ("Block this site", "Pick element") |
| `host_permissions` (`<all_urls>`) | Required so ad-blocking, site-lock, and element picker can run on any site you visit |

**Permissions are used for the features described in privacy.html. For network requests, see privacy.html ("Network Requests", Android section).**

---

## 🔗 Third Parties

**We do not sell, rent, or share any data, because we never receive any.**

The only third parties your browser ever talks to as a direct result of using this extension are:

| Service | Purpose | When It Runs |
|---|---|---|
| EasyList / EasyPrivacy | Filter list downloads | Automatically (periodic) |
| uBlock Origin Annoyances | Filter list downloads | Automatically (periodic) |
| haveibeenpwned.com | Opened as a website only (breach button) | Only when you click the button |
| The saved site itself (`/favicon.ico`) | New Tab saved-site logo (9.7.7) | When the New Tab page shows a saved site |

---

## 🧒 Children's Privacy

This extension does not knowingly collect any personal information from children under 13. The extension is designed for general use and does not target children.

---

## 📝 Changes to This Policy

If this policy changes, the updated version will be included with the next extension update and posted to:

[https://github.com/ramhardamp/babasitaram-pro](https://github.com/ramhardamp/babasitaram-pro)

The "Last updated" date at the top of this page will also be revised.

---

## 📬 Contact

Questions about this policy:

📧 **babasitarampro@gmail.com**

**Developer:** VIKRAM SINGH RAJPUT  
**GitHub:** [https://github.com/ramhardamp/babasitaram-pro](https://github.com/ramhardamp/babasitaram-pro)

---

## ✅ Summary

| Question | Answer |
|---|---|
| Do you collect my data? | ❌ **No** |
| Do you store my data on your servers? | ❌ **No** |
| Do you sell my data? | ❌ **No** |
| Do you share my data? | ❌ **No** |
| Do you use analytics or telemetry? | ❌ **No** |
| Is my data stored locally? | ✅ **Yes** |
| Can I export my data? | ✅ **Yes** (Settings → Export Backup) |
| Can I delete my data? | ✅ **Yes** (uninstall the extension) |
| Is my PIN transmitted anywhere? | ❌ **Never** |
| Is my browsing history sent anywhere? | ❌ **Never** |
| Does the Breach Check button send data to you? | ❌ **No** — it only opens haveibeenpwned.com; no email is collected or sent |

---

**BABASITARAM PRO is, and always will be, 100% free. No paywalls, no locked features, no telemetry, no tracking. Your privacy is the product — not you.**
