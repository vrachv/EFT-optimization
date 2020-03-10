## Guidelines
This guide is designed to improve performance in the game Escape from Tarkov.

If you think this guide can be improved, please let me know.

## Contributing to this project
Anyone and everyone is welcome to contribute.

## Table of Contents

- [Update GPU Drivers](#update-gpu-drivers)
- [NVIDIA Settings](#nvidia-settings)
- [AMD Settings](#amd-settings)
- [Full-screen optimizations](#full-screen-optimizations)
- [Virtual memory](#virtual-memory)
- [Power Options](#power-options)
- [Optimize Background Processes](#optimize-background-processes)
  - [Discord](#discord)
  - [Google Chrome](#google-chrome)
- [Graphics settings in the game](#graphics-settings-in-the-game)
- [Windows Performance](#windows-performance)
- [SSD optimizations](#ssd-optimizations)
- [Cleaning Temp folder](#cleaning-temp-folder)
- [How fix NVIDIA Freestyle](#how-fix-nvidia-freestyle)

## Update GPU Drivers

You must have the latest driver for your GPU.

NVIDIA drivers — [LINK](https://www.nvidia.com/download/index.aspx)

AMD drivers — [LINK](https://www.amd.com/en/technologies/radeon-software)

## NVIDIA Settings

- Open **NVIDIA Control Panel**
- Go to the **Adjust image settings with preview**
- Click the **Use my preference emphasising** and move the value to **Performance**
- **Apply**
- Go to **Manage 3D settings**
- Click the **Program Settings**
- Select or add **EscapeFromTarkov.exe** application
- Set these settings:

| Feature                             | Setting                    |
| ----------------------------------- | -------------------------- |
| Vertical sync                       | Off                        |
| Virtual Reality pre-rendered frames | 1                          |
| Shader Cache                        | On                         |
| Power management mode               | Prefer maximum performance |
| Triple buffering                    | Off                        |

- **Apply**

## AMD Settings

- Open **AMD Radeon Settings**
- Go to the **Gaming**
- Click on **Global Settings**
- Click on the **Texture Filtering Quality** and select the **Performance**

## Full-screen optimizations

- Go to the root folder of the game
- Go to **Properties** of the **EscapeFromTarkov.exe**
- Go to **Compatibility** tab and tick **Disable full-screen optimizations**
- On the same tab, go to **Change high DPI settings**
- Tick **Override high DPI scaling behavior** and use the **Scaling performed by:** drop-down menu, and select **Application**
- **OK** and again **OK**

## Virtual memory

- Press **Win+R**, type **control** and press enter key
- Go to the **System** and click **Advanced system settings**
- Click on the **Advanced** tab
- Click the **Settings** button from under the **Performance**
- Click the **Change** button from under the **Virtual memory**
- Uncheck the **Automatically manage paging file size for all drives** checkbox
- Click on the drive on which Windows is installed and set **Custom size**
- For EFT, it is recommended to set from 15 to 30 GB, regardless of the size of RAM
- Click **Set** and **OK**
- Restart computer for apply


## Power Options

- Press **Win+R**, type **powercfg.cpl** and press enter key
- Select the **High performance**

## Optimize Background Processes

### Discord

- Go to the **User Settings**
- Go to the **Appearance**
- Uncheck the **Hardware Acceleration**
- Go to the **Overlay**
- Uncheck the **Enable in-game overlay.**

### Google Chrome

- Using the address bar, go **chrome://settings/**
- Click the **Advanced**
- Go to the **System** tab
- Uncheck the **Continue running background apps when Google Chrome is closed**

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

## Windows Performance

- Press **Win** key and type **performance**
- Click to **Adjust the appearance and performance of Windows** from the results
- Select the **Adjust for best performance**
- Tick the **Smooth edge of screen fonts** and **Show window contents while dragging**
- **Apply**

## SSD optimizations

Escape from Tarkov should be installed on the SSD

- Open file explorer and select **This PC**
- Go to **Properties** of the **Local Disk (C:)**
- In **General** tab uncheck **Allow files on this drive to have contents indexed in addition to file properties**
- **Apply**
- Press **Win+R**, type **services.msc** and press enter key
- Find **Superfetch** in Services
- Go to **Properties** and select **Startup Type** on **Disabled**
- Press **Win** key and type **cmd**, right click the first result and select **Run as administrator**
- Type **powercfg -h off** and press enter key
- Restart the computer

## Cleaning Temp folder

**WARNING**: If you don't understand what temporary files are, don't do this.

- Press **Win+R**, type **%temp%** and press enter key
- Delete everything in the folder that opens.
- Press **Win+R**, type **temp** and press enter key
- Delete everything in the folder that opens.
- Press **Win+R**, type **prefetch** and press enter key
- Delete everything in the folder that opens.

Files that aren't deleted must be skipped!

## How fix NVIDIA Freestyle

**Researching**
