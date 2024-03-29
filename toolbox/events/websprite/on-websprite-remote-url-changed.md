# Overview

![The On WebSprite Remote URL Change Node.](../../../.gitbook/assets/onwebspriteremoteurlchangeupdatedimage.png)

**On WebSprite Remote URL Change** is an **Event Listener** **Node** used for executing a **Logic Branch** when the URL of a **WebSprite** changes.

[**Scope**](../../overview.md#scopes): **Scene**, **Prefab**.

# Attributes

![The On WebSprite Remote URL Change Node Attributes.](../../../.gitbook/assets/node-onwebspriteremoteurlchanged-attri.png)

|Attribute|Type|Description|
|---|---|---|
| `Object` | **ObjectID** | The **WebSprite** **Object** whose URL changing triggers the **Logic Branch**, if none is given in the **Input Socket**. | 

# Inputs

|Input|Type|Description|
|---|---|---|
|*Pulse Input* (►)|**Pulse**|A standard **Input Pulse**, to trigger the execution of the **Node**.|
| `Object ID` | **ObjectID** | The **WebSprite** **Object** whose URL changing triggers the **Logic Branch**. | 
| `Subscribe` (►)|**Pulse** | An **Input Pulse** that needs to be triggered to start listening to the **Event**. |

# Outputs

|Output|Type|Description|
|---|---|---|
|*Pulse Output* (►)|**Pulse**|A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution.|
| `Remote URL` | **String** | The new URL of the **WebSprite** **Object**. |
| `Object ID` | **ObjectID** | The **WebSprite** **Object** whose URL changing triggered the **Logic Branch**. |

# See Also

* [**WebSprite Objects**](../../../objects-and-types/scene-objects/web-sprite.md)
* [**WebSprite Nodes**](../../incari/websprite/README.md)



