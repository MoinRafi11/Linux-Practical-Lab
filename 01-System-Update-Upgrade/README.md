# Linux System Update & Upgrade Commands

This section covers basic commands used to update the package information and upgrade installed packages on a Linux system.

---

## 1. `apt update`

Updates the local package index and retrieves information about available packages and their latest versions.

### Command

```bash
sudo apt update

Purpose:

1.Refreshes the local package repository information.
2.Checks for available package updates.
3.Does not install or upgrade packages.


## 2. `apt upgrade`

Upgrades installed packages to their latest available versions.

### Command

sudo apt upgrade

Purpose:

1.Installs available updates for currently installed packages.
2.Helps keep the system and installed software up to date.
3.May ask for confirmation before installing updates.

## 3. `apt list --upgradable`

Lists packages that have newer versions available.

### Command

apt list --upgradable

Purpose:

1.Shows packages that can be upgraded.
2.Useful for checking available upgrades before running apt upgrade.

🔄 Basic Update Workflow:

A common update workflow is:

sudo apt update
sudo apt upgrade
apt list --upgradable


Command Flow:

apt update
    ↓
Refresh package information
    ↓
apt upgrade
    ↓
Install available package updates
    ↓
apt list --upgradable
    ↓
Check for remaining available upgrades


🧪 Practical Usage:

These commands were executed and tested on an Ubuntu Linux virtual machine as part of this Linux Practical Lab.
