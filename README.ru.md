#Гайд по оптимизации Escape from Tarkov
Read this in other languages: [English](README.md), [Russian](README.ru.md)

## Guidelines
Это руководство предназначено для повышения производительности в игре Escape from Tarkov.

Если вы считаете, что это руководство можно улучшить, пожалуйста, дайте мне знать.

## Contributing to this project
При желании каждый может внести свой вклад.

## Table of Contents

- [Обновление драйверов GPU](#обновление-драйверов-gpu)
- [Настройки NVIDIA](#настройки-nvidia)
- [Настройки AMD](#настройки-amd)
- [Полноэкранная оптимизация](#полноэкранная-оптимизация)
- [Файл подкачки](#файл-подкачки)
- [Power Options](#power-options)
- [Optimize Background Processes](#optimize-background-processes)
  - [Discord](#discord)
  - [Google Chrome](#google-chrome)
- [Graphics settings in the game](#graphics-settings-in-the-game)
- [Windows Performance](#windows-performance)
- [SSD optimizations](#ssd-optimizations)
- [Cleaning Temp folder](#cleaning-temp-folder)
- [How fix NVIDIA Freestyle](#how-fix-nvidia-freestyle)

## Обновление драйверов GPU

Рекомендуется установить последнюю версию драйвера для вашего GPU.

Драйвера NVIDIA — [LINK](https://www.nvidia.com/download/index.aspx)

Драйвера AMD — [LINK](https://www.amd.com/en/technologies/radeon-software)

## Настройки NVIDIA

- Откройте **Панель управления NVIDIA**
- Перейдите в **Регулировка настроек изображения с просмотром**
- Кликните на **Пользовательские настройки с упором на:** и установите значение **Производительность**
- Нажмите **Применить**
- Перейдите в **Управление параметрами 3D**
- Кликните на **Программные настройки**
- Выберите или добавьте приложение **EscapeFromTarkov.exe**
- Установите эти настройки:

| Функция                             | Параметр                   |
| ----------------------------------- | -------------------------- |
| Вертикальный синхроимпульс          | Выкл                       |
| Заранее подготовленные кадры в.р.   | 1                          |
| Кэширование шейдеров                | Вкл                        |
| Режим управления электропитанием    | Предпочтителен режим м. п. |
| Тройная буферизация                 | Выкл                       |

- Нажмите **Применить**

## Настройки AMD

**TODO**

## Полноэкранная оптимизация

- Зайдите в корневую папку игры
- Зайдите в **Свойства** файла **EscapeFromTarkov.exe**
- Перейдите в **Совместимость** и поставьте галочку **Отключить оптимизацию во весь экран**
- На той же странице нажмите **Изменить параметры высокого DPI**
- Поставьте галочку **Переопределите режим масштабирования выского разрешения.**, испольуйзте выпадающее меню ниже **Масштабирование выполняется:**, и выберите **Приложение**
- Нажмите **OK** и **OK**

## Файл подкачки

- Нажмите **Win+R**, напишите **control** и нажмите **enter**
- Перейдите в **Система** и слева нажмите **Дополнительные параметры системы**
- Перейдите в **Дополнительно**
- Нажмите **Параметры...** в блоке **Быстродействие**
- Перейдите в **Дополнительно**
- Нажмите **Изменить...** в блоке **Виртуальная память**
- Уберите галочку **Автоматически выбирать объем файла подкачки**
- Выберите системный диск и нажмите **Указать размер**
- Для игры Escape from Tarkov рекомендуются значения 15000-25000, независимо от количества оперативной памяти. **Устанавливайте одинаковые значения в обоих строках!**
- Нажмите **Задать** и **OK**
- Нажмите **Win+R**, напишите **regedit** и нажмите **enter**
- Перейдите по пути **HKEY_LOCAL_MACHINE \ SYSTEM \ CurrentControlSet \ Control \ Session Manager \ Memory Management**
- В правой панели найдите **ClearPageFileAtShutdown** и установите значение **1**
- Перезагрузите компьютер

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
