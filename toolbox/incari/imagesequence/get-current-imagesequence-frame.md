# Overview

![The Get Current Imagesequence Frame Node.](../../../.gitbook/assets/incari/imagesequence/GetCurrentImageSequenceFrame.PNG)

**Get Current Imagesequence Frame** returns the current frame number of an **ImageSequence** **Object**.

# Attributes
## Object

|Attribute|Type|Description|
|---|---|---|
|`Object`|**ObjectID**|The **ImageSequence** **Object** you wish to return the current frame from if one is not provided in the `Object ID` **Input** **Socket**.|

# Inputs

|Input|Type|Description|
|---|---|---|
|*Pulse Input* (►)|**Pulse**|A standard **Input Pulse**, to trigger the execution of the **Node**.|
|`Object ID`|**ObjectID**|The **ImageSequence** **Object** you wish to return the current frame from.|

# Outputs

|Output|Type|Description|
|---|---|---|
|*Pulse Output* (►)|**Pulse**|A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution.|
|`Frame No.`|**Int**|The frame number returned from the **ImageSequence** **Object**.|

# See Also
[**Get ImageSequence Duration**](get-imagesequence-duration.md)

[**Get ImageSequence FPS**](get-imagesequence-fps.md)

