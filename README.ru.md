# Гайд по оптимизации Escape from Tarkov
Read this in other languages: [English](README.md), [Russian](README.ru.md)

*Локализовано под Windows 10 - названия некоторых пунктов могут незначительно отличаться в зависимости от Вашей системы*

## Руководство
Это руководство предназначено для повышения производительности в игре Escape from Tarkov.

Если вы считаете, что это руководство можно улучшить, пожалуйста, дайте мне знать.

## Содействие
При желании каждый может внести свой вклад.

## Table of Contents

- [Обновление драйверов видеокарты](#обновление-драйверов-видеокарты)
- [Настройки NVIDIA](#настройки-nvidia)
- [Настройки AMD](#настройки-amd)
- [Оптимизация полноэкранного режима](#оптимизация-полноэкранного-режима)
- [Файл подкачки](#файл-подкачки)
- [Настройки электропитания](#настройки-электропитания)
- [Оптимизация фоновых процессов](#оптимизация-фоновых-процессов)
  - [Discord](#discord)
  - [Google Chrome](#google-chrome)
- [Graphics settings in the game](#graphics-settings-in-the-game)
- [Windows Performance](#windows-performance)
- [SSD optimizations](#ssd-optimizations)
- [Очистка временных файлов](#очистка-временных-файлов)
- [How fix NVIDIA Freestyle](#how-fix-nvidia-freestyle)

## Обновление драйверов видеокарты

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

## Оптимизация полноэкранного режима

- Зайдите в корневую папку игры
- Зайдите в **Свойства** файла **EscapeFromTarkov.exe**
- Перейдите в **Совместимость** и поставьте галочку **Отключить оптимизацию во весь экран**
- На той же странице нажмите **Изменить параметры высокого DPI**
- Поставьте галочку **Переопределение режима маштабирования высокого разрешения**, используйте выпадающее меню ниже **Масштабирование выполняется:**, и выберите **Приложение**
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
- Для игры Escape from Tarkov рекомендуются значения 15000-25000, независимо от объема установленной оперативной памяти. **Устанавливайте одинаковые значения в обеих строках!**
- Нажмите **Задать** и **OK**
- Нажмите **Win+R**, напишите **regedit** и нажмите **enter**
- Перейдите по пути **HKEY_LOCAL_MACHINE \ SYSTEM \ CurrentControlSet \ Control \ Session Manager \ Memory Management**
- В правой панели найдите **ClearPageFileAtShutdown** и установите значение **1**
- Перезагрузите компьютер

## Настройки электропитания

- Нажмите **Win+R**, напишите **powercfg.cpl** и нажмите **enter**
- Выберите **Высокая производительность**

## Оптимизация фоновых процессов

### Discord

- Перейдите в **Настройки пользователя**
- В левой панели нажмите **Внешний вид**
- Выключите **Аппаратное ускорение**
- В левой панели нажмите на **Оверлей**
- Выключите **Включить внутриигровой оверлей.**

### Google Chrome

- Используя адресную строку, перейдите **chrome://settings/**
- В левой панели нажмите **Дополнительные**
- Перейдите в **Система**
- Выключите **Не отключать работающие в фоновом режиме сервисы при закрытии браузера**

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

## Очистка временных файлов

**ВНИМАНИЕ**: Если вы не понимаете, что такое временные файлы, пропустите данный пункт!

- Нажмите комбинацию **Win+R**, наберите **%temp%** и нажмите **Enter**
- Удалите все файлы в открывшейся папке.

- Нажмите комбинацию **Win+R**, наберите **temp** и нажмите **Enter**
- Удалите все файлы в открывшейся папке.

- Нажмите комбинацию **Win+R**, наберите **prefetch** и нажмите **Enter**
- Удалите все файлы в открывшейся папке.

Пропустите неудаляющиеся файлы!

## How fix NVIDIA Freestyle

**Researching**
