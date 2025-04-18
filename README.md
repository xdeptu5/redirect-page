# Telegram Deep Link Redirect Hack ([for Remnawave Telegram Subscriptions Mini App](https://github.com/maposia/remnawave-telegram-sub-mini-app))

This project is a minimal HTML + JS redirector page that implements a **hack to work around Telegram Desktop on Windows not supporting certain external deep links** — such as `v2box://` or other custom protocols.

## 🧠 What is this?

Telegram Desktop on Windows doesn't properly open **external deep links** (like `v2box://`, `happ://`, `clash://...`, etc.) when they come from a browser or a message. This issue affects workflows such as activating subscriptions in services like **Remnawave**.

### ✅ The solution:
You **redirect the user first to this intermediate page**, and then the page **automatically redirects** them to the actual deep link using JavaScript.

This trick forces Windows to hand off the deep link to the appropriate app — bypassing Telegram’s default behavior.

---

## 🚀 How it works

1. A link (from Telegram, email, etc.) points to this redirect page with a `redirectTo` query parameter.
2. The page shows a message and a button that links to the real deep link.
3. After 5 seconds, the user is automatically redirected to the deep link.
4. If auto-redirect fails, the user can click the button manually.

---

## 🧾 Example

Since Telegram Desktop on Windows doesn’t support opening `v2box://` directly from mini app, instead you link the user to this page like so:
https://maposia.github.io/redirect-page/?redirect_to=v2box://install-sub?url=URL&name=Sub
The redirect page will handle it from there.

---

## 🌍 Features

- ✅ Language support (English & Russian)
- 🌓 Auto light/dark mode (based on system settings)
- ⏱ Optional 5-second delay before redirect
- 📦 Clean and customizable code

---

## 🔧 How to customize

You can adapt this page for your own project:

1. Modify the HTML/CSS as you like.
2. Host it anywhere — GitHub Pages, Vercel, your server, etc.

p.s. Special thanks to https://github.com/sm1ky for providing the hack
