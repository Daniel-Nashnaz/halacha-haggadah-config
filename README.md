## 📦 Remote Config Editor

This package contains a simple tool to **edit external text content** for your mobile app (built with React Native or Expo).

### 🔧 Contents

- `app-config.json` – A sample config file containing keys like `welcome_message`, `about_text`, and `contact_text`.

---

## 🎯 Purpose

This tool lets you:

- Maintain **dynamic text** in your app (welcome messages, about sections, contact info, etc.)
- Update the content **without needing to release a new app version**
- Host and fetch the content via **GitHub Pages** or any static file host

---

## 💡 Benefits

- 🔄 Live text updates without rebuilding the app
- ✅ No Firebase, no backend required
- 🧠 Easy to maintain, even by non-developers
- 💵 Completely free using GitHub Pages

---

## 📌 Notes

- The GitHub repository must be **public** for your app to access the config via `fetch`.
- For private data or API keys, do **not** use this method.
- Optional: you can extend the HTML editor to support more fields or auto-save.

