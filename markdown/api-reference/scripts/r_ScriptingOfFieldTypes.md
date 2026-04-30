---
title: Script evaluation of fields by data type
description: Script fields evaluate data based on the field type of the input.
locale: en-US
release: zurich
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Scripting, API implementation, API implementation and reference]
---

# Script evaluation of fields by data type

Script fields evaluate data based on the field type of the input.

<table id="table_c1l_ycb_yq"><thead><tr><th>

Type

</th><th>

Evaluates to in script

</th><th>

Example

</th></tr></thead><tbody><tr><td>

String

</td><td>

The string

</td><td>

"dog" &gt; "dog"

</td></tr><tr><td>

Decimal

</td><td>

A number with up to two decimal points

</td><td>

12.34 &gt; 12.34

</td></tr><tr><td>

Integer

</td><td>

A number with zero decimal points

</td><td>

12 &gt; 12

</td></tr><tr><td>

True / False

</td><td>

true or false

</td><td>

![The true icon](../image/CheckOn.png) &gt; true

 ![The false icon](../image/CheckOff.png) &gt; false

</td></tr><tr><td>

Date

</td><td>

A date formatted as yyyy-mm-dd

</td><td>

2008-11-04

</td></tr><tr><td>

Date-time

</td><td>

A day and time formatted as yyyy-mm-dd hh:mm:ss

</td><td>

2008-11-04 06:46:20

</td></tr><tr><td>

Duration

</td><td>

A date that is equal to January 1st 1970 00:00:00 + the amount of time of the duration being stored

 **Note:** This date corresponds to the system time zone. If a different user time zone has been specified, the date and time value may appear different for that user.

</td><td>

![](../image/ZeroDuration.png) &gt; "1970-01-01 00:00:00"

 ![](../image/TestDuration.png) &gt; "1970-01-02 02:03:04"

</td></tr><tr><td>

Choice

</td><td>

Returns the contents of the value field for the `sys_choice` record associated with that choice. See: Choice List for more information on returning the value associated with a particular item in a choice list.

</td><td>

![](../image/BasicSelect.png) &gt; "2" \(Note that this value is is a string\)

</td></tr><tr><td>

Journal

</td><td>

Returns a string of all entries made to that journal field. See Journal Fields for scripting of journal type fields

</td><td>

The web server is down &gt; The web server is down

</td></tr><tr><td>

Reference

</td><td>

Returns the `sys_id` of the record that is referenced

</td><td>

![](../image/Reference.png) &gt; "287ee6fea9fe198100ada7950d0b1b73"

</td></tr><tr><td>

Image

</td><td>

Returns the path to the image

</td><td>

![](../image/ImageFiletype.png) &gt; images/icons/image\_name.gif

</td></tr><tr><td>

URL

</td><td>

Returns a string

</td><td>

![](../image/URLExample.png) &gt; "http://www.service-now.com"

</td></tr><tr><td>

Glide Lists

</td><td>

Returns a string of comma-separated Sys IDs

</td><td>

![](../image/GlideListExample.png) &gt; 5137153cc611227c000bbd1bd8cd2007,46d14f04a9fe19810142e40c6b071512

</td></tr></tbody>
</table>**Parent Topic:**[Scripting](../../topic/c_Script.md)

