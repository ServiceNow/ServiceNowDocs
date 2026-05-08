---
title: Input data types in Virtual Agent topics
description: You can define inputs of commonly used Glide Virtual Agent \(com.glide.cs.chatbot\) data types in Assistant Designer without writing a script. Define the input data type on the Start node of a custom control or topic block.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Virtual Agent technical reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Input data types in Virtual Agent topics

You can define inputs of commonly used Glide Virtual Agent \(com.glide.cs.chatbot\) data types in Assistant Designer without writing a script. Define the input data type on the Start node of a custom control or topic block.

## Data types in Assistant Designer

The data type designation allows Virtual Agent to perform secondary validation on NLU predicted values. For example, if your choice list has red, white, and blue, but the NLU prediction service returns green, the input won't be slot-filled because that wasn't a valid choice.

When you specify an input with a data type on a calling topic, you can use the data pill picker to specify information collected from the user or previously looked up in a custom control or topic block.

<table id="table_w53_vk3_bpb"><thead><tr><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Alphanumeric text. The value uses JavaScript data conventions.

</td></tr><tr><td>

Boolean

</td><td>

Boolean value of true or false \(yes or no\).

</td></tr><tr><td>

Reference

</td><td>

Table record by sys\_id.Select a ServiceNow table in the **Table** field. You can define conditions for the returned record.

</td></tr><tr><td>

Date/Time

</td><td>

Date and time values.

</td></tr><tr><td>

Array.String

</td><td>

Sequence of alphanumeric text values.To limit the number of strings that authors can specify, use the **Max Number of Rows** field.

</td></tr><tr><td>

Array.Datetime

</td><td>

Sequence of date and time values.To limit the number of dates that authors can specify, use the **Max Number of Rows** field. Click **+** to specify more than one default value.

</td></tr><tr><td>

Array.Reference

</td><td>

Sequence of table records by sys\_id. Select a ServiceNow table in the **Table** field. You can define conditions for the returned record.

 To limit the number of records that authors can specify, use the **Max Number of Rows** field.

 **Note:** The **Array.Reference** input data type in Virtual Agent Designer corresponds to the **List.\[Table\]** input data type in Workflow Studio. For more information, see Action input and output data types.

</td></tr><tr><td>

Array.Choice

</td><td>

Sequence of choice list values for a specific choice field.For example, `printer`, `computer`, and `monitor`.

</td></tr></tbody>
</table>**Note:** Duplicate default values are not allowed with array data types.

## Example data type definition

This User Name Array.Reference input variable limits the number of records to 5. It references the sys\_user table with the condition that all names must start with **a**.

![Edit input window, showing data type definition inAssistant Designer.](../images/va-data-type-definition.png)

**Parent Topic:**[Virtual Agent technical reference](../concept/va-advanced-technical-reference.md)

**Related topics**  


[Domain separation and Virtual Agent](../concept/domain-separation-virtual-agent.md)

[Virtual Agent interaction records](../concept/va-interactions.md)

[Virtual Agent scripts](../concept/virtual-agent-scripts.md)

[NLU system entities](nlu-system-entities.md)

[Virtual Agent URL parameters](va-sysparm.md)

[Latency feedback in Virtual Agent](latency-feedback.md)

