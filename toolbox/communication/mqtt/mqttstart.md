# MQTT Start

## Overview

![The MQTT Start Node.](../../../.gitbook/assets/mqttstartupdatedimage.png)

The **MQTT Start Node** starts a **MQTT** connection that has already been set up in [**Project Settings**](../../../modules/project-settings.md#mqtt).

[**Scope**](../overview.md#scopes): **Project**, **Scene**.

## Attributes

![The MQTT Start Node Attributes.](../../../.gitbook/assets/mqttstartattributes.png)

| Attribute | Type | Description |
| :--- | :--- | :--- |
| `Configuration` | **Drop-down** | The connection, or signal name, that will be used. |

## Inputs

| Input | Type | Description |
| :--- | :--- | :--- |
| _Pulse Input_ \(►\) | **Pulse** | A standard **Input Pulse**, to trigger the execution of the **Node**. |

## Outputs

| Output | Type | Description |
| :--- | :--- | :--- |
| _Pulse Output_ \(►\) | **Pulse** | A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution. |

## See Also

* [**MQTT Stop**](mqttstop.md)
* [**MQTT Subscribe**](mqttsubscribe.md)
* [**MQTT Publish**](mqttpublish.md)

