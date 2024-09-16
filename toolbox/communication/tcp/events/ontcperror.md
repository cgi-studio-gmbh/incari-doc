# Overview

![The On TCP Error Node.](../../../../.gitbook/assets/ontcperrornode20241.png)

**On TCP Error** is an **Event Listener Node** that executes and triggers a **Logic Branch** when an **Error** in the connection occurs and returns the **Error** `Message`.

**TCP Communication** in **Incari** is available as a plugin and is enabled as default. However, in the case that it is disabled in the **Plugins Editor**, it will not appear in the **Project Settings** and **On TCP Error** will not show up in the [**Toolbox**](../../overview.md). Please refer to the [**Plugins Editor**](../../../../modules/plugins/communication/tcpconnectionsmanager.md) to find out more information.

[**Scope**](../../../overview.md#scopes): **Project**, **Scene**.

# Attributes

![The On TCP Error Node Attributes.](../../../../.gitbook/assets/ontcperrorattributes.png)

|Attribute|Type|Description|
|---|---|---|
|`Configuration`|**Drop-Down**|The desired _TCP_ server, which refers back to the selections made under *TCP* in the [**Project Settings**](../../../../modules/project-settings/tcp-connection.md).| 


# Outputs

|Output|Type|Description|
|---|---|---|
|*Pulse Output* (►)|**Pulse**|A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution.|
|`Message`|**String**|The returned **Error** `Message`.|




