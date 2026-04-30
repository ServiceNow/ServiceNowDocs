---
title: StringBuilder connector methods
description: The StringBuilder connector methods enable you to create, append, update, replace, or remove strings in your automation workflow in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [StringBuilder, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# StringBuilder connector methods

The StringBuilder connector methods enable you to create, append, update, replace, or remove strings in your automation workflow in RPA Desktop Design Studio.

## Append

Adds string to an existing string. You can create multiple strings by using multiple copies of the method. To view the output, use the ToString method.

**Note:** The method doesn't insert a line between the strings.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Parameter name

</th><th>

Description

</th><th>

Data Port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

Value

</td><td>

The string to be appended to the existing content.-   **Example**

Existing string: "Hello"

Value: " World!"

Output: Hello World!


</td><td>

Data In

</td><td>

String

</td></tr></tbody>
</table>## AppendLine

Adds a string followed by a newline character \(\\n\) automatically. When you add multiple strings using multiple copies of the method, it inserts a line between the strings. It functions exactly like the **Enter** key on a Microsoft Word document. To view the output, use the ToString method.

<table id="table_k3r_mks_32c"><thead><tr><th>

Parameter name

</th><th>

Description

</th><th>

Data Port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

Value

</td><td>

String to append followed by a line break.-   **Example**

Existing string: "Hello"

Value: "World!"

Output: Hello

World!


</td><td>

Data In

</td><td>

String

</td></tr></tbody>
</table>## Replace

Replaces a string with a string that you specify in both the Append and AppendLine methods.

<table id="table_t4x_mks_32c"><thead><tr><th>

Parameter name

</th><th>

Description

</th><th>

Data Port type

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

OldValue

</td><td>

Existing string that is replaced with a string specified in the **NewValue** field.-   **Example**

OldValue: User


</td><td>

Data In

</td><td>

String

</td></tr><tr><td>

NewValue

</td><td>

String that replaces the **OldValue** string.-   **Example**

NewValue: Abel Tutor


</td><td>

Data In

</td><td>

String

</td></tr></tbody>
</table>## Clear

Clears the string content in the methods.

## ToString

Returns the output of the Append and AppendLine methods.

|Parameter name|Description|Data Port type|Data type|
|--------------|-----------|--------------|---------|
|Return|Output that is returned after the execution of the Append and AppendLine methods. For examples, see Append and AppendLine parameters.|Data Out|String|

## Configure inputs for the parameters

To enter inputs for parameters, see [Configure port properties](../task/configure-input-port-properties.md).

**Parent Topic:**[StringBuilder](../concept/stringbuilder-connector.md)

