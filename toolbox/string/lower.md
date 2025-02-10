# Overview

![The Lower Node.](../../.gitbook/assets/lowernode20241.png)

The **Lower** **Node** converts a **String** to lowercase letters.

[**Scope**](../overview.md#scopes): **Project**, **Scene**, **Function**, **Prefab**.

# Attributes

![The Lower Node Attributes.](../../.gitbook/assets/lowerattributes.png)

|Attribute|Type|Description|
|---|---|---|
| `String` | **String** | The **String** to be converted to lowercase, if none is received in the **Input Socket**.|

# Inputs

|Input|Type|Description|
|---|---|---|
|*Pulse Input* (►)|**Pulse**|A standard **Input Pulse**, to trigger the execution of the **Node**.|
| `String` | **String** | The **String** to be converted to lowercase. |

# Outputs

|Output|Type|Description|
|---|---|---|
|*Pulse Output* (►)|**Pulse**|A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution.|
| `Result` | **String** | The **String** converted to lowercase. |


# See Also

* [**Upper**](upper.md)
