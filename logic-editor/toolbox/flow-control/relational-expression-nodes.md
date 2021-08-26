# Relational Expression Nodes

Relational expression nodes compare two values and yield a [**Boolean** ](../../data-types/bool.md)value based on the relationship of those inputs.

## IsEqual

### Overview

![The IsEqual node.](../../../.gitbook/assets/nodeisequal.png)

This node tests two values of the _same_ [**type**](../../data-types/) to see if they _equal_ or not; for example:

| Value 1 | Value 2 | IsEqual |
| :--- | :--- | :--- |
| 123 | 123 | True |
| Cat | Dog | False |
| False | False | True |
| Mr. Smith | Mr. Smyth | False |

A usage example would be to test if a user has provided the correct PIN, or if the current day is Sunday.

### Inputs

![The type can be specified from the drop-down menu in the Node attribute editor.](../../../.gitbook/assets/isequaltypes%20%281%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29.png)

The node takes two inputs of the _same_ [**type**](../../data-types/).

There are many types available, which are **Binary**, **Bool**, **Byte**, **CAN\_Packet**, **Float**, **Int**, **Matrix3x3**, **Matrix4x4**, **String**, **Variant**, **Vector2**, **Vector3**, **Vector4** and **Void.**

### Usage

![In this example, the IsEqual node checks if a person has a winning raffle ticket number.](../../../.gitbook/assets/isequalexample.png)

## IsGreaterEqual

### Overview

![The IsGreaterEqual node.](../../../.gitbook/assets/nodeisgreaterequal.png)

This node tests two values of the _same_ [**type**](../../data-types/) to see if one is greater than the other \_\_or not. There are two modes to the node:

* **IsGreater** - Returns _true_ if the first input value is _greater than_ the second.
* **IsGreaterEqual** - Returns _true_ if the first input value is _equal to_, or _greater than_ the second.

| Value 1 | Value 2 | IsGreaterEqual | IsGreater |
| :--- | :--- | :--- | :--- |
| 2018 | 2018 | True | False |
| 23 | 24 | False | False |
| 89.000001 | 89 | True | True |

### Inputs

![The type can be specified from the drop-down menu in the Node attribute editor.](../../../.gitbook/assets/isequaltypes%20%281%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29.png)

The node takes two inputs of the _same_ [**type**](../../data-types/).

Because the node compares the value of the inputs to equate their relation to each other, only numerical [**types**](../../data-types/) are available as inputs, which are **Byte**, **Float** and **Int**.

### Usage

![In this example, the IsGreaterEqual node is used to see if the current speed of a vehicle exceeds the speed limit.](../../../.gitbook/assets/isgreaterequalexample.png)

## IsLessEqual

### Overview

![The IsLessEqual node.](../../../.gitbook/assets/nodeislessequal.png)

This node tests two values of the _same_ [**type**](../../data-types/) to see if one is less than the other \_\_or not. There are two modes to the node:

* **IsLess** - Returns _true_ if the first input value is _less than_ the second.
* **IsLessEqual** - Returns _true_ if the first input value is _equal to_, or _less than_ the second.

| Value 1 | Value 2 | IsLessEqual | IsLess |
| :--- | :--- | :--- | :--- |
| 2018 | 2018 | True | False |
| 23 | 24 | True | True |
| 89.000001 | 89 | False | False |

A usage example would be to check if a tire's pressure drops below a certain amount.

### Inputs

![The type can be specified from the drop-down menu in the Node attribute editor.](../../../.gitbook/assets/isequaltypes%20%281%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%282%29%20%281%29.png)

The node takes two inputs of the _same_ [**type**](../../data-types/).

Because the node compares the value of the inputs to equate their relation to each other, only numerical [**types**](../../data-types/) are available as inputs, which are **Byte**, **Float** and **Int**.

### Usage

![In this example, the IsLessEqual node checks if a tire&apos;s value is below a certain value.](../../../.gitbook/assets/islessequalexample.png)

## Conclusion

Relational expressions alone aren't of much use, but when combined with other nodes they can form extremely complex logic and are an essential part of flow control.

