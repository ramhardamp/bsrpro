# Screenshots kaise dalein (v2)

1. Image is folder me daalein. Format **png / webp / jpg** — koi bhi chalega (naam same, extension aap ka).
2. Naam neeche ki table jaisa rakhein. **Sirf wahi images dikhengi jo upload hui hongi** — khaali slot website par nahi dikhte.
3. Kisi category me ek bhi image nahi hogi to uska tab apne aap chhup jayega.

## Password Manager (tab: 🔐 पासवर्ड मैनेजर)
| File | Kya dikhana hai | Shape |
|---|---|---|
| pm-01 | Lock / PIN screen | phone (portrait) |
| pm-02 | Vault — password list | phone |
| pm-03 | Add / Edit password | phone |
| pm-04 | Password details | phone |
| pm-05 | Security settings | phone |
| pm-06 | Backup / Restore | phone |
| pm-web-01 | Browser password manager | wide (landscape) |
| pm-web-02 | Browser vault | wide |

## Privacy Shield: ext-01 Monitor · ext-02 Ad blocking · ext-03 Focus · ext-04 Emergency Burn (wide)
## Digital Khata: khata-01 Home · khata-02 Ledger (phone)

## Aur screenshots badhane ke liye
`index.html` me `var SHOTS=[ ... ]` list dhoondhein aur ek line add karein:
`{id:'pm-07',cat:'pm',plat:'phone',hi:'हिंदी नाम',en:'English name'},`
phir `screenshots/pm-07.png` daal dein. `cat` = pm / shield / khata. Naya tab chahiye to `CATS` list me ek line add karein.

**Zaroori:** asli password, email, UPI, phone number screenshot me blur/hide karke hi daalein. Phone screenshots ~720x1520 (portrait), **extension/browser screenshots 1280x800 (16:10, Chrome/Firefox/Edge store ka standard size, poori browser window)**, har image 200 KB se kam (webp best).

## Size guide (koi crop nahi hota — image apne asli size me dikhti hai)
| Type | `plat` | Size | Frame |
|---|---|---|---|
| Android / mobile | `phone` | 720x1520 | phone frame |
| Extension / browser (full window) | `wide` | **1280x800** | browser window frame |
| Sirf chhota extension popup | `popup` | jaisa popup hai (~400x600) | chhota browser frame |

Extension ke liye: browser me extension chalu rakhein, window ko 1280x800 par set karein aur poora screenshot lein (popup/dashboard dikhna chahiye).
