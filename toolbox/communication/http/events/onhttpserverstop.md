# On HTTP Server Stop

## Overview

![The On HTTP Server Stop Node.](../../../../.gitbook/assets/onhttpserverstopupdatedimage.png)

**On HTTP Server Stop** is an **Event Listener Node** allowing the user to perform an action once a connection to an **HTTP** server has been terminated.

[**Scope**](../../overview.md#scopes): **Project**, **Scene**.

## Attributes

![The On HTTP Server Stop Node Attributes.](../../../../.gitbook/assets/onhttpserverstartattributes.png)

| Attribute | Type | Description |
| :--- | :--- | :--- |
| `Configuration` | **Drop-down** | The desired _HTTP(S)_ server, which refers back to the selections made under *HTTP* in the [**Project Settings**](../../../../modules/project-settings/http.md). |

## Outputs

| Output | Type | Description |
| :--- | :--- | :--- |
| _Pulse Output_ \(►\) | **Pulse** | A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution. |

## See Also

* [**On HTTP Server Start**](onhttpserverstart.md)

