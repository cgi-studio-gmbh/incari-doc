# Overview

![The On Hover Enter Node.](../../../.gitbook/assets/toolbox/events/OnHoverEnter.PNG)

Hovering a mouse on an **Object** supplied to the **Attributes**'s **Object** section will trigger the **On Hover Enter** **Node**. The **Node** returns the absolute position of the mouse cursor in the **Screen**.

# Attributes
## Object
|Attribute|Type|Description|
|---|---|---|
|`Object`|**ObjectID**|Mouse hover over this **Object** will trigger the **On Hover Enter** **Node**.|

# Inputs

|Input|Type|Description|
|---|---|---|
|*Pulse Input* (►)|**Pulse**|A standard **Input Pulse**, to trigger the execution of the **Node**.|

# Outputs

|Output|Type|Description|
|---|---|---|
|*Pulse Output* (►)|**Pulse**|A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution.|
|`Position`|**Vector2**|Returns the absolute `Position` of the mouse cursor at the point it's hovered over the **Object**. |

# See Also
[**On Hover Leave**](on-hover-leave.md)

[**On Mouse Move**](on-mouse-move.md)

