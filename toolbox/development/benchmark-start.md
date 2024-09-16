# Benchmark Start

## Overview

![The Benchmark Start Node.](../../.gitbook/assets/benchmarkstartnode20241.png)

The **Benchmark Start** **Node** starts a timer with a name given in the **Attributes**.

[**Scope**](../overview.md#scopes): **Project**, **Scene**, **Function**, **Prefab**.

## Attributes

![The Benchmark Start Node Attributes.](../../.gitbook/assets/benchmarkstartattributes.png)

| Attribute | Type | Description |
| :--- | :--- | :--- |
| `Timer Name` | **String** | Name of the timer. |

## Inputs

| Input | Type | Description |
| :--- | :--- | :--- |
| _Pulse Input_ \(►\) | **Pulse** | A standard **Input Pulse**, to trigger the execution of the **Node**. |

## Outputs

| Output | Type | Description |
| :--- | :--- | :--- |
| _Pulse Output_ \(►\) | **Pulse** | A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution. |

## See Also

* [**Benchmark Get**](benchmark-get.md)
* [**Benchmark Stop**](benchmark-stop.md)

