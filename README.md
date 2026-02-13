

Automated Windows 11 deployment XML — quick setup, local account, language, predictable clean install

## ⭐ Overview
This repository provides a minimal, fully transparent Windows 11 unattend.xml designed to create a clean local administrator account and apply basic setup defaults without modifying licensing, activation, identity, or cloud behavior.
It exists for one purpose:
To give someone a clean, safe, identity‑neutral Windows experience — especially when wiping the hard drive isn’t enough.
If you inherited a computer from a family member, or you’re dealing with a machine that still “remembers” a previous owner’s Microsoft account, cloud identity, or Insider enrollment, this file helps you start fresh without hacks, bypasses, or tricks.

## ⭐ What This File Does
✔ Creates a single local administrator account
You edit one line (the username).
Windows creates that account during OOBE.
No passwords, no auto‑login, no hidden accounts.
✔ Sets basic language and locale defaults (en‑US)
A predictable, universal baseline.
✔ Assigns a random computer name
No branding, no reused names, no identity leakage.
✔ Hides a few cosmetic OOBE screens
EULA, OEM fluff, and similar non‑essential pages.
✔ Leaves Microsoft’s identity flow untouched
It does not:
• 	bypass Microsoft account
• 	force offline mode
• 	skip privacy screens
• 	alter cloud provisioning
• 	change activation or licensing
Everything else behaves exactly as Windows intended.

## ⭐ How It Works
Windows Setup reads unattend.xml during two phases:
1. Specialize Phase
• 	Computer name
• 	System defaults
• 	Regional settings
2. OOBE Phase
• 	Local account creation
• 	Language/keyboard setup
• 	Cosmetic screen suppression
There are:
• 	no scripts
• 	no registry edits
• 	no hacks
• 	no provisioning packages
• 	no modifications to Windows
This file uses only Microsoft‑supported configuration options documented in Windows Deployment.

## ⭐ Why This Exists
Because sometimes you can erase the hard drive, but you can’t erase the board.
When a computer is inherited — especially after a parent passes away — the motherboard may still be tied to:
• 	the previous owner’s Microsoft account
• 	cloud identity
• 	Insider enrollment
• 	provisioning flags
• 	OEM metadata
• 	hardware‑based entitlements
These do not live on the disk.
They live in firmware, NVRAM, TPM, and cloud metadata.
So even after a clean install, Windows may still try to be their computer.
This unattend.xml gives the new owner:
• 	a clean local account
• 	a clean OOBE
• 	no inherited identity
• 	no cloud baggage
• 	no leftover provisioning
• 	no surprises
It’s not a hack.
It’s not a bypass.
It’s not a trick.
It’s a reset of the relationship between Windows and the board, giving the user a clean, identity‑neutral baseline.

## ⭐ Licensing & Safety Transparency
This file is safe to redistribute because it contains:
• 	no product keys
• 	no activation data
• 	no Windows binaries
• 	no copyrighted content
• 	no identity information
It does not modify:
• 	licensing
• 	activation
• 	TPM
• 	firmware
• 	cloud identity
• 	hardware IDs
It simply automates a few setup steps.
Small test recommended — use at your own risk.
Try it in a VM or on a spare drive before using it on important hardware.

## ⭐ Who This Helps
This project is especially useful for:
• 	people inheriting a computer from a family member
• 	machines stuck in old Microsoft account bindings
• 	devices previously enrolled in Insider builds
• 	systems with cloud provisioning leftovers
• 	anyone wanting a clean, identity‑neutral baseline
• 	technicians doing clean installs for clients
• 	users with only one PC and no extra hardware
If you want Windows to install with a clean local admin account and no inherited identity, run it.
If you prefer to click through OOBE manually, don’t.
Simple as that.

## ⭐ In One Sentence
A minimal, transparent Windows 11 unattend.xml that creates a clean local admin account and resets the user experience without touching licensing, activation, or identity.
