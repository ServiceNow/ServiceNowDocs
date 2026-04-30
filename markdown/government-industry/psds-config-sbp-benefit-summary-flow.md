---
title: Duplicate and configure a benefit summary flow
description: Duplicate the flow.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-26"
reading_time_minutes: 1
breadcrumb: [Configure benefit summary, Social Benefits Playbook, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Duplicate and configure a benefit summary flow

Duplicate the flow.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workflow Studio**, and select **Flows**.

2.  Select and open the **Social Benefits – Benefit Summary Calculation – TEMPLATE** flow.

3.  Select the More actions icon \(...\) button and then select **Copy flow**.

4.  Update the **New flow name** field to reflect the calculation for a particular product model/benefit.

    For example, for a nutrition assistance program, enter **Nutrition Assistance – Benefit Summary Calculation**.

5.  Select **Social Benefits Playbook** in the application dropdown.

6.  Select **Copy**.

    The flow is now copied. Next, create an expense flow variable to set and retrieve expense values throughout the flow.

7.  Select the **More actions** icon \(…\), then select **Flow Variables**.

8.  Select the plus \(grey plus with circle\) icon.

9.  On the Flow Variables form, fill in the fields.

    |Flow Variables form fields|Description|
    |--------------------------|-----------|
    |Label|expenseTotal|
    |Name|expensetotal|
    |Type|Floating Point Number|

10. Select **Save**.


## Result

The flow has been duplicated and configured.

## What to do next

Build a benefit summary for a nutrition assistance program Leverage reusable actions and flow variables to develop a benefit summary calculation. For more information on how to do this, see .

