# 🛡️ PhrasePass - Mnemonic Password Generator

[![Netlify Status](https://api.netlify.com/api/v1/badges/b4382586-7e30-4e56-9a25-835695843734/deploy-status)](https://app.netlify.com/sites/phrasepass/deploys)
![Version](https://img.shields.io/badge/version-2.1-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

> **"Security that humans can actually remember."**

**PhrasePass** is a web-based tool designed to solve a common IT problem: employees need strong passwords, but standard generators produce impossible-to-remember strings (like `Xj9#m2!L`). This leads to people writing passwords on sticky notes, which defeats the purpose.

**PhrasePass** takes a memorable English phrase (mnemonic) and algorithmically converts it into a cryptographically strong, 10-character password that meets strict corporate policy requirements.

---

## 🔗 Live Demo
🚀 **Try it here:** [https://phrasepass.netlify.app/](https://phrasepass.netlify.app/)

---

## 💡 Why PhrasePass?

I built this tool to assist my department employees. When opening new user accounts, we needed passwords that were:
1.  **Secure:** Contain Uppercase, Lowercase, Numbers, and Symbols.
2.  **Compliant:** Meet standard length and complexity policies.
3.  **Human-Friendly:** Easy for the user to type and remember immediately.

Standard generators prioritize entropy over usability. **PhrasePass balances both.**

---

## 🚀 Features

* **Smart Transformation:** Converts phrases like `my dog name is bonzo` into complex strings.
* **Policy Compliance:** Guarantees 10 characters, including `[A-Z]`, `[a-z]`, `[0-9]`, and symbols (`!@#$-`).
* **Security Filters:**
    * **Blocklist:** Prevents weak phrases (e.g., "password", "123456").
    * **Anti-Repetition:** Rejects results with triple characters (e.g., "aaa") or predictable sequences.
* **Privacy First:** Client-side only. No data is sent to any server; everything happens in your browser.
* **Hebrew UI:** Designed for Israeli users with a clean, Right-to-Left (RTL) interface.
* **Session History:** Remembers the last 10 generated passwords locally for quick workflow.

---

## 🛠️ The Logic (How it works)

1.  **Sanitization:** Input is cleaned of spaces and converted to lowercase.
2.  **Normalization:** The string is padded or trimmed to a base length using a secure character set.
3.  **Injection:** The algorithm randomly injects:
    * A symbol (`!`, `@`, `#`, `$`, `-`) at a random position.
    * A digit (0-9) at a random position.
    * Uppercase transformation for random letters.
4.  **Validation Loop:** It attempts up to 100 variations until it finds one that passes all security checks (no triple chars, valid length, includes all types).

---

## 💻 Installation (Local)

Since PhrasePass is a static web application, you don't need `npm` or a build server.

1.  Clone the repository:
    ```bash
    git clone [https://github.com/Chagai33/PhrasePass.git](https://github.com/Chagai33/PhrasePass.git)
    ```
2.  Navigate to the folder:
    ```bash
    cd PhrasePass
    ```
3.  Open `index.html` in any web browser.

---

## 📸 Screenshot

*(Place a screenshot of your app here. Example: `![App Screenshot](./screenshot.png)`)*

---

## 👤 Author

**Chagai Yechiel**
* **GitHub:** [@Chagai33](https://github.com/Chagai33)
* **LinkedIn:** [Chagai Yechiel](https://www.linkedin.com/in/chagai-yechiel/)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
