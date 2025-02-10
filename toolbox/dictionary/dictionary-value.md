# Dictionary Value

## Overview

![The Dictionary Value Node.](../../.gitbook/assets/dictionaryvaluenode20241.png)

The **Dictionary Value Node** defines a **Dictionary** by setting its _\(key, value\)_ pairings.

[**Scope**](../overview.md#scopes): **Project**, **Scene**, **Function**, **Prefab**.

## Attributes

![The Dictionary Value Node Attributes.](../../.gitbook/assets/dictionaryvalueattributeupdate.png)


`Inputs` - The number of **Input** elements you wish to add to the **Attribute section**. Each **Input** element represents a _\(key, value\)_ pair that is added to the **Dictionary Value** **Node**. The pairs in this section are used if no **Dictionary** is provided to the **Input** **Node**. The format of the section is the following:

| Attribute | Type | Description |
| :--- | :--- | :--- |
| `Key` | **String** | The `Key` you wish to add to the **Dictionary Value** **Node**. |
| `Value Type` | **Drop-down** | The `Data Type` of the `Value` you wish to add to the **Dictionary Value** **Node**. |
| `Value` | _Defined in the_ `Data Type` _**Attribute**_. | The `Value` you wish to give to the `Key` introduced above. |

## Inputs

| Input | Type | Description |
| :--- | :--- | :--- |
| _Pulse Input_ \(►\) | **Pulse** | A standard **Input Pulse**, to trigger the execution of the **Node**. |
| `Input` | **Dictionary** | A **Dictionary** you wish to add to the **Dictionary Value** **Node**. |

## Outputs

| Output | Type | Description |
| :--- | :--- | :--- |
| _Pulse Output_ \(►\) | **Pulse** | A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution. |
| `Output` | **Dictionary** | The **Dictionary** holding the \(`Key`, `Value`\) pairs that were added to the **Dictionary Value** **Node**. |

## See Also

* [**Clear Dictionary**](clear-dictionary.md)

## External Links

* [Fundamentals of data structures: Dictionaries](https://en.wikibooks.org/wiki/A-level_Computing/AQA/Paper_1/Fundamentals_of_data_structures/Dictionaries) on Wikibooks.
* [Associative Array](https://en.wikipedia.org/wiki/Associative_array) on Wikipedia.

