# My Dotfiles

This repository contains my personal configurations for the Linux Fedora environment, including the i3
 window manager and app settings.

**All the setup is highly personal and customized to my environment and needs, but the repository's
 structure and scripts can serve as inspiration for organizing your own dotfiles.**

## Why Dotfiles
With increasing customization, I realised the necessity to keep all my customizations together into one
 place, making it easier to review, back up, and quickly set up a new system when needed.

## Main Idea
The core principles behind this setup:
1. **Centralized Configuration**: All configuration files containing my customizations (e.g., `.bashrc`,
 `.config`, etc.) are stored in a single directory, allowing for organized backups and version control.
2. **Symbolic Links**: Instead of duplicating files, symlinks poin from original configuration file
 locations to these centralized configurations.
3. **Automation with Scripts**:
   -  A script to automate the installation of necessary software (`dnf install` script).
   -  Another script to recreate symbolic links in the appropriate locations, linking the centralized
    dotfiles to where they are expected by the system.

This structure ensures that all configurations can be managed in a single, version-controlled repository,
 making it easy to replicate the environment on a new system.

## How To Use
1. **Clone the Repository:**
```
git clone https://github.com/ElinaZoldnere/dotfiles.git
cd dotfiles
```
2. **Review and Customize:**
   - **If you intend to use any of my configurations directly, carefully review configuration files and both 
   `dnf-reinstall` and `config-symlinks` scripts and adapt them to match your system setup and preferences.**
   - Back up existing configuration files before proceeding.
3. **Install Necessary Software:**
   - Run the `dnf-reinstall` script first to ensure the required software is installed before linking configuration files:
```
./scripts/dnf-reinstall
```
4. **Create Symbolic Links:**
   - Run the symlink creation script to link the actual configuration files to their expected locations:
```
./scripts/config-symlinks
```
**Note**: This guide is primarily for personal use but can serve as inspiration. It assumes familiarity with Linux systems 
and configuration management. Always adapt and modify the configurations and scripts to suit your system and 
preferences.
