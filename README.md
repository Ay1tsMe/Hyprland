# Hyprland Installation Script

![Desktop Image](.images/swappy-20230410_131336.png) (replace with GIF)

This repository contains an install script to set up Hyprland on a fresh **Arch-based installation.** The script installs only the essential components required to get Hyprland up and running. It does not include everyday use packages such as web browsers, text editors, or other utilities. You can also just grab the .dotfiles and use them for your hyprland DE. **Has not been tested with a NVIDIA GPU. Your mileage may vary.**

**Note:** This script was inspired by [SolDoesTech's HyprV2 config](https://github.com/SolDoesTech/HyprV2) and has been edited to fit my needs. 

## Table of Contents

1. [Differences between the two scripts](#differences-between-the-two-scripts)
2. [Installation](#installation)
3. [Launching Hyprland](#launching-hyprland)
4. [Customizing Theme, Icons, and Wallpaper](#customizing-theme-icons-and-wallpaper)
5. [Additional Packages](#additional-packages)

## Differences between the two scripts.

The following changes have been made from HyprV2's Script:

1. Removed SDDM:
   - No longer includes the installation and setup of the SDDM login manager and related theme configurations.

2. Removed ASUS ROG software:
   - Does not provide optional installation and setup of software support for ASUS ROG laptops.

3. Added nwg-looks:
   - includes the installation of the `nwg-looks` package, which is a customization tool for GTK and icon themes, wallpapers, and more.

4. Changed Waybar weather script to Celsius:
   - The Waybar weather script has been updated to display temperatures in Celsius instead of the default Fahrenheit.

5. Removed update-sys script:
   - No longer includes the `update-sys` script for system updates and maintenance.

6. Removed dual theme (possible plans to add it in the future):
   - Removed the dual theme configuration. There might be plans to reintroduce this feature in future updates.

7. Updated hyprland.conf to meet personal preferences (editable by users):
   - The `hyprland.conf` configuration file has been modified to meet my preferences. You can edit this file to suit your own needs and preferences if desired. config file is located in:
   ```bash
   ~/.config/hypr
   ```

**If you need any of the above features, then use [SolDoesTech's install script](https://github.com/SolDoesTech/HyprV2)**


## Installation

To install Hyprland, follow these steps:

1. Clone this repository or download the `install.sh` script.
2. Make the script executable by running `chmod +x install.sh`.
3. Run the install script with `./install.sh`.

## Launching Hyprland

Once the installation is complete, type `Hyprland` in the terminal (TTY) to launch the Hyprland desktop environment.

## Customizing Theme, Icons, and Wallpaper
### Changing Theme and Icons with nwg-looks

`nwg-looks` is a customisation tool that allows you to easily change the GTK and icon themes for your Hyprland desktop environment. To change the theme and icons, follow these steps:

1. Launch nwg-looks by running the following command in the terminal:
```bash
nwg-looks
```
2. The `nwg-looks` GUI will open, and you can browse through the available GTK themes and icon sets.

3. Select the desired GTK theme and icon set by clicking on them.

4. Click the "Apply" button to save your changes.

### Changing Wallpaper with the setBG Script

You can change the wallpaper by editing the setBG script. The setBG script is responsible for setting the desktop wallpaper.

1. Open the setBG script in your preferred text editor. The script is located in the following directory:

```bash
~/.config/hypr/scripts/setBG
```
2. Change the following line to the wallpaper of your choice. (There are a few sample wallpapers located in the `~/.config/hypr/background` directory)

```bash
swww img /path/to/your/wallpaper.png
```

3. Replace /path/to/your/wallpaper.png with the path to the image file you want to use as your wallpaper.

4. Save the changes to the setBG script and restart Hyprland.

**Now, your Hyprland desktop environment will have a new theme, icons, and wallpaper according to your preferences.**

## Additional Packages

After installing Hyprland, you may want to install some commonly used packages for your everyday needs. Here are some recommendations:

- Web browser: `firefox`
- Code editor: `visual-studio-code` or `vim`
- Email client: `thunderbird`
- Communication app: `discord`
- Image editor: `gimp`

If you prefer to use the Zsh shell, you can install `zsh` and `oh-my-zsh` as well.

To install any of these packages, use the following command or read the documentation:

```bash
sudo pacman -S package-name
```
Replace package-name with the name of the package you want to install (e.g., firefox, vim, etc.).

**Enjoy your Hyprland experience!**
