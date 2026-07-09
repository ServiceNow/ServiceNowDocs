---
title: Create an event
description: Create a custom event in ServiceNow Quote Experience to trigger rule groupings, integrations, and stage transitions based on business-specific requirements in ServiceNow CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-create-custom-event.html
release: australia
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [Events, Configuring Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Create an event

Create a custom event in ServiceNow Quote Experience to trigger rule groupings, integrations, and stage transitions based on business-specific requirements in ServiceNow CPQ.

## Before you begin

Any rule groupings or integrations to assign to the event must exist before creating the event.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **CPQ Administration** &gt; **Transaction** &gt; **Events**.

2.  Select **+ New Event**.

3.  In the **Name** field, enter the name of the new field.

    The variable name is set in camel case from the name you enter. For example, entering `Total of Manufacturing Lines` produces the variable name **totalOfManufacturingLines**. To use a custom variable name, select the pencil icon to the right of the **Variable Name** field.

4.  Select the event level and then select **Save**.

    -   Select **Transaction** for a header-level event that appears as a button at the top of the quote.
    -   Select **Transaction Line** for a line-level event that appears on individual lines in the quote lines grid.
    The event editor opens. By default, new events have their event access set to **No Access**.

5.  Select **Edit Event Access**, change the access level to **Active**, and select **Done**.

6.  In the **Actions** area, select **+ Add New Action** and choose either a rule grouping or an integration to assign to the event.

    Multiple rule groupings and integrations can be assigned to the same event.

7.  To configure the event to transition the quote to another stage, enable the **Transition** toggle and set the transition direction \(forward or backward in the stage sequence\).

8.  Select **Save**.

    The new event appears in the events list at the transaction or transaction line level, depending on the level chosen.


## What to do next

Add the event to the quote layout to make it available as a button to users. For more information, see [Create a quote transaction layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-create-layout.md).

