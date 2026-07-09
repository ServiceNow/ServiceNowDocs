---
title: Create a transaction rule grouping
description: Create a rule grouping to bundle rules together for assignment to stages and events in ServiceNow CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-create-rule-grouping.html
release: australia
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 2
breadcrumb: [Rules and rule groupings, Configuring Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Create a transaction rule grouping

Create a rule grouping to bundle rules together for assignment to stages and events in ServiceNow CPQ.

## Before you begin

The rules to include in the grouping must exist before you create the rule grouping. For more information, see [Create a transaction rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-create-rule.md).

Role required: admin

## About this task

Rule groupings bundle transaction-level and transaction line-level rules together so they execute as a unit. A rule grouping can contain rules of both levels. Once created, rule groupings are assigned to stages and events — the grouping executes when the stage is entered or the event fires, running all rules within it that meet their conditions.

For a conceptual overview of how rule groupings relate to stages and events, see [Quote transaction rules and rule groupings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-rules-and-rule-groups.md).

## Procedure

1.  Navigate to **All** &gt; **CPQ Administration** &gt; **Transaction**.

2.  Select **Rule Groupings** in the left menu, then select **+ New Rule Grouping**.

3.  In the **New Rule Grouping** window, enter a name for the rule grouping and verify the variable name.

    The variable name is set in camel case from the name you enter. To use a custom variable name, select the pencil icon to the right of the **Variable Name** field.

4.  Select **Save**.

    The rule grouping editor opens.

5.  To associate rules with the grouping, select **+ Associate Rules**.

    A slide-out panel opens, showing available rules in the **Results** column.

6.  Select **+** next to a rule in the **Results** column to move it to the **Selected** column.

7.  Repeat the previous step for each rule to include in the grouping.

    A rule grouping can include both transaction-level and transaction line-level rules.

8.  Select **Done**.

    The rule grouping editor displays the rules added to the group. The rule grouping is saved and available for assignment to stages and events.


## Result

The rule grouping appears in the Rule Groupings list and is available to assign to a stage or event. All rules in the grouping execute when the stage is entered or the event fires, subject to each rule's own conditions.

## What to do next

Assign the rule grouping to a stage or event so that its rules execute during the quote lifecycle.

-   To assign to a stage, see .
-   To assign to an event, see [Create an event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-create-custom-event.md).

