# Telegram Deep Link Redirect Hack (for Remnawave Subscriptions)

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
