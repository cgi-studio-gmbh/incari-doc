# Overview

![The On TCP Stop Node.](../../../../.gitbook/assets/ontcpstop.png)

**On TCP Stop** is an **Event Listener Node** allowing the user to trigger a **Logic Branch** once a connection to a **TCP** server has been terminated.

**TCP Communication** in **Incari** is available as a plugin and is enabled as default. However, in the case that it is disabled in the **Plugins Editor**, it will not appear in the **Project Settings** and **On TCP Stop** will not show up in the [**Toolbox**](../../overview.md). Please refer to the [**Plugins Editor**](../../../modules/plugins/README.md) to find out more information.

[**Scope**](../../overview.md#scopes): **Project**, **Scene**.

# Attributes

![The On TCP Stop Node Attributes.](../../../../.gitbook/assets/ontcpstopatts.png)

|Attribute|Type|Description|
|---|---|---|
|`Configuration`|**Drop-Down**|The desired _TCP_ server, which refers back to the selections made under *TCP* in the [**Project Settings**](../../../modules/project-settings.md).| 


# Outputs

|Output|Type|Description|
|---|---|---|
|*Pulse Output* (►)|**Pulse**|A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution.|

# See Also

* [**On TCP Start**](ontcpstart.md)