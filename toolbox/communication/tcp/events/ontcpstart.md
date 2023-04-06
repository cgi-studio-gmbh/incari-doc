# Overview

![The On TCP Start Node.](../../../../.gitbook/assets/ontcpstart.png)

**On TCP Start** is an **Event Listener Node** notifying that the **TCP** connection was successfully established, therefore enabling the user to trigger a **Logic Branch** on said connection to the *TCP* server.

**SocketIO Communication** in **Incari** is available as a plugin and is enabled as default. However, in the case that it is disabled in the **Plugins Editor**, it will not appear in the **Project Settings** and **On TCP Start** will not show up in the [**Toolbox**](../../overview.md). Please refer to the [**Plugins Editor**](../../../../modules/plugins/communication/tcpconnectionsmanager.md) to find out more information..

[**Scope**](../../../overview.md#scopes): **Project**, **Scene**.

# Attributes

![The ON TCP Start Node Attributes.](../../../../.gitbook/assets/ontcpstartatts.png)

|Attribute|Type|Description|
|---|---|---|
|`Configuration`|**Drop-Down**|The desired _TCP_ server, which refers back to the selections made under *TCP* in the [**Project Settings**](../../../../modules/project-settings/tcp-connection.md).| 

# Outputs

|Output|Type|Description|
|---|---|---|
|*Pulse Output* (►)|**Pulse**|A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution.|

# See Also

* [**On TCP Stop**](ontcpstop.md)


