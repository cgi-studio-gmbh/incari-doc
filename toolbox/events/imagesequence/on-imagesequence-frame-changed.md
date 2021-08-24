# Overview

![The On Imagesequence Frame Changed Node.](../../../.gitbook/assets/node-on-imagesequence-frame-changed.png)

**On Imagesequence Frame Changed** is an **Event Listener** **Node** used for executing a **Logic Branch** when the frame of an **Image Sequence** changes.

# Attributes

|Attribute|Type|Description|
|---|---|---|
| `Object` | **ObjectID** | **Image Sequence** in which a frame change triggers the **Logic Branch**. |


# Outputs

|Output|Type|Description|
|---|---|---|
|*Pulse Output* (►)|**Pulse**|A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution.|
| `#Frame` | **Int** | Frame number within the sequence. |

# See Also

* [**Image Sequence**](README.md)

