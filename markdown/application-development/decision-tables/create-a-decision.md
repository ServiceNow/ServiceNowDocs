---
title: Create a decision table to resolve complex decisions
description: Create a decision table to help you resolve a complex decision that depends on multiple factors.
locale: en-US
release: zurich
product: Decision Tables
classification: decision-tables
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Decision tables in the classic environment, Decision Tables, Builder library, Developing your application, Building applications]
---

# Create a decision table to resolve complex decisions

Create a decision table to help you resolve a complex decision that depends on multiple factors.

## Before you begin

Role required: decision\_table\_admin

## Procedure

1.  Create or select a table to use for your decision answer records.

    You will associate an answer record to each decision on your decision table in later steps. This answer record is returned when that decision is reached based on your inputs. For information on creating a table, see [Create a table](https://www.servicenow.com/docs/access?context=t_CreateATable&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

2.  Ensure that one field on the table that you use for your decision records has been set as the display value.

    This field is used as a label when you display decision answers in Workflow Studio.

    You can use an existing table or create a new table to use for your decision records.

3.  Create a record on this table to each answer in your decision.

    If you have modified an existing table, you may need to customize the form to show the new fields that you have added.

4.  Create a decision table record.

    1.  Navigate to **System Definition** &gt; **Decision Tables**, and select **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Descriptive label for this decision.|
        |Application|Application scope of this decision. This field defaults to the current scope.|
        |Answer table|Table that this decision uses for answer records. Select the table that you created in the previous steps.|
        |Accessible From|Option to limit the availability of this decision to the current scope. Select **All application scopes** or **This application scope only**.|

    3.  Right-click the form header and select **Save**.

        The form refreshes with the Decision Inputs and Decisions related lists.

5.  Create decision input records.

    1.  In the Decision Inputs related list, select **New**.

    2.  On the form, fill in the fields.

<table id="table_lyr_psm_3fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the decision that is associated to this decision input. This field is automatically populated.

</td></tr><tr><td>

Application

</td><td>

Application scope of this decision input. This field defaults to the current scope.

</td></tr><tr><td>

Type

</td><td>

Type of data that is used for this input. When you use this decision in a flow, you can only use data pills that match this type.

</td></tr><tr><td>

Active

</td><td>

Check box to activate this input. This field is selected by default.

</td></tr><tr><td>

Label

</td><td>

Descriptive label for this input.

</td></tr><tr><td>

Read only

</td><td>

Check box to make this decision input read-only.

</td></tr><tr><td>

Column name

</td><td>

Column name for this input. This field is automatically populated when you give the **Label** field a value.

</td></tr><tr><td>

Mandatory

</td><td>

Check box to make this decision input mandatory.

</td></tr><tr><td>

Display

</td><td>

Check box to indicates that this decision input is the [display value](https://www.servicenow.com/docs/access?context=c_DisplayValues&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for reference fields.

</td></tr><tr><td>

Choice

</td><td>

Select a method for users to see a list of suggested values:-   List menu without -- None --
-   List menu with -- None --
-   [Suggestion field type](https://www.servicenow.com/docs/access?context=t_AddingASuggestionField&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)
If a choice is used, define your choices in the Choices related list at the bottom of the form.

</td></tr><tr><td>

Default Value

</td><td>

Default value for this input.

</td></tr></tbody>
</table>    3.  Select **Submit**.

        Your changes are saved and the decision table record reopens.

6.  Create decision records.

    1.  In the Decisions related list, select **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Label|Descriptive label for this decision table.|
        |Application|Application scope of this decision. This field defaults to the current scope.|
        |Order|Order in which the flow evaluates decisions. The order can be important in flows that use the **First decision that matches** option and ends after the first match is found.|
        |Answer|Answer that is used when the conditions in this decision are met.|
        |Default Answer|Check box to enable this decision as the default for your decision table.|
        |Condition|Conditions that are needed to reach this decision. The fields available for your condition are the Decision inputs that are associated with this decision table.|

    3.  Select **Submit**.

        Your changes are saved and the decision table record reopens.


## What to do next

With Workflow Studio, you can add your decision to the **Make a decision** flow logic. For more information about the **Make a decision** flow logic, see [Make a decision flow logic](https://www.servicenow.com/docs/access?context=flow-logic-make-decision&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

**Parent Topic:**[Decision tables in the classic environment](../concept/decision-tables-classic-ui.md)

