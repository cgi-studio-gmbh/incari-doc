# Seek Video

## Overview

![The Seek Video Node.](../../../.gitbook/assets/seekvideoupdatedimage.png)

The **Seek Video** **Node** can be used to move to a certain timeframe of a specified video by providing a variable for the `Frame Number`.

[**Scope**](../../overview.md#scopes): **Scene**, **Function**, **Prefab**.

## Attributes

![The Seek Video Node Attributes.](../../../.gitbook/assets/node-seek-video-attr.png)

| Attribute | Type | Description |
| :--- | :--- | :--- |
| `Object` | **ObjectID** | The target **Object**. |

## Inputs

| Input | Type | Description |
| :--- | :--- | :--- |
| _Pulse Input_ \(►\) | **Pulse** | A standard **Input Pulse**, to trigger the execution of the **Node**. |
| `Object ID` | **ObjectID** | The ID of the target **Object**. |
| `Frame Number` | **Int** | The timeframe of the video the user wishes to reference. |

## Outputs

| Output | Type | Description |
| :--- | :--- | :--- |
| _Pulse Output_ \(►\) | **Pulse** | A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution. |

## See Also

* [**Play Media**](../media/playmedia.md)
* [**Pause Media**](../media/pausemedia.md)
* [**Stop Media**](../media/stopmedia.md)
* [**Is Media Playing**](../media/ismediaplaying.md)

