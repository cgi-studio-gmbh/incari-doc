# Overview

![The Random Node.](../../.gitbook/assets/node-random.png)

The **Random** **Node** outputs a random number.

This **Node** can be set to three different **Modes** (**Advanced**, **Expert**, and **Standard**). Each of these **Modes** give different options for the generation and distribution of the random numbers generated.

# Attributes

## Advanced

### Generator

|Attribute|Type|Description|
|---|---|---|
| `Is deterministic` | **Bool** | |
| `Seed` | **Int** | |

### Distribution

|Attribute|Type|Description|
|---|---|---|
| `Distribution` | **Drop-down** | |
| `Data Type` | **Drop-down** | |
| `Minimum` | _Defined in the `Data Type` **Attribute**_ | |
| `Maximum` | _Defined in the `Data Type` **Attribute**_ | |

## Expert 

### Generator

|Attribute|Type|Description|
|---|---|---|
| `Generator` | **Drop-down** | |
| `Seed` | **Int** (*not available for non_deterministic*) | |

### Distribution

|Attribute|Type|Description|
|---|---|---|
| `Distribution` | **Drop-down** | |
| `Data Type` | **Drop-down** | |
| `Minimum` | _Defined in the `Data Type` **Attribute**_ | |
| `Maximum` | _Defined in the `Data Type` **Attribute**_ | |
## Standard

### Distribution

|Attribute|Type|Description|
|---|---|---|
| `Data Type` | **Drop-down** | |
| `Minimum` | _Defined in the `Data Type` **Attribute**_ | |
| `Maximum` | _Defined in the `Data Type` **Attribute**_ | |

# Inputs

|Input|Type|Description|
|---|---|---|
|*Pulse Input* (►)|**Pulse**|A standard **Input Pulse**, to trigger the execution of the **Node**.|

# Outputs

|Output|Type|Description|
|---|---|---|
|*Pulse Output* (►)|**Pulse**|A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution.|
| `Output` | _Defined in the `Data Type` **Attribute**_ | |

# See Also

# External Links

