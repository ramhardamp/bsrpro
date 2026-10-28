Privacy Policy — BABASITARAM PRO
Last updated: October 2026
Applies to:
•	BABASITARAM PRO — Ultimate Privacy Shield (v9.2.4)
•	BABASITARAM PRO Password Manager (v5.43.8)
•	BABASITARAM PRO Android App (APK)
•	BABASITARAM PRO — Location Guard BSRPRO browser extension (v1.2.2)
Developer: VIKRAM SINGH RAJPUT

🔒 Our Commitment
BABASITARAM PRO does not operate any backend server, and the developer does not collect, receive, or have access to any of your data.
All settings, preferences, and statistics are stored locally on your device using the browser's built-in storage APIs (chrome.storage.local). This data never leaves your device unless you explicitly export it yourself.
We do not collect:
•	❌ Personal information (name, email, address, etc.)
•	❌ Browsing history
•	❌ Usage statistics
•	❌ Analytics or telemetry
•	❌ Cookies or credentials
•	❌ Health, financial, or authentication data
•	❌ Your real location or GPS data (the Location Guard BSRPRO extension never reads or stores it)
No account is required. No tracking. No ads. 100% private.

📍 About Location Guard BSRPRO
Location Guard BSRPRO lets you choose a location and reports that location to websites instead of your device's real location.
•	The extension never reads, stores, or sends your real location.
•	Only the location you choose yourself is saved, and it is saved only on your device.
•	It changes only the browser's location feature (Geolocation API). It does not hide your IP address, so a website that estimates location from your IP can still see your general area.
•	It does not run on browser-internal pages.

📌 What Data Is Stored, And Where
The following data is stored locally on your device using chrome.storage.local:
Ultimate Privacy Shield and Password Manager
Data Type	Purpose
Settings & Preferences	To remember your chosen configuration (ad blocker, HTTPS, etc.)
Whitelist / Fireproof Sites	To protect specific sites from cleaning
Vault Sites	To password-protect sensitive sites
PIN (hashed)	To unlock the Vault — stored locally, never transmitted
Custom Block Rules	To remember element picker and CSS rules
Time Limits	To track daily time spent per domain
Activity Logs	To show recent activity in the popup
Statistics	To display ads blocked, trackers blocked, etc.
Location Guard BSRPRO
Data Type	Purpose
ON / OFF switch	To remember whether spoofing is active
Chosen latitude and longitude	The location you picked, reported to websites when the switch is ON
Accuracy value	The accuracy (in metres) you selected
Place name	To show the name of your chosen place in the popup
This data never leaves your device unless you explicitly use the Export Backup feature (Settings → Export Backup). Even then, the exported file is saved on your own device and is not transmitted to us. Removing an extension, or clearing its storage, deletes the data it saved.

☁️ Browser Sync (Optional)
If you enable the extension's "Cloud Sync" option:
•	A small subset of your settings is stored using chrome.storage.sync
•	This is operated by your browser vendor (Mozilla, Microsoft, or Google), not by us
•	This only runs if you turn it on
•	It only syncs between your own signed-in devices
Location Guard BSRPRO does not use browser sync. Its data stays only in local storage.

🌐 Network Requests These Extensions Make
1. Filter List Updates (Automatic)
The Ultimate Privacy Shield periodically downloads publicly published ad/tracker block-lists:
•	EasyList (https://easylist.to/)
•	EasyPrivacy (https://easylist.to/)
•	uBlock Origin's Annoyances list (https://ublockorigin.com/)
These are plain list downloads from their official hosts. No information about you or your browsing is sent.
2. Breach Alert (Optional, User-Initiated)
If you use the "Breach Alert" feature:
•	The email address you type is sent directly to haveibeenpwned.com's public API
•	This only happens when you press "Check"
•	Only the email address you enter is sent — nothing else
•	Never to us — we don't have any servers
•	You must provide your own free HIBP API key (available at haveibeenpwned.com/API/Key)
3. DNS-over-HTTPS (Optional)
If you enable a DoH provider in Settings:
•	Your browser's DNS resolution is routed through the provider you choose (e.g., Cloudflare, Google, Quad9)
•	This uses your browser's native DoH support
•	We do not proxy or see this traffic
4. Map and Place Search (Location Guard BSRPRO only)
The Location Guard BSRPRO popup shows a map and lets you search for a place. This happens only when you open the popup and use the map or search:
•	Map tiles are loaded from tile.openstreetmap.org. If it is unavailable, the map automatically falls back to basemaps.cartocdn.com (CARTO) or server.arcgisonline.com (Esri). These requests contain the map area being shown.
•	Place search and place-name lookup use nominatim.openstreetmap.org. These requests contain the text you typed, or the coordinates you chose to fix.
•	Like any website, these services also receive standard technical data such as your IP address and browser details.
•	These services are run by the OpenStreetMap Foundation, CARTO, and Esri, and are covered by their own privacy policies.
•	Never to us — nothing is sent to the developer, and your real location is never part of these requests.

🔑 Permissions Explained
Ultimate Privacy Shield and Password Manager
Permission	Why It's Needed
storage	To save your settings/lists locally
tabs	To know the current tab's URL for per-site features
cookies, browsingData, history	Used only for Cookie Cleaner, Emergency Burn, and Fireproof features — all local, user-initiated
declarativeNetRequest	To block ads/trackers at the network layer
webNavigation	To detect page navigation for site-specific features
idle	To trigger auto-cleanup when the browser is idle
alarms	To schedule periodic filter list updates and nightly cleanup
contextMenus	To add right-click menu items ("Block this site", "Pick element")
host_permissions (<all_urls>)	Required so ad-blocking, site-lock, and element picker can run on any site you visit
Location Guard BSRPRO
Permission / Access	Why It's Needed
storage	To save your chosen location and the ON/OFF switch on your device
Content script on all websites (<all_urls> match)	Any website can ask for your location, so the extension must be present on every page, before the page's own scripts run, to answer with your chosen location. It handles only location requests. It does not read, copy, or send page content, forms, cookies, or passwords.
Content script in the page context (MAIN world)	The browser's location feature lives in the page's own context, so the override must run there. It has no access to extension APIs.
Location Guard BSRPRO does not request tabs, activeTab, scripting, cookies, history, or any other permission.
All permissions are used exclusively for local functionality. No data is transmitted to the developer or to any server operated by the developer.

🔗 Third Parties
We do not sell, rent, or share any data, because we never receive any.
The only third parties your browser ever talks to as a direct result of using these extensions are:
Service	Purpose	When It Runs
EasyList / EasyPrivacy	Filter list downloads	Automatically (periodic)
uBlock Origin Annoyances	Filter list downloads	Automatically (periodic)
haveibeenpwned.com	Breach Alert (optional)	Only when you press "Check"
OpenStreetMap (tiles and Nominatim)	Map and place search in Location Guard BSRPRO	Only when you open its popup and use the map or search
CARTO / Esri	Fallback map tiles in Location Guard BSRPRO	Only if OpenStreetMap tiles cannot be loaded

✅ Limited Use Disclosure
The use of information received by BABASITARAM PRO extensions, including any information obtained through browser APIs, adheres to the Chrome Web Store User Data Policy, including the Limited Use requirements. Information is used only to provide the user-facing features described above. It is not transferred to others, not used for advertising, and not read by humans.

🧒 Children's Privacy
These extensions do not knowingly collect any personal information from children under 13. They are designed for general use and do not target children.

📝 Changes to This Policy
If this policy changes, the updated version will be included with the next extension update and posted to:
https://github.com/ramhardamp/babasitaram-pro
The "Last updated" date at the top of this page will also be revised.

📬 Contact
Questions about this policy:
📧 babasitarampro@gmail.com
Developer: VIKRAM SINGH RAJPUT GitHub: https://github.com/ramhardamp/babasitaram-pro Website: https://ramhardamp.github.io/bsrpro/

✅ Summary
Question	Answer
Do you collect my data?	❌ No
Do you store my data on your servers?	❌ No
Do you sell my data?	❌ No
Do you share my data?	❌ No
Do you use analytics or telemetry?	❌ No
Is my data stored locally?	✅ Yes
Can I export my data?	✅ Yes (Settings → Export Backup)
Can I delete my data?	✅ Yes (uninstall the extension)
Is my PIN transmitted anywhere?	❌ Never
Is my browsing history sent anywhere?	❌ Never
Does Breach Alert send data to you?	❌ No — it goes directly to HIBP
Does Location Guard BSRPRO read my real location?	❌ Never
Does Location Guard BSRPRO send anything to you?	❌ No — map and search requests go directly to OpenStreetMap, CARTO, or Esri
Does Location Guard BSRPRO hide my IP address?	❌ No — it changes only the browser's location feature

BABASITARAM PRO is, and always will be, 100% free. No paywalls, no locked features, no telemetry, no tracking. Your privacy is the product — not you.
