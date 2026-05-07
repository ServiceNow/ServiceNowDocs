---
title: Override model ratings
description: Override the risk rating and materiality tier of a model manually at any stages of its life-cycle. This helps maintain data accuracy, transparency, and governance when business context or expert judgment requires adjustments to system-calculated values.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Model Risk Management, Governance, Risk, and Compliance]
---

# Override model ratings

Override the risk rating and materiality tier of a model manually at any stages of its life-cycle. This helps maintain data accuracy, transparency, and governance when business context or expert judgment requires adjustments to system-calculated values.

## Before you begin

Role required: sn\_model\_risk\_mgmt.model\_governance or sn\_model\_risk\_mgmt.risk\_coordinator

## Procedure

1.  Navigate to **All** &gt; **Model Risk Workspace**.

2.  Select the list icon ![](../image/list-icon-mrm.png).

3.  From the list, navigate to **Models** &gt; **All**.

4.  Select the model and go to the **Details** tab.

5.  In the Risk &amp; materiality section, select the override icon ![](../image/edit-icon.png) on the **Risk rating** field.

6.  On the Override risk rating dialog, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Computed risk rating|The system-calculated risk rating. This field is automatically set to the computed value.|
    |New risk rating|Risk rating you want to apply, reflecting business context or expert judgment.|
    |Reason for override|Context to justify the manual override of the system-calculated risk rating.|
    |Revert to computed|Option to revert to the system-calculated risk rating.|

7.  In the Risk &amp; materiality section, select the override icon ![](../image/edit-icon.png) on the **Materiality tier** field.

8.  On the Override materiality tier dialog, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Computed materiality tier|The system-calculated materiality tier. This field is automatically set to the computed value.|
    |New materiality tier|Materiality tier you want to apply, reflecting business context or expert judgment.|
    |Reason for override|Context to justify the manual override of the system-calculated materiality tier.|
    |Revert to computed|Option to revert to the system-calculated materiality tier.|

9.  Select **Save**.


**Parent Topic:**[Using Model Risk Management](../concept/using-mrm.md)

