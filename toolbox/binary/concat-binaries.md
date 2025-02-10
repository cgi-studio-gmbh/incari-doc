# Concat Binaries

## Overview

![The Concat Binaries Node.](../../.gitbook/assets/concatbinariesnode20241.png)

**Concat Binaries** merges two or more **Binary** numbers into a new one. The numbers to be merged are given as input to the **Node**.

[**Scope**](../overview.md#scopes): **Project**, **Scene**, **Function**, **Prefab**.

## Attributes

![The Concat Binaries Node Attributes.](../../.gitbook/assets/concatbinariesattributes.png)


| Attribute | Type | Description |
| :--- | :--- | :--- |
| `Input [n]` | **Binary** | The default value of the **Binary** number, if none is given in the **Input Socket**. |

## Inputs

| Input | Type | Description |
| :--- | :--- | :--- |
| _Pulse Input_ \(►\) | **Pulse** | A standard **Input Pulse**, to trigger the execution of the **Node**. |
| `Input [n]` | **Binary** | Two or more **Binary** numbers to be concatenated. |

## Outputs

| Output | Type | Description |
| :--- | :--- | :--- |
| _Pulse Output_ \(►\) | **Pulse** | A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution. |
| `Output` | **Binary** | The merged **Binary** number. |

