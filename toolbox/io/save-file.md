# Overview

![The Save File Node.](../../.gitbook/assets/toolbox/io/SaveFile.PNG)

**Save File** Saves a file into the local system.

# Attributes

## File
|Attribute|Type|Description|
|---|---|---|
|`File's local path`|**String**|The local path you wish to save the file.|
|`Overwrite file if exits`|**Bool**|A previously saved file will be overwritten if the toggle is switched on otherwise it will not.|

# Inputs

|Input|Type|Description|
|---|---|---|
|*Pulse Input* (►)|**Pulse**|A standard **Input Pulse**, to trigger the execution of the **Node**.|
|`Content`|**String**|Content you wish to save into a file.|

# Outputs

|Output|Type|Description|
|---|---|---|
|*Pulse Output* (►)|**Pulse**|A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution.|

# See Also
[**Load File**](load-file.md)

