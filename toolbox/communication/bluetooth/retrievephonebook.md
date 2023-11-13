

# Overview

![The Retrieve Phonebook Node.](../../../.gitbook/assets/retrievephonebooknode.png)

The **Retrieve Phonebook Node** returns a device's phonebook, speed dial, and favorites. These are presented in **Dictionary** form with the keys `Contacts`, `SpeedDialContacts`, and `FavoriteContacts`.

**Bluetooth Communication** in **Incari** is available as a plugin and is enabled as default. However, in the case that it is disabled in the **Plugins Editor**, it will not appear in the **Project Settings** and **Retrieve Phonebook** will not show up in the [**Toolbox**](../../overview.md). Please refer to the [**Plugins Editor**](../../../modules/plugins/README.md) to find out more information.

[**Scope**](../../overview.md#scopes): **Project**, **Scene**.


# Inputs

|Input|Type|Description|
|---|---|---|
|*Pulse Input* (►)|**Pulse**|A standard **Input Pulse**, to trigger the execution of the **Node**.|
|`Bluetooth Address`|**String**|The unique *Bluetooth* identifier that is associated with a *Bluetooth* device.|

# Outputs

|Output|Type|Description|
|---|---|---|
|*Pulse Output* (►)|**Pulse**|A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution.|
|`On Finished`(►)|**Pulse**|An **Event Pulse** which is triggered if the phonebook was successfully retrieved.|
|`Phonebook`|**Dictionary**|The **Dictionary** containing the device's phonebook.|
|`Finished Bluetooth Address`|**String**|The **Bluetooth** address of the device.|
|`On Error`(►)|**Pulse**|An **Event Pulse** that fires in the event of an error, namely that the retrieval of the phonebook was unsuccessful.|
|`Error Message`|**String**|The error message in the event of an error.|
|`Error Bluetooth Address`|**String**|The *Bluetooth* address associated with the error.|