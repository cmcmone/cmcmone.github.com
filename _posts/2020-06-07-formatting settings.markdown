---
layout: post
title:  "Formatting Settings in Visual Studio 2019"
date:   2020-06-07 12:30:35 -1234
categories: Settings K&R-derived VisualStudio2019
excerpt:  ...... 
---

Formatting settings in Visual Studio 2019 use K&R-derived layout and more.

## Indent

For set indent in Visual Studio 2019, from top menu: `Tools` -> `Options` -> `Text Editor` -> `Tabs` options:

## Line width

For set line width in Visual Studio 2019:

1. From top menu: `Extensions` -> `Manage Extensions` options. (<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>X</kbd>)

![]()

2. Search(<kbd>Ctrl</kbd> + <kbd>E</kbd>) `editor Guidelines` in the upper right corner and Download the `editor Guidelines`.

![]()

3. Close Visual Studio 2019 and start installing this extension.

![]()

4. For set line width, from top menu: `View` -> `Other Windows` -> `Command Window` options. **`Edit.AddGuideline`** and **`Edit.RemoveGuideline`** commands used to set the line width and remove the line width.

    i.e. To place a guide to the right of column 110, use `Edit.AddGuideline 110`.

## K&R layout

For set layout in Visual Studio 2019, from top menu: `Tools` -> `Options` -> `Text Editor` -> `C/C++` -> `Formatting` options:

## Reset the settings to default

For reset the settings in Visual Studio 2019, from top menu: `Tools` -> `Import and Export Settings...`options, you can also import or export settings.
