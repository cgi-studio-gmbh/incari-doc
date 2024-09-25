# Overview

![The Get Language Node.](../../.gitbook/assets/getlanguagenode.png)

The **Get Language Node** returns the current active language of the **Project**.

[**Scope**](../overview.md#scopes): **Project**, **Scene**, **Function**, **Prefab**.

# Inputs

|Input|Type|Description|
|---|---|---|
|*Pulse Input* (►)|**Pulse**|A standard **Input Pulse**, to trigger the execution of the **Node**.|

# Outputs

|Output|Type|Description|
|---|---|---|
|*Pulse Output* (►)|**Pulse**|A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution.|
|`Language`|**String**|The current language.|

# See Also

* [**Set Language**](setlanguage.md)
