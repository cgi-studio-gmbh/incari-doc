# Arc Cosine

## Overview

![The Arc Cosine Node.](../../../.gitbook/assets/arccosineupdatedimage.png)

The **Arc Cosine Node** takes a single **Float** value and returns its _arccosine_, in degrees \(°\) or radians \(rad\)

[**Scope**](../../overview.md#scopes): **Project**, **Scene**, **Function**, **Prefab**.

## Attributes

![The Arc Cosine Node Attributes.](../../../.gitbook/assets/node-arc-cosine2-attr.png)


| Attribute | Type | Description |
| :--- | :--- | :--- |
| `Is Degree` | **Bool** | Determines whether the `Output` value is given in degrees \(°\) or radians \(rad\). |
| `Default Value` | **Float** | The default value of `Input`, if no value is provided in the `Input` **Socket**. |

## Inputs

| Input | Type | Description |
| :--- | :--- | :--- |
| _Pulse Input_ \(►\) | **Pulse** | A standard **Input Pulse**, to trigger the execution of the **Node**. |
| `Input` | **Float** | The value to calculate the _arccosine_ of. |

## Outputs

| Output | Type | Description |
| :--- | :--- | :--- |
| _Pulse Output_ \(►\) | **Pulse** | A standard **Output Pulse**, to move onto the next **Node** along the **Logic Branch**, once this **Node** has finished its execution. |
| `Output` | **Float** | The _arccosine_ of `Input`. |

## See Also

* [**Trigonometry**](./)
* [**Cosine**](cosine.md)
* [**Radian-Degree Converter**](radian-degree-converter.md)

## External Links

* [_Trigonometry_](https://www.khanacademy.org/math/trigonometry) on Kahn Academy.
* [_Sine, Cosine and Tangent_](https://www.mathsisfun.com/sine-cosine-tangent.html) on Maths is Fun.

