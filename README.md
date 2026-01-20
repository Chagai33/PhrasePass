# 🛡️ PhrasePass - Mnemonic Password Generator

![Version](https://img.shields.io/badge/version-2.1-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Language](https://img.shields.io/badge/language-Hebrew-orange)

**PhrasePass** is a client-side web application designed to solve the dilemma of creating complex passwords that are easy to remember. It converts simple, memorable English phrases (mnemonics) into strong, secure, and complex 10-character passwords.

The interface is designed in **Hebrew** with a mobile-first approach, ensuring accessibility for RTL users.

---

## 🚀 Features

* **Mnemonic Logic:** Transforms phrases like `my dog name is bonzo` into cryptographically strong passwords.
* **Smart Complexity:** Automatically injects uppercase letters, numbers, and symbols (`!@#$-`) into the base phrase.
* **Security Validation:**
    * **Blocklist:** Prevents usage of common weak phrases (e.g., "password", "123456").
    * **Pattern Detection:** Rejects passwords with repeating characters (e.g., "aaa") or predictable sequences.
* **Client-Side Only:** All processing happens locally in the browser. No data is ever sent to a server.
* **Session History:** Keeps track of the last 10 generated passwords for quick retrieval.
* **User Experience:**
    * One-click "Copy to Clipboard".
    * Responsive design (Mobile/Desktop).
    * Clear history management.

---

## 🛠️ How It Works (The Algorithm)

1.  **Input Sanitization:** The user enters a phrase. Spaces are removed, and text is converted to lowercase.
2.  **Length Normalization:** The base string is trimmed or padded (using a varied character set) to ensure a consistent base length.
3.  **Injection:**
    * A random **symbol** (`!`, `@`, `#`, `$`, `-`) is inserted at a random position.
    * A random **digit** (0-9) is inserted at a random position.
    * A random letter is converted to **Uppercase**.
4.  **Validation Loop:** The generator attempts up to 100 variations until the result passes strict criteria:
    * Exactly 10 characters long.
    * Contains [A-Z], [a-z], [0-9], and a symbol.
    * No triple repetitive characters.

---

## 💻 Installation & Usage

Since this is a lightweight, static web application, no build process or package manager is required.

### Option 1: Run Locally
1.  Clone the repository:
    ```bash
    git clone [https://github.com/your-username/phrase-pass.git](https://github.com/your-username/phrase-pass.git)
    ```
2.  Navigate to the project folder.
3.  Open `index.html` in any modern web browser.

### Option 2: Deploy
You can deploy this file directly to **GitHub Pages**, **Netlify**, or **Vercel** simply by uploading the `index.html` file.

---

## 🎨 Tech Stack

* **HTML5** - Semantic structure.
* **CSS3** - Flexbox layout, responsive design, and system-ui fonts.
* **JavaScript (ES6+)** - DOM manipulation and generation logic.

---

## 📸 Screenshots

*(Add a screenshot of your app here if possible)*

| Desktop View | Mobile View |
|:---:|:---:|
| ![Desktop](https://via.placeholder.com/400x300?text=Desktop+UI) | ![Mobile](https://via.placeholder.com/200x350?text=Mobile+UI) |

---

## 👤 Author

**Chagai Yechiel**

* **Version:** 2.1

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
