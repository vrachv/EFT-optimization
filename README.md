# Escape from Tarkov optimization guide
Read this in other languages: [English](README.md), [Russian](README.ru.md)

## Guidelines
This guide is designed to improve performance in the game Escape from Tarkov.
We aren't responsible for your actions on your computer.

If you think this guide can be improved, please let me know.

## Contributing to this project
Anyone and everyone is welcome to contribute.

## Table of Contents

### General recommendations

- [Update GPU Drivers](#update-gpu-drivers)
- [NVIDIA Settings](#nvidia-settings)
- [AMD Settings](#amd-settings)
- [Virtual memory](#virtual-memory)
- [Power Options](#power-options)
- [Graphics settings in the game](#graphics-settings-in-the-game)
- [SSD optimizations](#ssd-optimizations)
- [How enable NVIDIA Freestyle (12.5+)](#how-enable-nvidia-freestyle)

### For weak PCs

- [Full-screen optimizations](#full-screen-optimizations)
- [Optimize Background Processes](#optimize-background-processes)
  - [Discord](#discord)
  - [Google Chrome](#google-chrome)
  - [XBOX DVR](#xbox-dvr)
- [Cleaning Temp folder](#cleaning-temp-folder)

# Fast decision

If you don't understand or don't want to do everything manually, you can use **.reg** file. The text guide contains more information.

- Optimization **.reg** file — [Download](https://github.com/vrachv/EFT-optimization/releases/download/1.0.0/optimization.reg)
- Reset optimization settings  — [Download](https://github.com/vrachv/EFT-optimization/releases/download/1.0.0/default.reg)

Reboot PC for apply.

# General recommendations

## Update GPU Drivers

You must have the latest driver for your GPU.

NVIDIA drivers — [Download](https://www.nvidia.com/download/index.aspx)

AMD drivers — [Download](https://www.amd.com/en/technologies/radeon-software)

## NVIDIA Settings

1. Open **NVIDIA Control Panel**
2. Go to the **Adjust image settings with preview**
3. Click the **Use my preference emphasising** and move the value to **Performance**
4. **Apply**
5. Go to **Manage 3D settings**
6. Click the **Program Settings**
7. Select or add **EscapeFromTarkov.exe** application
8. Set these settings:

| Feature                             | Setting                    |
| ----------------------------------- | -------------------------- |
| Vertical sync                       | Off                        |
| Virtual Reality pre-rendered frames | 1                          |
| Shader Cache                        | On                         |
| Power management mode               | Prefer maximum performance |
| Triple buffering                    | Off                        |

9. **Apply**

## AMD Settings

**TODO**

## Virtual memory

1. Press **Win+R**, type `control` and press enter key
2. Go to the **System** and click **Advanced system settings**
3. Click on the **Advanced** tab
4. Click the **Settings** button from under the **Performance**
5. Click on the **Advanced** tab
6. Click the **Change** button from under the **Virtual memory**
7. Uncheck the **Automatically manage paging file size for all drives** checkbox
8. Click on the drive on which Windows is installed and set **Custom size**
9. For EFT, it is recommended to set from **15000-25000**, regardless of the size of RAM. **Set the same value on both lines!**
10. Click **Set** and **OK**
11. Press **Win+R**, type `regedit` and press enter key
12. Go to `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager\Memory Management`
13. Locate **ClearPageFileAtShutdown** in the right panel and set value `1`
14. Reboot PC for apply

## Power Options

1. Press **Win** key and type `cmd`, right click the first result and select **Run as administrator**
2. Copy `powercfg -duplicatescheme e9a42b02-d5df-448d-aa00-03f14749eb61`, paste in cmd and press **enter** key
3. Reboot PC for apply

## Graphics settings in the game

Settings for minimum system requirements. If you have a good PC, you can increase the settings.

| Setting               | Value      |
| --------------------- | ---------- |
| Fullscreen mode       | Fullscreen |
| VSync                 | Disable    |
| Texture quality       | low-medium |
| Shadows quality       | low        |
| Object LOD quality    | 2          |
| Overall visibility    | 400-1000   |
| Shadow visibility     | 40         |
| Antialiasing          | off        |
| Resampling            | 1x off     |
| HBAO                  | off        |
| SSR                   | off        |
| Anisotropic Filtering | off        |
| Sharpness             | 0-0.5      |
| Lobby FPS Limit       | 60         |
| Game FPS Limit        | 120        |
| Z-Blur                | Uncheck    |
| Chrom. aberrations    | Uncheck    |
| Noise                 | Uncheck    |
| Grass Shadows         | Uncheck    |

- Go to the gameplay settings and turn on the auto ram cleaner. This can cause statters! If this is the case, turn off the option to clean the RAM!

Z-Blur, Chrom. aberratins, Noise and Grass Shadows don't affect performance, but may interfere with the gameplay.

## SSD optimizations

Escape from Tarkov should be installed on the SSD

1. Open file explorer and select **This PC**
2. Go to **Properties** of the **Local Disk (C:)**
3. In **General** tab uncheck **Allow files on this drive to have contents indexed in addition to file properties**
4. **Apply** and **OK**
5. Press **Win+R**, type `services.msc` and press enter key
6. Find **SysMain** in Services
7. Go to **Properties** and select **Startup Type** on **Disabled**
8. Press **Win** key and type `cmd`, right click the first result and select **Run as administrator**
9. Type `powercfg -h off` and press enter key
10. Reboot PC for apply

## How enable NVIDIA Freestyle

> Works: **0.12.6.7709**

1. If your NVIDIA driver is newer than version 445.87, uninstall it and install this version - [Download](http://us.download.nvidia.com/Windows/445.87/445.87-desktop-win10-64bit-international-dch-whql.exe)
2. Remove **GeForce Experience**
3. Install GFE version 3.20.0.118 — [Download](https://us.download.nvidia.com/GFE/GFEClient/3.20.0.118/GeForce_Experience_v3.20.0.118.exe)
4. Run **GeForce Experience** and login to your NVIDIA account
5. Press **Win+R**, type `C:\Program Files\NVIDIA Corporation\NVIDIA GeForce Experience`, press enter key and open **NVIDIA GeForce Experience.json** (Using Notepad++ — [Download](https://notepad-plus-plus.org/downloads/))
6. Find `"nv-self-update-path=Downloader\\gfeupdate.json",`
7. Replace `Downloader` with `1Downloader`
8. Save changes and close file

**If something doesn't work:**
- Don't use GeForce Experience experimental features
- Carefully check the version of GFE and NVIDIA driver

**ReShade filters for NVIDIA freestyle:**
1. [Download](https://mega.nz/file/kUkjgLZC#_z1lzI1a1eCXDASQ7CwxA_36PGlFg7d7mBsuuWLfofo)
2. Copy folder **Custom** along the path `C:\Program Files\NVIDIA Corporation\Ansel` (create Ansel folder if it doesn't exist)

# For weak PCs

## Full-screen optimizations

1. Go to the root folder of the game
2. Go to **Properties** of the **EscapeFromTarkov.exe**
3. Go to **Compatibility** tab and tick **Disable full-screen optimizations**
4. On the same tab, go to **Change high DPI settings**
5. Tick **Override high DPI scaling behavior** and use the **Scaling performed by:** drop-down menu, and select **Application**
6. **OK** and again **OK**

## Optimize Background Processes

### Discord

1. Go to the **User Settings**
2. Go to the **Appearance**
3. Uncheck the **Hardware Acceleration**
4. Go to the **Overlay**
5. Uncheck the **Enable in-game overlay.**

### Google Chrome

1. Using the address bar, go `chrome://settings/`
2. Click the **Advanced**
3. Go to the **System** tab
4. Uncheck the **Continue running background apps when Google Chrome is closed**

### XBOX DVR

NVIDIA GPUs are limited to two encoding sessions. Game DVR and Geforce Experience(ShadowPlay) will often consume both of these sessions if enabled, preventing you from recording or streaming(or both simultaneously) when using NVENC. Game DVR can also cause performance issues, it is still recommended to disable Game DVR even if you don't plan on using hardware encoding.

1. Right-click the Start button
2. Click **Settings**
3. Click **Gaming**
4. Click **Game Bar**
5. Set **Record game clips, screenshots and broadcast using Game bar** to **Off**
6. Click **Game Mode**
7. Set **Game Mode** to **Off**
8. Click **Captures**
9. Set **Record in the background while I'm playing a game** to **Off**
10. Reboot PC for apply

## Cleaning Temp folder

**WARNING**: If you don't understand what temporary files are, don't do this.

1. Press **Win+R**, type `%temp%` and press enter key
2. Delete everything in the folder that opens.
3. Press **Win+R**, type `temp` and press enter key
4. Delete everything in the folder that opens.
5. Press **Win+R**, type `prefetch` and press enter key
6. Delete everything in the folder that opens.

Files that aren't deleted must be skipped!
