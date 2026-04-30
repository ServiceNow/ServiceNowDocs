---
title: Create a question for a catalog item in Catalog Builder
description: Specify a question that the requester should answer before submitting the catalog item.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Creating or editing catalog item template, Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a question for a catalog item in Catalog Builder

Specify a question that the requester should answer before submitting the catalog item.

## Before you begin

Role required: catalog\_builder\_editor, catalog\_admin, or admin

## About this task

If allowed in the template by the template owner \(catalog\_admin\) while configuring the template, the following question types can be used in the item creation process in the catalog builder. These question types are grouped into types and subtypes:

-   Text
    -   Single-line. Single-line text variable type in ServiceNow AI Platform.
    -   Multi-line. Multi-line text variable type in ServiceNow AI Platform.
    -   Rich text. HTML variable type in ServiceNow AI Platform.
-   Option
    -   Check box. Check box variable type in ServiceNow AI Platform.
    -   Yes/No. Yes/No variable type in ServiceNow AI Platform.
-   Choice
    -   Drop down \(fixed values\). Select Box variable type in ServiceNow AI Platform.
    -   Drop down \(values from a table\). Lookup Select Box variable type in ServiceNow AI Platform.
    -   Record reference. Reference variable type in ServiceNow AI Platform.
    -   Radio. Multiple Choice variable type in ServiceNow AI Platform.
    -   Multi-select. List Collector variable type in ServiceNow AI Platform.
    -   Requested for
-   Date/Time
    -   Date. Date variable type in ServiceNow AI Platform.
    -   Date &amp;Time. Date and time variable type in ServiceNow AI Platform.
    -   Duration
-   Display label
    -   Plain text. Label variable type in ServiceNow AI Platform.
    -   Rich text. Rich Text Label variable type in ServiceNow AI Platform.
-   Attachment

For detailed information about these question types, see [Types of service catalog variables](../reference/r_VariableTypes.md).

## Procedure

1.  Navigate to **Catalog Builder** &gt; **Create a new catalog item** &gt; **Question** and click **Insert new question**.

2.  On the Create question form, specify the required details.

    **Note:**

    -   The fields on the form vary based on the question type and subtype.
    -   While you configure each question, its preview is available.
    -   The question preview doesn't show interactions for the following questions types until the question is saved and then edited.
        -   Record reference
        -   Multi-select
        -   Drop down \(values from a table\)
    -   The question preview doesn't show annotations.
    1.  Specify the details on the **Question** tab.

<table id="table_okf_km2_g4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Type

</td></tr><tr><td>

Question type

</td><td>

Group under which the question type is categorized.

</td></tr><tr><td>

Question subtype

</td><td>

Subtype of the question.Only the question types allowed in the template are available.

</td></tr><tr><td class="sub-head" colspan="2">

Details

</td></tr><tr><td>

Map to field

</td><td>

Maps the question to a specific field on the table for the record producer.

</td></tr><tr><td>

Question label

</td><td>

Question for a requester while ordering the catalog item. For the Rich text question subtype, you can specify a formatted label to be displayed on a catalog item form.

</td></tr><tr><td>

Name

</td><td>

Internal name to identify the question.The name should not contain spaces or special characters. Only the underscore character is allowed.

</td></tr><tr><td>

Mandatory

</td><td>

Option to specify if the question is mandatory.

</td></tr><tr><td>

Hidden

</td><td>

Option to specify if the question is hidden.

</td></tr><tr><td>

Read-only

</td><td>

Option to specify if the question is read-only.

</td></tr><tr><td>

Conversational label

</td><td>

Option to specify the text that you want to ask in the conversation for the question of your catalog item.

</td></tr></tbody>
</table>    2.  Specify the details on the **Annotation** tab.

        This tab is available for the following question subtypes:

        -   Single-line
        -   Multi-line
        -   Rich text
        -   Yes/No
        -   Drop down \(fixed values\)
        -   Drop down \(values from a table\)
        -   Record reference
        -   Radio
        -   Date
        -   Date &amp;Time
        -   Multi-select
        |Field|Description|
        |-----|-----------|
        |Instructions|
        |Show instructions|Option to specify if instructions should be displayed for the question.|
        |Instructions label|Instruction for the requester while ordering the catalog item.|
        |Instructions|Detailed instruction content.|

    3.  Specify the details on the **Additional Details** tab.

        This tab is available for the following question subtypes:

        -   Single-line
        -   Drop down \(values from a table\)
        -   Record reference
        -   Multi-select
<table id="table_edr_jm2_g4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Validation

</td></tr><tr><td colspan="2">

Available for the Single-line question type

</td></tr><tr><td>

Text validation

</td><td>

Option to validate the specified text value based on the regular expression validations that have been set up in the system.

</td></tr><tr><td class="sub-head" colspan="2">

Source

</td></tr><tr><td colspan="2">

Available for the Dropdown \(values from a table\), Record reference, and Multi-select question subtypes

</td></tr><tr><td>

Table

</td><td>

Table from which the choices are retrieved.

</td></tr><tr><td>

Field

</td><td>

Field that should be displayed as a choice. This field is not available for the Record reference and Multi-select subtypes.

</td></tr><tr><td>

Filter conditions

</td><td>

Conditions to filter the choices.

</td></tr></tbody>
</table>    4.  Specify the details on the **Choices** tab.

        This tab is available for the following question subtypes:

        -   Drop down \(fixed values\)
        -   Drop down \(values from a table\)
        -   Yes/No
        -   Radio
<table id="table_fll_bn2_g4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Settings

</td></tr><tr><td>

Include none choice

</td><td>

Option to include **None** as a choice for the question.

</td></tr><tr><td>

Choice direction

</td><td>

Direction in which the choices should be displayed. Possible options are **Down** and **Across**. This option is available only for the Radio question subtype.

</td></tr><tr><td>

Do not select first choice

</td><td>

Option to ignore the first choice. This option is available only for the Radio question subtype.

</td></tr><tr><td class="sub-head" colspan="2">

Available Choices

</td></tr><tr><td colspan="2">

Available for the Drop down \(fixed values\) and Radio question subtypes. You can add a name-value pair for each choice.

</td></tr><tr><td>

Display name

</td><td>

Label for a choice.

</td></tr><tr><td>

Value

</td><td>

Value of the choice.

</td></tr></tbody>
</table>    5.  Specify the details in the **Default Value** tab.

        The default value specified here is pre-selected as the answer for the question when a requester opens the catalog item form for the item. This tab is available for the following question subtypes:

        -   Single-line
        -   Multi-line
        -   Yes/No
        -   Radio
        -   Date
        -   Date &amp;Time
        -   Multi-select
    6.  Specify the question details on the **Auto-populate** tab.

        For more information about configuring auto-populate value, see [Configure an auto-populate value for a question in Catalog Builder](config-auto-populate-value-for-question-cat-builder.md#).

3.  Click **Insert Question** to add the question to the item.

    **Note:**

    -   If there are two consecutive check boxes, then a virtual container is created for a group of check boxes. Only check box variable types can then be added inside that group.
    -   Even if a check box variable is added immediately after a group of check boxes, it's automatically added to the group.

-   **[Configure an auto-populate value for a question in Catalog Builder](config-auto-populate-value-for-question-cat-builder.md#)**  
Configure the value of a question to populate automatically whenever the value of another question of the reference type changes.

**Parent Topic:**[Creating or editing catalog item template](create-cat-item-template-cat-builder.md)

