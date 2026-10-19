# Screenshots kaise dalein (v4 — auto)

Images is folder me daalein. **Koi code/config badalne ki zaroorat nahi** — website khud dhoondh leti hai.

## Naam ka niyam: `<prefix>-01`, `-02`, `-03` ...
| Product | Prefix (koi bhi ek) | Example |
|---|---|---|
| 🔐 Password Manager **ऐप** (Android) | `pm-app`, `pm`, `android` | pm-app-01.png, android-02.png |
| 🧩 Password Manager **एक्सटेंशन** (browser) | `pm-ext`, `pm-web` | pm-ext-01.png, pm-web-01.jpg |
| 🛡️ Privacy Shield (extension) | `ext`, `shield` | ext-01.png, shield-02.webp |
| 📒 Digital Khata (app) | `khata` | khata-01.png |

- Extension: png / jpg / jpeg / webp (aur .PNG / .JPG) — sab chalenge. Har prefix me 15 tak images.
- Beech me ek number chhoot jaye (01, 03) to bhi chalega; do lagataar number chhootne par aage nahi dhoondhta.
- **Frame/size apne aap tay hota hai:** landscape image (jaise 1280x800) = browser-window frame, portrait (720x1520) = phone frame. Koi crop nahi.
- Chaaron products ke tabs hamesha dikhte hain. Jis product ki image nahi, usme "जल्द आएँगे" dikhta hai.

**Tip:** sirf `pm-01...` naam diya ho to website khud tay kar leti hai — portrait image = Password Manager ऐप, landscape image = Password Manager एक्सटेंशन.

## Agar aapki files ke naam alag hain
`screenshots/screenshots.json` banayein:
```json
[
  {"file": "mera-vault.png", "cat": "pmapp", "hi": "Vault सूची", "en": "Vault List"},
  {"file": "dashboard.jpg", "cat": "shield", "hi": "डैशबोर्ड", "en": "Dashboard"},
  {"file": "udhaar.png", "cat": "khata", "hi": "उधार खाता", "en": "Udhaar Ledger"}
]
```
`cat` = `pmapp` (PM ऐप) / `pmext` (PM एक्सटेंशन) / `shield` / `khata`.

## Size
Extension/browser **1280x800**, phone ~720x1520, har image 200 KB se kam (webp best).
**Asli password, email, UPI, phone number blur karke hi daalein.**
