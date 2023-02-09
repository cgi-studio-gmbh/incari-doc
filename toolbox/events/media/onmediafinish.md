# On Media Finish

## Overview

![The On Media Finish Node.](../../../.gitbook/assets/onmediafinish.png)

**On Media Play** is an **Event Listener Node** that gives the user a way to perform an action once a media **Object** ends, such as repeating a **Video**. Media in **Incari** is either a **Video** or **Audio**. 

[**Scope**](../../overview.md#scopes): **Scene**, **Prefab**.


## Inputs

| Input | Type | Description |
|:---|:---|:---|
|`Object ID` | **ObjectID** | The media **Object** that triggers the **Logic Branch** on ending. |
| `Subscribe` (►)|**Pulse** | An **Input Pulse** that needs to be triggered to start listening to the **Event**. |



## Outputs

| Output | Type | Description |
| :--- | :--- | :--- |
| _Pulse Output_ \(►\) | **Pulse** | A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution. |
| `Object ID` | **ObjectID** | The media **Object** received as **Input**. |

## See Also

* [**On Media Play**](onmediaplay.md)
