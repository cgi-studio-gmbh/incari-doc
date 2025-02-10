# Overview

![The Compare Node.](../../.gitbook/assets/comparenode20241.png)

The **Compare** **Node** compares two **Strings** and outputs the result indicating whether they are equal or not in two forms: an **Int** and a **Bool**.

[**Scope**](../overview.md#scopes): **Project**, **Scene**, **Function**, **Prefab**.

# Attributes

![The Compare Node Attributes.](../../.gitbook/assets/compareattributes.png)


|Attribute|Type|Description|
|---|---|---|
| `String 1` | **String** | The default value of the first **String** to be compared, if none is given in the `String 1` **Socket**. |
| `String 2` | **String** | The default value of the second **String** to be compared, if none is given in the `String 2` **Socket**.|



# Inputs

|Input|Type|Description|
|---|---|---|
|*Pulse Input* (►)|**Pulse**|A standard **Input Pulse**, to trigger the execution of the **Node**.|
| `String 1` | **String** | The first **String** to be compared. |
| `String 2` | **String** | The second **String** to be compared. |

# Outputs

|Output|Type|Description|
|---|---|---|
|*Pulse Output* (►)|**Pulse**|A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution.|
| `Result` | **Int** | 0, if the **Strings** are equal; -1, if they are not.  |
| `Equal` | **Bool** | *True*, if the **Strings** are equal; *false*, if they are not.|


# See Also

* [**String Value**](stringvalue.md)