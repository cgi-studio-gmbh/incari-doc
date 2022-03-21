# Overview

![The Set Local Rotation Node.](../../../.gitbook/assets/setlocalrotation.png)

The **Set Local Rotation Node**  assigns the local coordinates (in reference to the **Object** itself)  for a **3D Object's** *local rotation* in **Vector3** form. 

# Attributes

|Attribute|Type|Description|
|---|---|---|
|`Object`|**ObjectID**|The target **Object** whose local `Rotation` you wish to assign, if one is not provided in the `Object ID` **Socket**.|
|`Rotation`|**Vector3**| A 3-dimensional **Vector** that provides the X, Y, and Z _local rotation_ values for the target **Object**. |

# Inputs

|Input|Type|Description|
|---|---|---|
|*Pulse Input* (►)|**Pulse**|A standard **Input Pulse**, to trigger the execution of the **Node**.|
| `Object ID` | **ObjectID** | The ID of the target **Object** whose local `Rotation` you wish to assign.|
|`Rotation`|**Vector3**| A 3-dimensional **Vector** that provides the X and Y and Z _local rotation_ values for the target **Object**. |

# Outputs

|Output|Type|Description|
|---|---|---|
|*Pulse Output* (►)|**Pulse**|A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution.|

# See Also

* [**Set Local Position**](set-local-position.md)
* [**Get Local Position**](get-local-position.md)
* [**Get Local Rotation**](get-local-rotation.md)
