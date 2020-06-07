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

- move open braces to a new line for types

    ```c++
    namespace Namespace1
    class Class1
    {
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

- place close braces on separate lines for empty types, function bodies.

    ```c++
    class MyException
    {
    }

    MyClass::~MyClass()
    {
    }
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

    ![open braces](https://github.com/cmcmone/cmcmone.github.com/blob/master/imgs/202006/openbraces.png?raw=true)

    ![close braces](https://github.com/cmcmone/cmcmone.github.com/blob/master/imgs/202006/closebraces.png?raw=true)

## Indent

For set indent in Visual Studio 2019, from top menu: `Tools` -> `Options` -> `Text Editor` -> `Tabs` options:

![Indent](https://github.com/cmcmone/cmcmone.github.com/blob/master/imgs/202006/indenting.png?raw=true)

## Line width

For set line width in Visual Studio 2019:

1. From top menu: `Extensions` -> `Manage Extensions` options. (<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>X</kbd>)

2. Search(<kbd>Ctrl</kbd> + <kbd>E</kbd>) `editor Guidelines` in the upper right corner and Download the `editor Guidelines`.

    ![editor Guidelines](https://github.com/cmcmone/cmcmone.github.com/blob/master/imgs/202006/guidelines.png?raw=true)

3. Close Visual Studio 2019 and start installing this extension.

    ![install](https://github.com/cmcmone/cmcmone.github.com/blob/master/imgs/202006/install.png?raw=true)

4. For set line width, from top menu: `View` -> `Other Windows` -> `Command Window` options. **`Edit.AddGuideline`** and **`Edit.RemoveGuideline`** commands used to set the line width and remove the line width.

    i.e. to place a guide to the right of column 110, use `Edit.AddGuideline 110`.

    ![command](https://github.com/cmcmone/cmcmone.github.com/blob/master/imgs/202006/command.png?raw=true)

## Reset the settings to default

For reset the settings in Visual Studio 2019, from top menu: `Tools` -> `Import and Export Settings...`options, you can also import or export settings.

![reset](https://github.com/cmcmone/cmcmone.github.com/blob/master/imgs/202006/reset.png?raw=true)
