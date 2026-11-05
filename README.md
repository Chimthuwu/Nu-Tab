# 🪐Nu Tab

A sleek, fully customizable, Bento-style dashboard for your browser. Built with vanilla HTML, CSS, and JavaScript, this new tab page replaces your default homepage with a beautiful, functional workspace.

![Aesthetic New Tab Preview](https://nu-tab.pages.dev/preview.png)

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

## 🚀 How to Use

1. Visit **[nu-tab.pages.dev](https://nu-tab.pages.dev/)** to see it live.
2. **To make it your homepage:**
   - **Chrome/Edge:** Go to Settings > On Startup > Open a specific page > Add `https://nu-tab.pages.dev/`.
   - **Firefox:** Go to Settings > Home > Homepage and set it to `https://nu-tab.pages.dev/`.
   - **Extensions:** Alternatively, use extensions like *New Tab Override* to redirect your new tab page to this URL.

---

## 🛠️ How to Deploy Your Own

Because this is a static site (just a single HTML file), hosting is completely free and takes seconds.

### Cloudflare Pages (Recommended)
1. Fork this repository or download the files.
2. Go to [Cloudflare Dashboard](https://dash.cloudflare.com/) > Workers & Pages > Create Application > Pages.
3. Choose **Connect to Git** (and select your repo) or **Upload assets** (drag and drop the `index.html` and `preview.png`).
4. Deploy! You will get a free `*.pages.dev` URL.

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
