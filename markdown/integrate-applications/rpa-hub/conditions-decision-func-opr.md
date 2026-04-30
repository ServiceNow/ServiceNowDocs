---
title: Functions, data types, and operators
description: The Decision component supports certain functions and operators described in the topic. Use this topic as a reference.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Conditions, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Functions, data types, and operators

The Decision component supports certain functions and operators described in the topic. Use this topic as a reference.

## Supported functions and operators

<table id="table_vhj_ncl_ttb"><thead><tr><th>

Type

</th><th>

Example

</th><th>

Evaluated as

</th></tr></thead><tbody><tr><td>

Values

</td><td>

-   Integer
-   Floating point number
-   Date and time
-   Boolean
-   String
-   Function
-   Parameter

</td><td>

Not applicable

</td></tr><tr><td>

Integers

</td><td>

Represented using numbers. Example, 443, 124, and 665.

</td><td>

Int32

</td></tr><tr><td>

Floating point numbers

</td><td>

221.12, 43.76, and 5.9

</td><td>

Decimal

</td></tr><tr><td>

Scientific notation

</td><td>

You can use the e to define the power of 10 \(10^\).

-   1.22e1
-   1e2
-   1e+2
-   1e-2
-   .1e-2
-   1e10

</td><td>

Double

</td></tr><tr><td>

Dates and Times

</td><td>

Must be enclosed between `sharps`.

 \#2008/01/31\# // for en-US culture

</td><td>

DateTime

</td></tr><tr><td>

Boolean

</td><td>

True or False

</td><td>

Boolean

</td></tr><tr><td>

Strings

</td><td>

Any character between single quotes ' is evaluated as String.

</td><td>

'ServiceNow'

</td></tr><tr><td>

Parameters

</td><td>

A parameter as a name, and can be optionally contained inside brackets.

 2 + x, 2 + \[x\]

</td><td>

 

</td></tr><tr><td>

Function

</td><td>

A function is made of a name followed by braces, containing optionally any value as arguments. Abs\(1\), doSomehting\(1, 'dummy'\)

</td><td>

 

</td></tr><tr><td>

Operators

</td><td>

Expressions can be combined using operators. Each operator as a precedence priority. Here is the list of those expression's priority.1.  primary
2.  unary
3.  power
4.  multiplicative
5.  additive
6.  relational
7.  logical

</td><td>

 

</td></tr><tr><td>

Logical

</td><td>

These operators can do some logical comparison between other expressions:-   or - \|\|
-   and - &amp;&amp;
-   true or false

 The and operator has a higher priority than the or, thus in the example above, false and true are evaluated first.

</td><td>

 

</td></tr><tr><td>

Relational

</td><td>

Relational operators are used to compare values. These operators always result in a boolean value.-   =, ==, !=, &lt;&gt;
-   &lt;, &lt;=, &gt;, &gt;=
-   1 &lt; 2

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Conditions](../concept/conditions-components.md)

