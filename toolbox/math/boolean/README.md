# Boolean

## Introduction

A **Boolean** is a **Data Type**, which represents one of two values: _true_ or _false_.

Although **Booleans** themselves are conceptually simple, and take up very little memory, they are an integral part of **Incari**'s **Logic** system, and computer programming in general, due to their use in **Flow Control**. More specifically, _Boolean expressions_ are used to define the conditions that determine which actions will be performed, dependending on whether they are evaluated as being _true_ or _false_.

## Boolean Value

The [**Bool Value Node**](bool-value.md) simply stores a **Boolean** value in its internal _state_, which can be defined before the **Project**'s execution and can be modified and retrieved at runtime.

## Logical Operator Nodes

_Logical operator_ **Nodes** combine two or more **Boolean** expressions to yield a **Boolean** value based on the inputs' logical relationship to one another. These are:

* [**AND**](and.md) - Returns _true_ if all of the **Node**'s inputs are also _true_. The equivalent of the `&&` operator in computer programming.
* [**OR**](or.md) - Returns _true_ if at least one of the **Node**'s inputs are _true_. The equivalent of the `||` operator in computer programming.

There is also the [**Negate Node**](negate.md), whose output is simply the **Boolean** value _opposite_ to its input. This is used to mean _NOT_ and is the equivalent of the `!` operator in computer programming.

## Contents

* [**AND**](and.md)
* [**Bool Value**](bool-value.mde)
* [**Negate**](negate.md)
* [**OR**](or.md)

## External Links

* [_Logical operation_](https://www.computerhope.com/jargon/l/logioper.htm) on Computer Hope.
