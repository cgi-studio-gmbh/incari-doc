# Overview

![The On Mouse Move Node.](../../../.gitbook/assets/toolbox/events/OnMouseMove.PNG)

Moving a mouse on an **Object** supplied to the **Attributes**'s **Object** section will trigger the **On Mouse Move** **Node**. The **Node** returns the absolute **Screen** position of the mouse pointer when it's moved anywhere over the **Object**.

# Attributes
## Object
|Attribute|Type|Description|
|---|---|---|
|`Object`|**ObjectID**|Moving the mouse over this **Object** will trigger the **On Mouse Move** **Node**.|

# Inputs

|Input|Type|Description|
|---|---|---|
|*Pulse Input* (►)|**Pulse**|A standard **Input Pulse**, to trigger the execution of the **Node**.|

# Outputs

|Output|Type|Description|
|---|---|---|
|*Pulse Output* (►)|**Pulse**|A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution.|
|`Position`|**Vector2**|Returns the absolute `Position` of the mouse when it's moved anywhere on the **Object**. |

# See Also
[**On Mouse Button Up**](on-mouse-button-up.md)

[**On Mouse Double Click**](on-mouse-double-click.md)

