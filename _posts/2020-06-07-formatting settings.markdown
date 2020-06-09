---
layout: post
title:  "Formatting Settings in Visual Studio 2019"
date:   2020-06-07 12:30:35 -0400
categories: Settings K&R Layout VisualStudio2019
excerpt:  Formatting settings in Visual Studio 2019 use K&R-derived layout and more...... 
---

Formatting settings in Visual Studio 2019 use K&R-derived layout and more.

## K&R layout

For set [K&R layout](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#nl17-use-kr-derived-layout) in Visual Studio 2019, from top menu: `Tools` -> `Options` -> `Text Editor` -> `C/C++` -> `Formatting` options:

- move open braces to a new line for namespaces

    ```c++
    namespace Namespace1
    {
        namespace Namespace2
        {
        }
    }
    ```

- keep open braces on the same line for types

    ```c++
    namespace Namespace1
    class Class1 {
    };
    ```

- move open braces to a new line for functions

    ```c++
    void Function1()
    {
    }
    ```

- keep open braces on the same line for control blocks

    ```c++
    void Function()
    {
        while (cin >> word) {
            if (word.length() > 2) {
            }
        }
    }
    ```

- keep open braces on the same line for lambadas

    ```c++
    void Function()
    {
        auto lambda1 = []() {
        };
        auto lambda2 = [&]() {
        };
    }
    ```

- place braces on separate lines for scopes

    ```c++
    void Function()
    {
        // Scope
        {
            int i;
        }
    }
    ```

- keep close braces on the same line for empty types, function bodies.

    ```c++
    class MyException
    {}

    MyClass::~MyClass()
    {}
    ```

- place 'catch', 'else' and similar keywords on a new line

    ```c++
    try {
    }
    catch (...) {
    }

    if (a < b) {
    }
    else {
    }
    ```

    ![open braces](/imgs/202006/openbraces.png){: width="50%" height="50%"}

    ![close braces](/imgs/202006/closebraces.png){: width="50%" height="50%"}

## Indent

For set indent in Visual Studio 2019, from top menu: `Tools` -> `Options` -> `Text Editor` -> `Tabs` options:

![Indent](/imgs/202006/indenting.png){: width="50%" height="50%"}

Tips: If you set the indentation to `Keep tabs`, then 8 spaces will be displayed on Github. You can add `?ts=4` to a diff or file URL will display tab characters as 4 spaces wide instead of the default 8. For more details and other nuggets, please see [github-cheat-sheet](https://github.com/tiimgreen/github-cheat-sheet#adjust-tab-space)

## Line width

For set line width in Visual Studio 2019:

1. From top menu: `Extensions` -> `Manage Extensions` options. (<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>X</kbd>)

2. Search(<kbd>Ctrl</kbd> + <kbd>E</kbd>) `editor Guidelines` in the upper right corner and Download the `editor Guidelines`.

    ![editor Guidelines](/imgs/202006/guidelines.png){: width="50%" height="50%"}

3. Close Visual Studio 2019 and start installing this extension.

    ![install](/imgs/202006/install.png){: width="40%" height="40%"}

4. For set line width, from top menu: `View` -> `Other Windows` -> `Command Window` options. **`Edit.AddGuideline`** and **`Edit.RemoveGuideline`** commands used to set the line width and remove the line width.

    i.e. to place a guide to the right of column 110, use `Edit.AddGuideline 110`.

    ![command](/imgs/202006/command.png)

## Reset the settings to default

For reset the settings in Visual Studio 2019, from top menu: `Tools` -> `Import and Export Settings...`options, you can also import or export settings.

![reset](/imgs/202006/reset.png){: width="45%" height="45%"}
