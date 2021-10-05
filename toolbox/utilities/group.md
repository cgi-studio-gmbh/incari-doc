# Group

## Overview

#### Example Node

![The Group Node.](../../.gitbook/assets/group%20%281%29.PNG)

A **Group Node** is used as a container for other **Logic**. As the color, opacity, size, and name can all be changed, it is very useful for management and organization.

The easiest way to create a **Group** is to select some **Nodes** and then press `Ctrl` + `G`, but it is also available in the right-click context menu.

Another advantage of the **Group Node** is that, by changing the `Name` **Attribute** you can easily create descriptive comments for your blocks of **Logic**. When you zoom out beyond a certain threshold within the **Logic Editor**, text on **Nodes** is no longer rendered, however, the _names_ of the **Group Nodes** are.

![](../../.gitbook/assets/node-group-example.png)

## Attributes

### Color

| Attribute | Type | Description |
| :--- | :--- | :--- |
| `Color` | **Color** | The **Color** of the **Group Node**. |
| `ZIndex` | **Int** | The `ZIndex` determines the stack order of the **Group** **Node**. Therefore a **Group** **Node** with a higher `ZIndex` will be stacked in front of a **Group** **Node** with a lower `ZIndex` in the **Logic Editor**. |
| `Content Alpha` | **Int** | The _alpha_ value of the **Group** **Node**'s color space. |

## Usage

![Group Node Usage](../../.gitbook/assets/group%20%283%29%20%284%29%20%284%29%20%284%29%20%281%29%20%287%29.gif)

## See Also

* [**Camera**](https://github.com/cgi-studio-gmbh/incari-doc/tree/66656c2442958de634bc73f77b533a03f83df0fb/toolbox/utilities/camera.md)
* [**List**](https://github.com/cgi-studio-gmbh/incari-doc/tree/66656c2442958de634bc73f77b533a03f83df0fb/toolbox/utilities/list.md)

