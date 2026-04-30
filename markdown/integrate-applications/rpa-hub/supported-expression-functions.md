---
title: Supported functions for the Expression components
description: Learn about the various functions for the Expression components in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [General, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Supported functions for the Expression components

Learn about the various functions for the Expression components in RPA Desktop Design Studio.

|Name|Description|Usage|Result|
|----|-----------|-----|------|
|Abs|Returns the absolute value of a specified number.|Abs|1|
|Acos|Returns the angle whose cosine is the specified number.|Acos|\(1\)|
|Asin|Returns the angle whose sine is the specified number.|Asin\(0\)|0|
|Atan|Returns the angle whose tangent is the specified number.|Atan\(0\)|0|
|Ceiling|Returns the smallest integer that is greater than or equal to the specified number.|Ceiling\(1.5\)|2|
|Cos|Returns the cosine of the specified angle.|Cos\(0\)|1|
|Exp|Returns raised to the specified power.|Exp\(0\)|1|
|Floor|Returns the largest integer less than or equal to the specified number.|Floor\(1.5\)|1|
|IEEERemainder|Returns the remainder resulting from the division of a specified number by another specified number.|IEEERemainder\(3, 2\)|-1|
|Log|Returns the logarithm of a specified number.|Log\(1, 10\)|0|
|Log10|Returns the base 10 logarithm of a specified number.|Log10\(1\)|0|
|Max|Returns the larger of two specified numbers.|Max\(1, 2\)|2|
|Min|Returns the smaller of two numbers.|Min\(1, 2\)|1|
|Pow|Returns a specified number raised to the specified power.|Pow\(3, 2\)|9|
|Round|Rounds a value to the nearest integer or specified number of decimal places. The mid number behavior can be changed by using EvaluateOption.RoundAwayFromZero during the construction of the Expression object.|Round\(3.222, 2\)|3.22|
|Sign|Returns a value indicating the sign of a number.|Sign\(-10\)|-1|
|Sin|Returns the sine of the specified angle.|Sin\(0\)|0|
|Sqrt|Returns the square root of a specified number.|Sqrt\(4\)|2|
|Tan|Returns the tangent of the specified angle.|Tan\(0\)|0|
|Truncate|Calculates the integral part of a number.|Truncate\(1.7\)|1|
|NCalc|The NCalc is a mathematical expressions evaluator in .NET. With this function, you can parse any expression and evaluate its result. This includes static or dynamic parameters, or custom functions.|For more information, see [https://github.com/ncalc/ncalc/wiki](https://github.com/ncalc/ncalc/wiki)| |

**Parent Topic:**[General](../concept/general-component.md)

