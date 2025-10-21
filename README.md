# <p align="center">
  <img src="https://raw.githubusercontent.com/habanada/ByteBadger/refs/heads/main/bytebadger.jpg" 
       alt="ByteBadger Logo" width="300">
</p>   <em>ByteBadger – Bite by byte, from mess to bright.</em>

<p align="center">

</p>
 ByteBadger - Text Cleanup Tool

> **Tough on junk. Gentle on meaning.** 
> Bite by byte, from mess to bright.

ByteBadger is a **browser-based text cleanup and encoding repair tool**. 
It automatically detects and fixes **broken characters (Mojibake)**, 
removes invisible Unicode junk, normalizes symbols, trims excess spaces, 
and cleans up messy multilingual text - all **locally in your browser**, no data sent anywhere.

---

## 🚀 Features

- **Fix broken encodings (UTF-8 ↔ ANSI/Windows-125x)** 
 → Automatically repairs text corruption like `Ã¤`, `Ã¶`, `ÃŸ`, `ÐŸÑ€Ð¸Ð²ÐµÑ‚`, `Ã§`, etc. 
- **Supports multiple alphabets:** 
 German 🇩🇪, English 🇬🇧, French 🇫🇷, Turkish 🇹🇷, Russian 🇷🇺 and more. 
- **Removes or normalizes:**
 - Invisible Unicode (zero-width, NBSP, BOM, etc.)
 - Typographic quotes, dashes, bullets
 - Math letters (𝑥, 𝑦 → x, y)
 - Extra or non-breaking spaces
 - Emojis (with selective filtering)
- **Automatic language detection** powered by [franc](https://github.com/wooorm/franc)
- **Live preview, copy, and statistics display**
- **Works fully offline** (pure HTML + JavaScript)
- **Dark mode optimized**

---

## 🧠 How It Works

ByteBadger simulates real-world encoding mixups using `TextEncoder` and `TextDecoder`
for multiple character sets (`windows-1252`, `windows-1251`, `windows-1254`, `iso-8859-1`)
to build a **dynamic Mojibake mapping table**.

That allows it to reverse-engineer corrupted text sequences like:

| Corrupted | Fixed |
|------------|--------|
| `Ã¤` | `ä` |
| `Ã§` | `ç` |
| `ÃŸ` | `ß` |
| `ÐŸÑ€Ð¸Ð²ÐµÑ‚` | `Привет` |
| `Ã¶` | `ö` |

Everything runs inside your browser - no server calls, no tracking.

---

## 🧩 Usage

1. Open **[`ByteBadger.html`](./ByteBadger.html)** in your browser. 
2. Paste any messy or corrupted text into the input area. 
3. Choose your cleanup options:
 - ✅ Fix encoding
 - ✅ Replace special characters
 - ✅ Remove Unicode / emojis
 - ✅ Normalize math or technical symbols
4. Click **"Clean Text"**.
5. Copy your polished result.

---

## 📸 UI Overview

| Feature | Description |
|----------|--------------|
| 🧹 **Clean Text** | Runs full cleanup process |
| 📋 **Copy** | Copies cleaned output |
| 🗑 **Clear** | Resets both text fields |
| 🧪 **Demo** | Inserts a multilingual corrupted sample for testing |
| 🧠 **Language Mode** | Auto / Manual / Disabled |
| 🐍 **Encoding Fix** | Corrects Mojibake automatically |

---

## 🧱 Technology Stack

- **Pure JavaScript / HTML / CSS**
- **No frameworks or build tools**
- **Language detection:** [franc (MIT License)](https://github.com/wooorm/franc)
- **Encoding repair:** dynamic multi-decoder map
- **Storage:** uses `localStorage` for settings persistence

---

## 🔒 License

**Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** 
© 2025 [Selahattin Erkoc](https://github.com/habanada)

You may use, share, and modify ByteBadger for **non-commercial purposes only**. 
Commercial use requires explicit permission from the author.

Includes the *franc* language detection library by Titus Wormer (MIT License). 
[https://creativecommons.org/licenses/by-nc/4.0/](https://creativecommons.org/licenses/by-nc/4.0/)

---

## 🏷 Recommended GitHub Tags

