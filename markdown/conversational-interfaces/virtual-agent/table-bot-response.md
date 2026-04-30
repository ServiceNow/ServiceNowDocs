---
title: Table bot response control
description: Use the Table bot response control in a Virtual Agent topic to display a bot response as a table.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-05-13"
reading_time_minutes: 3
breadcrumb: [Virtual Agent Designer bot responses, Virtual Agent Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Table bot response control

Use the Table bot response control in a Virtual Agent topic to display a bot response as a table.

Table bot responses enable users to see information in a more organized way.

For example, you can organize and display information such as the following:

-   Planned service changes
-   Company holidays
-   Contact information
-   Testing sites

Output tables can have between one and four columns and may include optional column headers. You can populate tables using the conditioner builder or scripts.

## Table bot response properties

<table id="table_vm3_4ry_hfc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

Name that identifies this Table bot response control node in the topic flow.

</td></tr><tr><td>

Populate this table by

</td><td>

Options for populating the table. Select one of the following:-   **Table**: Select the ServiceNow table that contains the data to be displayed.
-   **Script**: Enter code in the Define rows dialog box.

</td></tr><tr><td>

Table

</td><td>

The name of the table that contains the data.This field is available only when the **Table** option is selected.

</td></tr><tr><td>

Filter rows

</td><td>

Options for filtering the contents of the table. Choose one of the following:-   **Condition**: Specify a no-code condition statement using the condition builder. For more information, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).
-   **Script**: Enter a low-code script that specifies a condition.

 This field is available only when the **Table** option is selected.

</td></tr><tr><td>

No records response message

</td><td>

Message displayed if no records are found.

</td></tr><tr><td>

Show links for each record

</td><td>

Slide this toggle to activate links for each record in the output in your Virtual Agent conversation. The **Show links for each record** toggle is not available by default. It can be enabled by changing the value of the system property sn\_cs\_builder.table\_show\_links\_enabled to true.

</td></tr><tr><td class="sub-head" colspan="2">

Columns and rows

</td></tr><tr><td>

Columns \(left to right\)

</td><td>

Table columns that you want to display in the conversation. You can have up to 4 columns.-   **Field**: Select a field from the ServiceNow table to be displayed in the column.
-   **Display name**: Reflects the selected column name. Use the default name or change the name.

 This field is available only when the **Table** option is selected.

</td></tr><tr><td>

Sort rows by

</td><td>

Option for sorting returned rows by column. You can sort by one of the selected columns, or by a column not shown in the response to the user. Choose **Ascending** or **Descending** order for the sort.If you don't specify a sort order, rows are sorted by creation date in descending order. If you specify a different sort order, creation date is used as a secondary sort order.

 This field is available only when the **Table** option is selected.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td class="sub-head" colspan="2">

Headers

</td></tr><tr><td>

Header

</td><td>

Header or title for the table when the table is displayed in the response output. The header can be a text string, variables, or a script.

</td></tr><tr><td>

Display Column Headers

</td><td>

Toggle switch that enables the display of column headings.

</td></tr><tr><td class="sub-head" colspan="2">

Hide this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr></tbody>
</table>## Channel support

|Channel|Support|Constraints|
|-------|-------|-----------|
|Web UI|Supported|None|
|Mobile UI|Supported|None|
|Now Assist panel|Not supported|Not applicable|
|Microsoft Teams|Supported|None|
|Slack|Supported|None|
|Workplace|Supported|None|
|Facebook Messenger|Not supported|Not applicable|
|SMS Twilio|Not supported|Not applicable|
|LINE|Supported|None|
|WhatsApp|Not supported|Not applicable|
|Apple Messages for Business|Supported|None|
|Alexa \(Voice\)|Partial support|Supported on devices with screens. For nonscreen devices, the table will be read, if possible. For details, see [Fine-tune Virtual Agent settings and topics for the best Alexa voice chat experience](../concept/va-settings-for-alexa.md).|

## Example Table bot response output

**Note:** Virtual Agent Designer controls may display and function differently in other channels.

<table id="table_f1f_v2p_xdb"><thead><tr><th>

Response properties

</th><th>

Table bot response output

</th></tr></thead><tbody><tr><td rowspan="2">

![Basic properties include the node name, the method of populating the table, the filter, and the columns to be returned.](../images/table-bot-response.png "Table bot response control basic properties")

</td><td>

![Table in a chat window that displays the 2020 Company Holidays by Holiday and Date.](../images/table-bot-response-web-ui.png "Web UI Table bot response output")

</td></tr><tr><td>

![Table in a chat window that displays the first six 2021 Company Holidays by Holiday and Date. The user can choose an option to view all 11 rows.](../images/table-bot-response-mobile.png "Table bot response output in ServiceNow mobile")

</td></tr></tbody>
</table>**Parent Topic:**[Virtual Agent Designer bot responses](va-bot-responses.md)

