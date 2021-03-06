# RISC Game/Application Guide [WIP]

This will be WIP for a short time while working out the layout. Goal is to document running native Linux (binary/source), translated x86 Linux(Box86/64), and emulated Windows (Wine) games and productivity applications and working state. To keep this list curated and manageable, focus should be put on titles that at least initiate a graphical session; first objective is listing all games/apps that are legitimately playable/usable.

The following Games are tested using aarch64 hardware using a desktop class AMD GPU. Will add details for alternative archetectures at some point, as I only have access to older ppc64 hardware.

## Natively Available

[Working Games List](Native)

## Box86/64 Translation

[Games List](Box86)

[Steam Games List](Box86Steam)

## BoxWine Translation

[Working Games List](BoxWine)

[Working Steam Games List](BoxWineProton)

## Setup

Guide currently references the HoneyComb LX2K (aarch64) running Debian, but should apply to most modern ARM devices running debian-based systems by tweaking a few flags:

[Setup Multiarch, Box86/64, Wine and Steam](https://github.com/Wooty-B/LX2K_Guide/blob/main/Setup-Armhf-Chroot.md)

### Notes

1. MSI Package "dxvk" (DirectX-to-Vulkan) does not improve quality/framerate for some DirectX 9 games. (i.e.: Oblivion and Fallout 3) Therefore, not installing the package in your Wine directory (~/.wine/drive_c) will allow you to use games in Windowed mode, as Windowed mode is not available in the dxvk package and causes applications to crash.

2. Anti-Aliasing in some games seems to have the biggest impact in performance. May be my system/hardware.

3. Steam Proton "should" work out-of-the-box! Just open Big Picture mode, navigate to the app in question and select Manage Game. Set Steam Play options, and "force" the game to use a version of Proton of your choosing. When you exit, Small View will show only your Linux and Proton selected titles. (Unless you select "All Games" of course)

4. If you have issues with delayed keyboard input, try accessing your desktop Accessibility settings and disable "Repeat Keys".
