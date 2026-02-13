Unattended.xml — Minimal Windows 11 Automated Deployment

A minimal, deterministic unattended configuration for Windows 11.

This answer file automates only the essential setup phases required for a clean, reproducible installation. It avoids registry hacks, activation bypasses, hardware requirement modifications, or undocumented behavior.

Designed for deployment engineers, IT technicians, and power users who want a predictable baseline installation without altering Windows’ default compliance model.

Features

Creates the first persistent local Administrator account (RID 1000)

Sets system locale, input method, and UI language (en-US)

Skips non-essential OOBE screens (EULA, OEM registration, online account prompts)

Assigns a unique machine identity during deployment

Compatible with WinPE, VHD/VHDX boot, and bare-metal installation

Preserves activation, licensing, servicing stack integrity, and system binaries

Why RID 1000

Ensures the first real local account receives RID 1000, preventing SID shifts caused by temporary setup or provisioning accounts.

This maintains predictable user namespace alignment across deployments.

Scope & Limitations

This configuration:

Does not bypass TPM, Secure Boot, or CPU requirement checks

Does not alter activation, licensing, or product keys

Does not execute scripts or modify the registry outside documented unattended schema

Stores no passwords, keys, or sensitive data

It strictly follows Microsoft’s documented unattended deployment structure.

Deployment

Save the file as Autounattend.xml

Place it in the root of a Windows 11 installation USB

Boot the target machine from the USB

Windows Setup processes the file during:

specialize — system identity initialization and hardware preparation

oobeSystem — user creation and final provisioning

No additional tooling is required.

Optional: Compatible with VHD/VHDX-based deployment and recovery workflows.

Compatibility

Windows 11 installation media (21H2 or newer)

WinPE environments

Bare-metal or virtualized deployments

Offline or fully online installation workflows

Online Installation Behavior

This configuration is safe to use while connected to the internet.

Because it does not provision Microsoft accounts or alter identity workflows, Windows remains in a standard retail configuration. Windows Update and activation operate normally.
