Install

Chrome Web Store: (listing link will be added here after approval)

From source (developer mode):

Download or clone this repository.
Open chrome://extensions and switch on Developer mode.
Click Load unpacked and select the extension/ folder.
Open any website and click the extension icon.
Permissions explained
Permission	Why it is needed
activeTab	Lets the extension run its audit on the tab you are looking at, only when you click the icon
scripting	Injects the bundled analyzer into that tab
storage	Saves your last scores per site on your device (chrome.storage.local)

No host permissions are requested and no data is sent to any server.

Privacy Policy

Effective date: 11 October 2026

AI Search Readiness is a Chrome extension that audits the web page you are viewing. This policy explains what it does with data. The short version: it collects nothing and sends nothing anywhere.

What the extension does not do
It does not collect, transmit, sell or share any personal data or browsing data.
It does not use analytics, telemetry, advertising or tracking of any kind.
It does not have accounts, logins or a backend server.
It does not load or run remote code. All code ships inside the extension package.
It does not use cookies.
What happens when you click the icon
The extension runs its audit only on the tab you are viewing, and only after you click its icon (permission: activeTab).
It reads that page's content in your browser and makes requests to the same website you are viewing (its /robots.txt, /llms.txt and the page's own HTML, without cookies) to check how the site is set up for AI crawlers.
The score and recommendations are computed locally and shown in the popup. The results are not sent to the developer or to any third party.
What is stored on your device

The extension saves a short audit history in your browser using chrome.storage.local: for each website you audit, up to the last 20 entries containing the page URL, the score and a timestamp. This is used only to show "change since your last audit". It stays on your device, is not synced and is not accessible to the developer. You can remove it at any time by removing the extension or clearing the extension's data in chrome://extensions.

Clipboard

The "Copy" buttons write the report or draft code you asked for to your clipboard when you click them. The extension never reads your clipboard.

Third parties

None. The extension does not communicate with any third-party service.

Children

The extension is a professional web tool and is not directed at children. It collects no data from anyone.

Changes to this policy

If this policy changes, the updated version will be published on this page with a new effective date. Any future feature that handles data would be disclosed here and in the Chrome Web Store listing before release.

Contact

Questions or concerns: open an issue in this repository's Issues tab.

Support

Found a bug or have an idea? Open an issue in this repository's Issues tab.

Development
bash
npm install        # installs Playwright (dev only)
npx playwright install chromium
npm test           # runs the analyzer in real Chromium against local sample sites
npm run assets     # regenerates the Chrome Web Store screenshots in store-assets/
extension/        the extension (this folder is what gets uploaded to the Web Store)
test/             Playwright test runner + sample pages
tools/            store image generator
store-assets/     Chrome Web Store screenshots, promo tiles, icon
docs/             publishing checklist, store listing text, README images

Pull requests are welcome. Please keep the extension dependency-free and local-only: no remote code, no analytics.

Disclaimer

This project is independent and is not affiliated with, endorsed by or sponsored by OpenAI, Anthropic, Google, Perplexity, Microsoft or any other company mentioned. ChatGPT, Claude, Gemini, Perplexity and other names are trademarks of their respective owners and are used only to describe compatibility.

License

MIT
