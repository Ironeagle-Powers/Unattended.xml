# Unattended.xml — Minimal Windows 11 Automated Setup

A clean, minimal unattended setup file for Windows 11 that automates only the essential setup tasks while leaving licensing, identity, and system integrity untouched.

---

## ⭐ Features

This answer file:

- Auto‑creates a **local Administrator account** (first real user with **RID 1000**)  
- Applies default **locale and keyboard settings** (en‑US)  
- Sets a **random computer name**  
- Skips non‑essential OOBE screens (EULA, registration, OEM screens)  
- Works with standard Windows install media without hacks or scripts  

> **Why RID 1000 matters:**  
> Creating the first real user at RID 1000 ensures Windows finalizes properly and behaves as a stable system without leftover provisioning or identity baggage.

---

## ❌ What This File Does NOT Do

- Bypass TPM, Secure Boot, or CPU compatibility checks  
- Modify activation, licensing, or product keys  
- Add scripts, registry hacks, or hidden tweaks  
- Carry sensitive information (passwords, keys, tokens)  

It uses **only documented Microsoft settings** for unattended setup.

---

## 🛠 Usage

1. Save this file as `Autounattend.xml`  
2. Place it in the root of a Windows 11 install USB  
3. Boot the target machine from the USB  
4. Windows Setup will automatically apply this file during install  

*Optional:* Works with WinPE environments and VHD/VHDX based recovery or portable installations.

---

## 📦 Compatibility

- Clean Windows 11 install media (21H2 and newer)  
- WinPE environments for scripted install  
- Deployment tools that support unattended files  
- No online connectivity required  

---

## 🧾 Background

Windows Setup reads unattend files in two primary phases:

- **specialize** — system identity and configuration  
- **oobeSystem** — user creation and OOBE screens  

This file only sets the required fields and leaves all other Windows behavior untouched.

---

## 📌 Short Description (for repo search)

> Minimal Windows 11 unattended setup — auto local admin (RID 1000), default locale, skip OOBE, safe and clean.
