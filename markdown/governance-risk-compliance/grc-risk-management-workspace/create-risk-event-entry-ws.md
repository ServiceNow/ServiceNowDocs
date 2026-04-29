---
title: Create a risk event entry in the Risk Workspace
description: Create a risk event entry to determine the monetary or non-monetary impact of the risk event. A risk event can have multiple risk event entries.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Create a risk event entry in the Risk Workspace

Create a risk event entry to determine the monetary or non-monetary impact of the risk event. A risk event can have multiple risk event entries.

## Before you begin

Role required: sn\_risk.manager

## About this task

Risk event entries capture the direct and indirect losses reported due to the risk event. For example, if a risk event of a fire outbreak in an organization is reported, the direct and indirect losses associated with it could be replacing furniture, replacing hardware, losing important data and so on. All these associated losses must be captured individually. You can add risk event entries only for actual events. Potential Risk event entries cannot have risk event entries. You can select any currency while reporting the losses and the currency conversion system will convert the currency to USD.

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Workspace** &gt; **Risk events** &gt; **All events**.

2.  Open the event for which you want to add risk event entries.

3.  Click the Risk Event Entries related list.

4.  To create direct and indirect losses, new loss recovery, new additional cost, or new non-financial impact, perform the following actions as necessary.

    |To create...|Action|
    |------------|------|
    |**New direct/indirect loss.**|Click **New direct/indirect loss** and fill in the details.|
    |**New loss recovery**|From the **New direct/indirect loss** list, select **New loss recovery** and fill in the details. New loss recovery is amount recovered from the total financial impact. If the amount is recovered within the number of days specified in your configuration, the **Full rapid recovery**option is automatically selected.|
    |**New additional cost**|From the **New direct/indirect loss** list, select **New additional cost** and fill in the details. New additional cost is the cost incurred due to the impact.|

5.  Click **Save** and refresh the page.

    The loss amounts get updated on the page.


**Parent Topic:**[Using the Risk Workspace](../concept/using-risk-workspace.md)

