# Overview

![The On On-Screen Keyboard Input Changed Node.](../../../.gitbook/assets/node-on-onscreen-keyboard-input-changed.png)

The **On On-Screen Keyboard Enter Pressed** **Node** is an **Event Listener** **Node** used for executing a **Logic Branch** when the input of an **On-Screen Keyboard** is changed.

# Attributes

|Attribute|Type|Description|
|---|---|---|
|`Object` | **ObjectID** | The **On-Screen Keyboard** in which an input change triggers the **Logic Branch**. |

# Outputs

|Output|Type|Description|
|---|---|---|
|*Pulse Output* (►)|**Pulse**|A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution.|
| `Keyboard Input` | **String** | The input of the **On-Screen Keyboard**. |

