# Unattended.xml — Minimal Windows 11 Automated Deployment

A **deterministic, minimal unattended setup** for Windows 11 that orchestrates essential configuration while preserving **system integrity, provisioning fidelity, and identity hygiene**.  

This is intended for deployment engineers, IT technicians, or power users who require a **reproducible golden image setup** without injecting external dependencies or breaking baseline compliance.

---

## ⭐ Features

- Auto‑creates a **local Administrator account (RID 1000)** to ensure proper **SID alignment** and **security context initialization**  
- Configures default **locale, input method, and system locale** (en-US)  
- Assigns a **randomized machine identity** for post-deployment uniqueness  
- Skips non‑essential OOBE screens (EULA, OEM registration, online accounts)  
- Compatible with **WinPE** environments, VHD/VHDX boot, and **bare-metal provisioning**  
- Maintains **non-destructive deployment**: licensing, activation, and system binaries remain untouched  

> **Why RID 1000 matters:**  
> Creating the first user at RID 1000 ensures **baseline user namespace alignment** and prevents Windows from inheriting **residual provisioning artifacts** from temporary or pre-deployment accounts.

---

## ❌ Limitations / Scope

- Does not bypass TPM, Secure Boot, or CPU attestation checks  
- Does not alter **activation, licensing, or product keys**  
- Does not run scripts, registry hacks, or undocumented tweaks  
- No sensitive data is stored (passwords, keys, tokens)  

This file adheres strictly to **Microsoft documented unattended deployment schemas**.

---

## 🛠 Deployment / Usage

1. Save this file as `Autounattend.xml`  
2. Place it in the root of a Windows 11 install USB  
3. Boot target hardware from USB  
4. Windows Setup consumes this file during the **specialize** and **oobeSystem** passes, executing deterministic configuration automation  

*Optional:* Works in VHD/VHDX recovery scenarios or **disconnected deployment chains**.

---

## 📦 Compatibility

- Clean Windows 11 installation media (21H2 and newer)  
- WinPE environments for scripted or headless installation  
- Supports **dynamic provisioning, hardware abstraction**, and bare-metal deployment  
- Offline or online deployment workflows  

---

## 🧾 Technical Background

Windows Setup processes unattended files in **phased configuration passes**:

- **specialize** — initializes system identity, applies locale, and prepares hardware profile  
- **oobeSystem** — creates the first local user, applies OOBE settings, and finalizes provisioning  

This file only populates fields essential for a **predictable, compliant installation**, leaving all other behavior in its **pristine default state**.

---

## 📌 Search-Friendly Keywords

> Windows 11 unattended deployment, automated provisioning, RID 1000, SID alignment, OOBE skip, VHD/VHDX boot, WinPE integration, deterministic image, IT deployment, system integrity

### Works Fully Online
This answer file is designed to be safe while connected to the internet during installation.  
Because it bypasses OOBE without creating accounts or modifying identity, Windows never enters the cloud‑identity pipeline.  
You can stay online the entire time — Windows Update will run normally, and the install will remain clean, neutral, and retail‑aligned.
