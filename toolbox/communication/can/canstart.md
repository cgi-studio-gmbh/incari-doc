# CAN Start

## Overview

![The CAN Start Node.](../../../.gitbook/assets/canstartupdatedimage.png)

The **CAN Start Node** starts communication with a **CAN** connection that has already been set up in [**Project Settings**](../../../modules/project-settings.md#can).

[**Scope**](../overview.md#scopes): **Project**, **Scene**, **Function**, **Prefab**.

## Inputs

| Input | Type | Description |
| :--- | :--- | :--- |
| _Pulse Input_ \(►\) | **Pulse** | A standard **Input Pulse**, to trigger the execution of the **Node**. |

## Outputs

| Output | Type | Description |
| :--- | :--- | :--- |
| _Pulse Output_ \(►\) | **Pulse** | A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution. |

## See Also

* [**CAN Stop**](canstop.md)
* [**CAN Send Packet**](cansendpacket.md)

