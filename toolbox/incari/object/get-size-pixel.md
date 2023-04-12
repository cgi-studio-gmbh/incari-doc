# Get Size

## Overview

![The Get Size Node.](../../../.gitbook/assets/getsizenode.png)

The **Get Size Node** returns the X and Y values of a **2D Object's** `Size`.

[**Scope**](../../overview.md#scopes): **Scene**, **Function**, **Prefab**.

## Inputs

| Input | Type | Description |
| :--- | :--- | :--- |
| _Pulse Input_ \(►\) | **Pulse** | A standard **Input Pulse**, to trigger the execution of the **Node**. |
| `Object ID` | **ObjectID** | The ID of the target **Object** whose `Size` you wish to return. |

## Outputs

| Output | Type | Description |
| :--- | :--- | :--- |
| _Pulse Output_ \(►\) | **Pulse** | A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution. |
| `Size` | **Vector2** | A 2-dimensional **Vector** that contains the _X_ and _Y_ `Size` _values_ of the target **Object**. |

## See Also

* [**Get Position 2D (px)**](get-position-pixel.md)
* [**Get Rotation 2D**](get-rotation-pixel.md)

