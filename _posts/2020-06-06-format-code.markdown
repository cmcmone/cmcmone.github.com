---
layout: post
title:  "How to format code in Visual Studio 2019"
date:   2020-06-06 13:52:35 -0411
categories: CodeFormatting VisualStudio2019
excerpt:  In order to maintain the unity of code style in teamwork, we should format the code before submitting to Github....... 
---

In order to maintain the unity of code style in teamwork, we should format the code before submitting to Github.

### Shortcut Key

Format the code in Visual Studio 2019 (Windows):

|Shortcut Key|Description|
|:---|:---|
|<kbd>Ctrl</kbd> + <kbd>K</kbd>, and <kbd>Ctrl</kbd> + <kbd>D</kbd>|Format the whole document|
|<kbd>Ctrl</kbd> + <kbd>K</kbd>, and <kbd>Ctrl</kbd> + <kbd>F</kbd>|Format Selection only|

### Set Code Style

For set code style in `Visual Studio 2019`, from top menu: `Tools` -> `Options` -> `Text Editor` options, then click the language of your choice(I used `C++`).

![Text Editor](https://github.com/cmcmone/cmcmone.github.com/blob/master/imgs/202006/texteditor.png?raw=true)

### Set Keyboard

For change the shortcut key in `Visual Studio 2019`, from top menu: `Tools` -> `Options` -> `Environment` -> `Keyboard` options.

![Keyboard](https://github.com/cmcmone/cmcmone.github.com/blob/master/imgs/202006/keyboard.png?raw=true)

### Extensions

Of course, you can also use an extension to automatically format the code when it is saved, from top menu: `Extensions` -> `Manage Extensions`, then search `format` in the upper right corner and install `Format document on Save`.

![Extension](https://github.com/cmcmone/cmcmone.github.com/blob/master/imgs/202006/extension.png?raw=true)
