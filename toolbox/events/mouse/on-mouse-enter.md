# Overview

![The On Mouse Enter Node.](../../../.gitbook/assets/toolbox/events/OnMouseEnter.PNG)

**On Mouse Enter** **Node** is triggered when a mouse cursor moves over an **Object** supplied to the **Attributes**'s **Object** section. The **Node** returns the absolute **Screen** position of the mouse cursor at the point where the cursor moves over the **Object**.

# Attributes

|Attribute|Type|Description|
|---|---|---|
## Object
|Attribute|Type|Description|
|---|---|---|
|`Object`|**ObjectID**|Moving the mouse cursor over this **Object** will trigger the **On Mouse Enter** **Node**.|

# Inputs

|Input|Type|Description|
|---|---|---|
|*Pulse Input* (►)|**Pulse**|A standard **Input Pulse**, to trigger the execution of the **Node**.|

# Outputs

|Output|Type|Description|
|---|---|---|
|*Pulse Output* (►)|**Pulse**|A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution.|
|`Position`|**Vector2**|Returns the absolute `Position` of the mouse cursor on the **Screen** at the point where it enters over the **Object**. |

# See Also
[**On Mouse Button Up**](on-mouse-button-up.md)

[**On Mouse Double Click**](on-mouse-double-click.md)

[**On Mouse Leave**](on-mouse-leave.md)
