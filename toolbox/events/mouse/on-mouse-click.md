# On Mouse Click

## Overview

![The On Mouse Click Node with Object base.](../../../.gitbook/assets/node-on-mouse-click-objbase.png)

![The On Mouse Click Node with Screen base.](../../../.gitbook/assets/node-on-mouse-click-evbase.png)

**On Mouse Click** is an **Event Listener** **Node** used for executing a **Logic Branch** when there is a mouse click, either on a particular **Object** or anywhere in the **Screen**. 

The **Attributes** allow the user to choose which mouse button will trigger the **Event** and whether the `Event Base` is a specific **Object** or the entire **Screen**.

[**Scope**](../../overview.md#scopes): **Scene**, **Prefab**.

## Attributes

![The On Mouse Click Node Attributes.](../../../.gitbook/assets/node-on-mouse-click-attri.png)

### Button

| Attribute | Type | Description |
| :--- | :--- | :--- |
| `Mouse Button` | **Drop-down** | Whether the left, middle, or right button of the mouse will trigger the **Logic**. |

### Event Base

| Attribute | Type | Description |
| :--- | :--- | :--- |
| `Event Base` | **Drop-down** | Whether the **Logic** will be triggered when there is a mouse click on a particular **Object** or anywhere in the **Screen**.  |

## Inputs

Note: **Input Sockets** only available when `Event Base` is set to `Object`.

| Attribute | Type | Description |
| :--- | :--- | :--- |
| `Object ID` | **ObjectID** | The **Object** in which a click triggers the **Logic Branch**. |
| `Subscribe` (►)|**Pulse** | An **Input Pulse** that needs to be triggered to start listening to the **Event**. |



## Outputs

| Output | Type | Description |
| :--- | :--- | :--- |
| _Pulse Output_ \(►\) | **Pulse** | A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution. |
| `IsLongClick` | **Bool** | _True_ when the button is pressed longer than usual. |
| `Object ID` | **ObjectID** | The **Object ID** of the **Object** that was clicked on. If there is no **Object** on that part of the **Screen**, the output is the **Object ID** `00000000-0000-0000-0000-000000000000`.  |
|`Event ID`| **ObjectID**| The ID of the current **Event**. This can be connected to the [**Unsubscribe Node**](../unsubscribe.md) to unsubscribe from the **Event**.|

## See Also

* [**Events**](../)
* [**Mouse**](./)

