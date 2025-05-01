## 📦 Remote Config Editor

This package contains a simple HTML tool to **edit external text content** for your mobile app (built with React Native or Expo).

### 🔧 Contents

- `index.html` – A clean, RTL-friendly UI to edit configuration values and generate a JSON file.
- `app-config.json` – A sample config file containing keys like `welcome_message`, `about_text`, and `contact_text`.
- `README.txt` – This documentation file you're reading.

---

## 🎯 Purpose

This tool lets you:

- Maintain **dynamic text** in your app (welcome messages, about sections, contact info, etc.)
- Update the content **without needing to release a new app version**
- Host and fetch the content via **GitHub Pages** or any static file host

---

## 🚀 How to Use

### 1. Open the Editor

Open the `index.html` file in any modern browser. You’ll see editable fields for:

- Welcome message
- About text
- Contact info

Click **"Generate JSON"**, and the output will appear below in a formatted JSON block.

---

### 2. Copy and Save the Output

Copy the generated JSON and **replace the contents of `app-config.json`** with it.

> ✅ Tip: You can also save this JSON directly using your own workflow or automation.

---

### 3. Upload to GitHub Pages

To make the config accessible by your app:

1. Create a public GitHub repository (e.g., `app-config`)
2. Commit the updated `app-config.json`
3. Go to `Settings → Pages`, and enable GitHub Pages with:
   - Branch: `main`
   - Folder: `/ (root)`
4. After saving, GitHub will provide a public URL:
   ```
   https://<your-username>.github.io/app-config/app-config.json
   ```

---

### 4. Load in Your App

In your React Native / Expo app, fetch this file once and use its content via context:

```ts
fetch('https://<your-username>.github.io/app-config/app-config.json')
  .then(res => res.json())
  .then(setConfig);
```

Use it inside a global context like `RemoteConfigProvider` for best architecture.

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

