# Overview

![The Serial Start Node.](../../../.gitbook/assets/serialstartupdatedimage.png)

The **Serial Start Node** starts a **Serial** connection that has already been set up in [**Project Settings**](../../../modules/project-settings.md#serial).

[**Scope**](../overview.md#scopes): **Project**, **Scene**, **Function**, **Prefab**.

# Attributes

![The Serial Start Node Attributes.](../../../.gitbook/assets/serialstartattributes.png)

|Attribute|Type|Description|
|---|---|---|
|`Configuration`|**Drop-down**|The desired **Serial** connection.|

# Inputs

|Input|Type|Description|
|---|---|---|
|*Pulse Input* (►)|**Pulse**|A standard **Input Pulse**, to trigger the execution of the **Node**.|

# Outputs

|Output|Type|Description|
|---|---|---|
|*Pulse Output* (►)|**Pulse**|A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution.|

# See Also

* [**Serial Send Packet**](serialsendpacket.md)
* [**Serial Stop**](serialstop.md)

