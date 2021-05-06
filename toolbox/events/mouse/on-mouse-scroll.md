# Overview

![The On Mouse Scroll Node.](../../../.gitbook/assets/toolbox/events/OnMouseScroll.PNG)

A mouse scroll on an **Object** supplied to the **Attributes**'s **Object** section will trigger the **On Mouse Scroll** **Node**. The **Node** returns the absolute **Screen** position of the mouse pointer.

# Attributes

|Attribute|Type|Description|
|---|---|---|
## Object
|Attribute|Type|Description|
|---|---|---|
|`Object`|**ObjectID**|Scrolling the mouse over this **Object** will trigger the **On Mouse Scroll** **Node**.|


# Inputs

|Input|Type|Description|
|---|---|---|
|*Pulse Input* (►)|**Pulse**|A standard **Input Pulse**, to trigger the execution of the **Node**.|

# Outputs

|Output|Type|Description|
|---|---|---|
|*Pulse Output* (►)|**Pulse**|A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution.|
|`Position`|**Vector2**|Returns the absolute `Position` of the mouse cursor when it's scrolled on the **Object**. |

# See Also
[**On Mouse Button Up**](on-mouse-button-up.md)

[**On Mouse Double Click**](on-mouse-double-click.md)

[**On Mouse Move**](on-mouse-move.md)
