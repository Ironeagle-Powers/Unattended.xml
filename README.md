# Unattended.xml  
A clean, safe, and transparent Windows setup automation file.

---
**Compatibility**  
This template has been tested and works with both **Windows 10** and **Windows 11** installations.
---

This project provides a minimal `unattend.xml` that automates the out‑of‑box experience (OOBE) on a **fresh, legitimate Windows installation**.  
It does **not** bypass licensing, activation, identity, or security. It simply removes repetitive setup steps so you can get to a usable desktop faster.

---

## ⭐ What This File Does
- Skips the interactive OOBE screens  
- Creates a **local administrator account** you can rename or edit  
- Applies a few basic, non‑controversial defaults  
- Lets you finish setup without internet  
- Keeps everything transparent and editable

Nothing is hidden. Nothing is obfuscated. Everything is inside one XML file you can read yourself.

---

## ⭐ What This File Does *Not* Do
- It does **not** activate Windows  
- It does **not** bypass Microsoft account requirements in unsupported ways  
- It does **not** modify licensing, security, BitLocker, or identity  
- It does **not** install software, drivers, or scripts  
- It does **not** touch anything outside the normal Windows setup process

This is a **safe, compliant, beginner‑friendly** automation file — not a hack, not a workaround, not a tool for modifying system internals.

---

## 📁 How to Use It
1. Download `unattend.xml` from this repository  
2. Place it in:  
   `USB:\sources\unattend.xml`  
3. Boot from your Windows installation media  
4. Install Windows normally — the file handles the setup screens  
5. Log in with the local account defined in the file

You can edit the username, password, or settings using any text editor.

---

## 🛠 Editing the File
You can safely change:
- Username  
- Password  
- Computer name  
- Region / language  
- Time zone  

See the **Wiki** for detailed explanations of every section:
https://github.com/Ironeagle-Powers/Unattended.xml/wiki

---

## ❓ FAQ
**Does this activate Windows?**  
No — you still need a valid license.

**Is this safe?**  
Yes. It uses only documented Windows setup components. No scripts, no binaries, no modifications.

**Can I customize it?**  
Absolutely. The file is intentionally minimal so you can build on it.

---

## 🧭 Philosophy
This project exists for one reason:  
**to give people a clean, honest, transparent starting point for Windows automation.**

Most unattended files online are:
- bloated  
- outdated  
- unsafe  
- or full of questionable tweaks  

This one is intentionally simple.  
You can run it as‑is or use it as a foundation for your own deployments.

---

## 📚 Documentation
The full documentation lives in the Wiki:  
- How It Works  
- What Each Section Does  
- Troubleshooting  
- Philosophy  
- Use Cases  
- Advanced Notes  

https://github.com/Ironeagle-Powers/Unattended.xml/wiki

---

## ✔ License
MIT License — do whatever you want with it.  
Just be responsible and test before deploying.
