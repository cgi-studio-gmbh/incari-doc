# Overview

![The Load File Node.](../../.gitbook/assets/toolbox/io/LoadFile.PNG)

**Load File** loads a file from the local system into Incari.

# Attributes
## File

|Attribute|Type|Description|
|---|---|---|
|`File`|**ObjectID**|The File you wish to load into Incari.

# Inputs

|Input|Type|Description|
|---|---|---|
|*Pulse Input* (►)|**Pulse**|A standard **Input Pulse**, to trigger the execution of the **Node**.|

# Outputs

|Output|Type|Description|
|---|---|---|
|*Pulse Output* (►)|**Pulse**|A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution.|
|`Content`|**String**|Loaded file content.

# See Also
[**Save File**](save-file.md)

