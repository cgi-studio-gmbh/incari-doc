# Overview

![The Get Imagesequence Fps Node.](../../../.gitbook/assets/incari/imagesequence/GetImageSequenceFPS.PNG)

**Get ImageSequence FPS** returns the frame rate per second (FPS) of an **ImageSequence** **Object**. 

# Attributes
## Object

|Attribute|Type|Description|
|---|---|---|
|`Object`|**ObjectID**|The **ImageSequence** **Object** whose `FPS` you wish to return, if one is not provided in the `Object ID` **Input** **Socket**.|

# Inputs

|Input|Type|Description|
|---|---|---|
|*Pulse Input* (►)|**Pulse**|A standard **Input Pulse**, to trigger the execution of the **Node**.|
|`Object ID`|**ObjectID**|The **ImageSequence** **Object** whose `FPS` you wish to return.|

# Outputs

|Output|Type|Description|
|---|---|---|
|*Pulse Output* (►)|**Pulse**|A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution.|
|`FPS`|**Int**|The `FPS` of an **ImageSequence** **Object**.|

# See Also
[**Get Current ImageSequence Frame**](get-current-imagesequence-frame.md)

[**Get ImageSequence FPS**](get-imagesequence-fps.md)

