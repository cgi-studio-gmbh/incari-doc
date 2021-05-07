# Overview

![The Get Imagesequence Duration Node.](../../../.gitbook/assets/incari/imagesequence/GetImageSequenceDuration.PNG)

**Get ImageSequence Duration** returns the duration in seconds it takes to play an **ImageSequence** **Object** from start to finish.

# Attributes
## Object

|Attribute|Type|Description|
|---|---|---|
|`Object`|**ObjectID**|The **ImageSequence** **Object** whose duration you wish to return, if one is not provided in the `Object ID` **Input** **Socket**.|

# Inputs

|Input|Type|Description|
|---|---|---|
|*Pulse Input* (►)|**Pulse**|A standard **Input Pulse**, to trigger the execution of the **Node**.|
|`Object ID`|**ObjectID**|The **ImageSequence** **Object** whose `Duration` you wish to return.|


# Outputs

|Output|Type|Description|
|---|---|---|
|*Pulse Output* (►)|**Pulse**|A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution.|
|`Duration`|**Float**|The `Duration` of an **ImageSequence** **Object**.|

# See Also
[**Get Current ImageSequence Frame**](get-current-imagesequence-frame.md)

[**Get ImageSequence FPS**](get-imagesequence-fps.md)

