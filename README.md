# Arabic Number Converter

A lightweight, single-file web app that converts Western (English) numerals into Eastern Arabic numerals in real time — with a bilingual (English/Arabic) interface, live Gregorian and Hijri date cards, dark/light themes, and conversion history.

**[Live Demo](#) · [Report a Bug](#) · [Request a Feature](#)**

---

## ✨ Features

- **Real-time conversion** — English digits (`0-9`) convert instantly to Eastern Arabic numerals (`٠-٩`) as you type
- **Bilingual UI** — one-click toggle between English (LTR) and Arabic (RTL) interfaces, with full layout direction switching
- **Dark / light mode** — theme preference is saved locally and persists across visits
- **Gregorian & Hijri date cards** — displays today's date in both calendars, each showing the numeral and its Arabic-numeral equivalent side by side
- **Copy to clipboard** — one-click copy with a clipboard API fallback for older browsers
- **Conversion history** — keeps your last 5 unique conversions for quick reference
- **Keyboard shortcut** — `Ctrl + K` clears the input instantly
- **Responsive design** — adapts cleanly from mobile to desktop
- **Ad-ready** — pre-wired Google AdSense placements (banner, square, in-feed, footer)

---

## 🖥️ Tech Stack

- **HTML5** — semantic, accessible markup
- **Tailwind CSS** (via CDN) — utility-first styling
- **Vanilla JavaScript** — no frameworks, no build step
- **Intl API** — native `Intl.DateTimeFormat` for Hijri (Umm al-Qura) and Gregorian date calculations, with a manual fallback algorithm if the browser lacks Islamic calendar support
- **Google Fonts** — Playpen Sans Arabic

---

## 📦 Getting Started

This is a static, dependency-free project — no build tools or package manager required.

1. Clone or download the repository
   ```bash
   git clone <repository-url>
   cd arabic-number-converter
   ```
2. Open `index.html` directly in a browser, or serve it locally:
   ```bash
   npx serve .
   ```
3. That's it — the app runs entirely client-side.

---

## ⚙️ Configuration


### Adding a Language

Translations live in a single `T` object in the script:

```js
const T = {
  en: { ... },
  ar: { ... },
};
```

Add a new locale key with the same set of fields, then extend `updateLanguage()` to handle it.

---

## 📁 Project Structure

```
.
└── index.html   # Entire app: markup, styles, and logic in one file
```

---

## 🌐 Browser Support

Requires a modern browser with support for:
- `Intl.DateTimeFormat` with the `islamic-umalqura` calendar (for native Hijri dates — a manual fallback covers browsers without it)
- `navigator.clipboard` (with a `document.execCommand` fallback for older browsers)
- CSS `backdrop-filter`

Tested on the latest versions of Chrome, Firefox, Safari, and Edge.

---

## 🤝 Contributing

Contributions are welcome. Please open an issue to discuss significant changes before submitting a pull request.

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes
4. Open a pull request

---

## 📄 License

This project is available for use under the MIT License. See `LICENSE` for details.