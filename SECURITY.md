# Security — BABASITARAM PRO

Last updated: 25 October 2026 · Version: TBD by developer

This file is the single reference for security statements. Website pages link here instead of repeating different text.
Every statement below comes from the source code reviewed for this update. Items marked **TBD by developer** are not verified.

## Scope
- Android app (BSRPRO Vault)
- Browser extensions: Password Manager, Privacy Shield
- **Digital Khata is not covered here.** It uses online services (Firebase, EmailJS). See [privacy.html](https://ramhardamp.github.io/bsrpro/privacy.html). Only a partial source package was reviewed, so no complete audit exists for it.

## Android app — encryption (verified in source)
- Cipher: AES in GCM mode (`AES/GCM/NoPadding`), 256-bit key
- Key from master password: PBKDF2-HMAC-SHA256, 600,000 iterations, 16-byte salt
- Keys protected with Android Keystore (`AndroidKeyStore`, AES/GCM): master key, biometric session key, pending-save data
- Biometric unlock: `androidx.biometric`
- No SCrypt or Argon2 is used
- Cleartext network traffic is disabled; `allowBackup` is false

## Android app — behaviour (verified in source)
- Screenshots / screen recording: blocked by `FLAG_SECURE` by default; the setting "Allow screenshots" (default off) can lift it
- Auto-lock default: 1800 seconds (30 minutes)
- Clipboard auto-clear options: Never, 15, 30, 60 seconds (default: TBD by developer)
- Encrypted backups use the master password. Plain CSV / JSON exports are **not encrypted**; the app shows a warning and asks for the master password first
- Auto-backup folder (if enabled): `Downloads/BSRPRO_Backups`

## Android app — network activity
| Feature | Endpoint | What is sent | Optional |
|---|---|---|---|
| Password breach check | `api.pwnedpasswords.com/range/` | First 5 characters of the SHA-1 hash of a password | Yes; the Breach page is off by default |

No other network use was found in the Android source reviewed.

## Android app — permissions (source manifest; merged permissions of the built APK: TBD by developer)
| Permission | Why |
|---|---|
| USE_BIOMETRIC, USE_FINGERPRINT | Biometric unlock |
| CAMERA | 2FA QR scan only; image analysed in memory, not saved (manifest comment) |
| READ_CONTACTS | Contacts Import screen (name and phone number) |
| INTERNET | Optional breach check |
| POST_NOTIFICATIONS, VIBRATE | Notifications, vibration |
| Autofill service, Quick Settings tile | Services protected by BIND_AUTOFILL_SERVICE and BIND_QUICK_SETTINGS_TILE |

## Browser extensions (source reviewed)
- Password Manager: backup encryption AES-256-GCM with PBKDF2 (100,000 iterations); PIN unlock derives a non-extractable AES-GCM key with PBKDF2. Encryption of the stored vault: **TBD by developer**
- Password Manager network: optional breach check to `api.pwnedpasswords.com/range/` (5-character hash prefix)
- Privacy Shield 9.7.7 (developer's build record; 9.7.7 source not re-reviewed for this update):
  - Network: filter-list downloads from `easylist.to` (EasyList, EasyPrivacy) and `raw.githubusercontent.com` (uBlock Origin Annoyances); the New Tab shows a saved site's own `/favicon.ico`. No analytics, telemetry or crash-report endpoint was found by the code scan
  - No `chrome.storage.sync` and no sync permission (Cloud Sync removed in 9.7.0). Breach button only opens haveibeenpwned.com (no email collected or sent)
  - DNS-over-HTTPS: default off; the extension does not set DNS itself, it only opens the browser's settings page
  - Details: privacy.html
- Manifest permissions are listed in each extension's `manifest.json`

## Known limitations
- If you lose your master password and have no backup, the vault cannot be recovered
- Root / tamper detection: the app does not claim any. A root-check class exists in the source but is not used by the interface
- Anyone who can unlock your phone and the app can see your vault

## Verify a release
- Release: TBD by developer (git tag / release link not yet confirmed)
- Privacy Shield 9.7.7 zips, SHA-256 as recorded in the developer's build record (built 2026-10-28). The file on the release page must match; if not, do not install it and write to us:
  - `BSRPRO-Privacy-Shield-v9.7.7-CHROME-STORE.zip` — `d61cf29f280be50192824e35ae93407c57a56ebd3da27e00747e1f21548cf23f`
  - `BSRPRO-Privacy-Shield-v9.7.7-FIREFOX.zip` — `62ed4bc366658951e9193be60c78ebe04403b9f20012aef64cf69a3eb49e96c3`
  - Check with `sha256sum <file>`
- SHA-256 of the APK: TBD by developer (published on the release page)
- Signing certificate SHA-256 fingerprint: TBD by developer (published on the release page)
- To check a downloaded APK yourself: `sha256sum <apk file name>` and `apksigner verify --print-certs <apk file name>`. The script `scripts/release-checksums.sh <apk file name>` prints both.
- Build instructions: TBD by developer
- Independent audit: TBD by developer

## Report a vulnerability
- Email: babasitarampro@gmail.com
- Please do not report vulnerabilities in public issues
- Response and disclosure timeline: TBD by developer


## Privacy Shield v9.7.7 release artifact
- Release page: https://github.com/ramhardamp/bsrpro/releases/tag/V9.7.7
- Chrome ZIP: https://github.com/ramhardamp/bsrpro/releases/download/V9.7.7/BSRPRO-Privacy-Shield-v9.7.7-CHROME-STORE.zip
- SHA-256 supplied: `d61cf29f280be50192824e35ae93407c57a56ebd3da27e00747e1f21548cf23f`
- This hash has not been independently recomputed in this environment; verify locally before installing.
