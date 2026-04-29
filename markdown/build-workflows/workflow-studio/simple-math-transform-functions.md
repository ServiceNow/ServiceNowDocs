---
title: Simple math transform functions
description: Use simple math transform functions to perform basic mathematical calculations on Number data pills.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Transform functions, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Simple math transform functions

Use simple math transform functions to perform basic mathematical calculations on Number data pills.

Simple math transform functions require an Array.Number, Array.Integer, or Array.Decimal input data pill. Make sure to use the correct input [data pill type](action-inputs-outputs.md) when applying simple math transform functions. If a simple math transform function is applied to an improper data type, the data is not transformed at runtime and the input value is returned instead. For more information on confirming your flow runtime values, see [Test a flow](../task/flow-test.md).

## Absolute Value

A mathematical function that returns the distance from zero for any real number. An absolute value is always a positive or zero value.

|Input data pill|Output data pill|
|---------------|----------------|
|Number, Integer, or Decimal|Number as the absolute value of the input number|

-   Input: `-3`
-   Output: `3`

## Add

Adds the given value to the input.

|Input data pill|Parameters|Output data pill|
|---------------|----------|----------------|
|Number, Integer, or Decimal|Number to be added.|Number as the addition of the input value by the parameter.|

-   Input: `12`
-   Parameter: `4`
-   Output: `16`

## Average

Returns the average value of the elements in the input array.

|Input data pill|Output data pill|
|---------------|----------------|
|Array.Number, Array.Integer, or Array.Decimal|Number as the average value of the input array.|

-   Input: `[10, 30, 20]`
-   Output: `20`

## Count

Returns the number of elements in the input array.

|Input data pill|Output data pill|
|---------------|----------------|
|Array.Number, Array.Integer, Array.Decimal, Array.Object, Array.String, or Array.Boolean|Number of elements in the input array|

-   Input: `[2, 10, 30]`
-   Output: `3`

## Divide

Divides the input value by a given value.

|Input data pill|Parameters|Output data pill|
|---------------|----------|----------------|
|Number, Integer, or Decimal|Number to divide the input value by.|Number as the division of the input value by the parameter.|

-   Input: `12`
-   Parameter: `4`
-   Output: `3`

## Max

Returns the highest value found in the input Array.

|Input data pill|Output data pill|
|---------------|----------------|
|Array.Number, Array.Integer, or Array.Decimal|Number as the highest value in the input Array|

-   Input: `[1, -5, 20, 6]`
-   Output: `20`

## Median

Returns the median value of elements in the input array.

|Input data pill|Output data pill|
|---------------|----------------|
|Array.Number, Array.Integer, or Array.Decimal|Number as the median value of the input array.|

-   Input: `[10, 30, 15]`
-   Output: `15`

## Min

Returns the lowest value found in the input Array.

|Input data pill|Output data pill|
|---------------|----------------|
|Array.Number, Array.Integer, or Array.Decimal|Number as the lowest value in the input Array|

-   Input: `[1, -5, 20, 6]`
-   Output: `-5`

## Multiply

Multiplies the input value by a given value.

|Input data pill|Parameters|Output data pill|
|---------------|----------|----------------|
|Number, Integer, or Decimal|Number to be multiplied.|Number as multiplication of the input value by the parameter.|

-   Input: `12`
-   Parameter: `4`
-   Output: `48`

## Power

Returns the value of the input value raised to the power of a given value.

|Input data pill|Parameters|Output data pill|
|---------------|----------|----------------|
|Number, Integer, or Decimal|Number as the exponent of the power.|Number as the power of input value to the parameter.|

-   Input: `2`
-   Parameter: `3`
-   Output: `8`

## Round

A mathematical function that approximates a numeric value based on rounding rules and a digit position. The function rounds up by adding one to the digit to be rounded and then replacing all digits to its right with zeroes.

|Input data pill|Parameters|Output data pill|
|---------------|----------|----------------|
|Number, Integer, or Decimal|**Number of Digits** - A positive integer specifying the position of the digit to be rounded starting on the left|Number as the rounded value of the input number|

-   Input: `194`
-   Parameter: `2`
-   Output: `190`

**Note:** The function uses the digit to the right of the parameter digit to round up or down. If the digit to the right has a value from zero through four, the function rounds down. If the digit to the right has a value from five through nine, then the function rounds up. If there is no digit to the right, then the function rounds down.

## Square Root

A mathematical function that computes a positive number that when multiplied by itself produces the input value. The input value must be a positive real number.

|Input data pill|Output data pill|
|---------------|----------------|
|Number, Integer, or Decimal|Number as the square root of the input number|

-   Input: `16`
-   Output: `4`

## Subtract

Subtracts the given value from the input.

|Input data pill|Parameters|Output data pill|
|---------------|----------|----------------|
|Number, Integer, or Decimal|Number to subtract from the input value.|Number as the subtraction of the input value by the parameter.|

-   Input: `12`
-   Parameter: `4`
-   Output: `8`

## Sum

Returns the sum of all values in the input Array.

|Input data pill|Output data pill|
|---------------|----------------|
|Array.Number, Array.Integer, or Array.Decimal|Number as a sum of all values in the input Array|

-   Input: `[1, -5, 20, 6]`
-   Output: `22`

## To Fixed

Truncates a floating number to the specified number of decimal places.

|Input data pill|Parameter|Output data pill|
|---------------|---------|----------------|
|Number - Decimal number before truncation.|Number of Digits - Number that specifies the number of decimal places to truncate.|Number - Decimal number after truncation.|

-   Input: `1.93456`
-   Parameter: `2`
-   Output: `1.93`

**Parent Topic:**[Transform functions](../concept/transform-functions.md)

