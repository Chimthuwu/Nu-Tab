# 🪐 Nu Tab

A sleek, fully customizable, Bento-style dashboard for your browser. Built with vanilla HTML, CSS, and JavaScript, Nu Tab replaces your default homepage with a beautiful, functional workspace.

![Nu Tab Preview](https://nu-tab.pages.dev/preview.png)

---

## 🔥 How to set as your New Tab

The easiest way to use Nu Tab is to visit the live URL: **[nu-tab.pages.dev](https://nu-tab.pages.dev/)**

To make it open automatically when you open a new tab, use one of the methods below:

### Method 1: Browser Settings (Homepage)
If you just want it to open when you click the "Home" button or launch your browser:
- **Chrome / Edge / Brave:** Go to `Settings` > `On startup` > Select **Open a specific page or set of pages** > Click **Add a new page** and paste `https://nu-tab.pages.dev/`.
- **Firefox:** Go to `Settings` > `Home` > Under **Homepage and new windows**, select **Custom URLs** and paste the link.
- **Safari:** Go to `Safari` > `Preferences` > `General` > Set **Homepage** to the URL.

### Method 2: New Tab Override Extensions (Recommended)
Browsers often lock the *actual* New Tab page (the one you get when you click the `+` button). To force Nu Tab to open there, you need a tiny, free extension.
- **Chrome / Edge:** Install an extension like **New Tab Redirect** or **New Tab Override** from the Chrome Web Store, and set the redirect URL to `https://nu-tab.pages.dev/`.
- **Firefox:** Install **New Tab Override** from Firefox Add-ons. It allows you to set a custom URL for the new tab page directly in its settings.

---

## ✨ Features

- **⚙️ No-Code Settings:** Click the gear icon in the top right to customize your dashboard without touching a single line of code.
- **🕒 Local Clock & Weather:** Automatically detects your local time. Just type your city in the settings, and it automatically geocodes your location to fetch real-time conditions, temperature, wind, and humidity.
- **🔍 Smart Search:** A beautiful search bar that lets you switch between search engines (Qwant, Google, Bing, DuckDuckGo, Ecosia) on the fly.
- **⚡ Slash Commands:** Type `/` in the search bar to instantly open a command menu. Search YouTube (`/yt`), GitHub (`/gh`), ask AI models (`/gpt`, `/claude`), or translate with DeepL (`/deepl`).
- **👀 Stealth Model Tracker:** A built-in widget that automatically checks for new "stealth" AI models on OpenRouter and OpenCode. It pings a live API and highlights updates with a lime-green dot.
- **🖤 BlankScreen Mode:** Click the black square next to the search bar to instantly turn your screen into a pure black, distraction-free void. Double-click anywhere to exit.
- **💾 Saved Locally:** All your settings and custom links are saved to your browser's `localStorage`. No account needed, and your layout stays exactly how you left it.

---

## 🎨 Customization

While the **Settings Gear** handles all your daily changes (City, Link Names, Link URLs), you can dig into the code to change the default behavior for anyone who uses your fork.

Open `index.html` and find the `DEFAULT_CONFIG` block at the top of the `<script>` tag:

```javascript
const DEFAULT_CONFIG = {
  location: {
    city: "Sydney, Australia",
    lat: "-33.8688",
    lon: "151.2093"
  },
  links: {
    gmail: { name: "Gmail", url: "https://mail.google.com/" },
    // ...
