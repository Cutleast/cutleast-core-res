# Cutleast Core Res

This repository contains common resources used by my projects.

As it's all licensed under MIT, feel free to do whatever you want, only **exceptions are**:

- ./icons/discord.png
- ./icons/ko-fi.png
- ./icons/nexus_mods.png

which belong to their respective owners.

## Usage

Using the stylesheets requires inserting the placeholders `<accent_color>` and `<highlighted_accent>` and bundling the icons in a compiled Qt resource module accessible under `:/icons/`.

It's recommended to subclass [ui.utilities.theme_manager.ThemeManager](https://github.com/Cutleast/cutleast-core-lib/blob/master/src/cutleast_core_lib/ui/utilities/theme_manager.py) from the [cutleast-core-lib](https://github.com/Cutleast/cutleast-core-lib).

## Installation in projects

1. Add this repository as a [git submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules) to `<project root>/core-res` with this command:
    `git submodule add -b master https://github.com/Cutleast/cutleast-core-res.git core-res`.
2. Add the following to your `resources.qrc` file under `<qresource>`:
```xml
        <!-- Dark mode icons -->
        <file alias="icons/dark/arrow_down.svg">../core-res/icons/dark/arrow_down.svg</file>
        <file alias="icons/dark/arrow_left.svg">../core-res/icons/dark/arrow_left.svg</file>
        <file alias="icons/dark/arrow_right.svg">../core-res/icons/dark/arrow_right.svg</file>
        <file alias="icons/dark/arrow_up.svg">../core-res/icons/dark/arrow_up.svg</file>
        <file alias="icons/dark/checkmark.svg">../core-res/icons/dark/checkmark.svg</file>
        <file alias="icons/dark/exit.svg">../core-res/icons/dark/exit.svg</file>
        <file alias="icons/dark/horizontal_grip.png">../core-res/icons/dark/horizontal_grip.png</file>
        <file alias="icons/dark/quick_reference.svg">../core-res/icons/dark/quick_reference.svg</file>
        <file alias="icons/dark/search.svg">../core-res/icons/dark/search.svg</file>
        <file alias="icons/dark/vertical_grip.png">../core-res/icons/dark/vertical_grip.png</file>

        <!-- Disabled icons -->
        <file alias="icons/disabled/arrow_down.svg">../core-res/icons/disabled/arrow_down.svg</file>
        <file alias="icons/disabled/arrow_left.svg">../core-res/icons/disabled/arrow_left.svg</file>
        <file alias="icons/disabled/arrow_right.svg">../core-res/icons/disabled/arrow_right.svg</file>
        <file alias="icons/disabled/arrow_up.svg">../core-res/icons/disabled/arrow_up.svg</file>

        <!-- Light mode icons -->
        <file alias="icons/light/arrow_down.svg">../core-res/icons/light/arrow_down.svg</file>
        <file alias="icons/light/arrow_left.svg">../core-res/icons/light/arrow_left.svg</file>
        <file alias="icons/light/arrow_right.svg">../core-res/icons/light/arrow_right.svg</file>
        <file alias="icons/light/arrow_up.svg">../core-res/icons/light/arrow_up.svg</file>
        <file alias="icons/light/checkmark.svg">../core-res/icons/light/checkmark.svg</file>
        <file alias="icons/light/exit.svg">../core-res/icons/light/exit.svg</file>
        <file alias="icons/light/horizontal_grip.png">../core-res/icons/light/horizontal_grip.png</file>
        <file alias="icons/light/quick_reference.svg">../core-res/icons/light/quick_reference.svg</file>
        <file alias="icons/light/search.svg">../core-res/icons/light/search.svg</file>
        <file alias="icons/light/vertical_grip.png">../core-res/icons/light/vertical_grip.png</file>

        <!-- Other icons -->
        <file alias="icons/close.svg">../core-res/icons/close.svg</file>
        <file alias="icons/discord.png">../core-res/icons/discord.png</file>
        <file alias="icons/ko-fi.png">../core-res/icons/ko-fi.png</file>
        <file alias="icons/nexus_mods.png">../core-res/icons/nexus_mods.png</file>

        <!-- Stylesheets -->
        <file alias="base_stylesheet.qss">../core-res/base_stylesheet.qss</file>
        <file alias="dark_stylesheet.qss">../core-res/dark_stylesheet.qss</file>
        <file alias="light_stylesheet.qss">../core-res/light_stylesheet.qss</file>
```
