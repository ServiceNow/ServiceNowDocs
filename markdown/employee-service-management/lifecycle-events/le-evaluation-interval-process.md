---
title: View and use the Condition with Event BR \(Demo\) activity set
description: You can trigger activity sets using an event that is included in the Condition with Event BR \(Demo\) activity set or you can create and use server-side code \(business rule, event script, scheduled job, etc.\) that triggers the check\_activity\_set\_trigger event into the HR Activity Set Trigger Check workflow.
locale: en-US
release: xanadu
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Lifecycle Events evaluation interval, Configure a lifecycle event, Building a lifecycle event, Lifecycle Events, HR Service Delivery, Employee Service Management]
---

# View and use the Condition with Event BR \(Demo\) activity set

You can trigger activity sets using an event that is included in the Condition with Event BR \(Demo\) activity set or you can create and use server-side code \(business rule, event script, scheduled job, etc.\) that triggers the check\_activity\_set\_trigger event into the HR Activity Set Trigger Check workflow.

## Before you begin

Role required: admin

**Note:** To access the **Condition with Event BR \(Demo\)** activity set, activate the Human Resources Scoped App: Lifecycle Events for Enterprise \(com.sn\_hr\_lifecycle\_ent\) plugin. This is an optional method that can be used instead of the values in the **Evaluation interval** field.

## Procedure

1.  Navigate to **Lifecycle Events** &gt; **Administration** &gt; **Manage Lifecycle Events**.

2.  Select the **New Hire Onboarding \(Demo\)** lifecycle event.

3.  Select the **Activity Sets** tab.

4.  Scroll to the right and select the **Condition with Event BR \(Demo\)** activity set.

    **Note:** The **Condition with Event BR \(Demo\)** activity set is an example of what you can use. This is an optional solution, but you can create and use server-side code \(business rule, event script, scheduled job, etc.\) that triggers the check\_activity\_set\_trigger event into the HR Activity Set Trigger Check workflow.

5.  Select the edit \(![Edit icon](../../legal-mobile/image/edit-icon.png)\) in the **Condition with Event BR \(Demo\)** activity set.

    -   The **Trigger type** is **Condition**.
    -   When the **State** of the LE/HR case changes to **Work in Progress**, the **Condition with Event BR \(Demo\)** activity set triggers and sends a email.
    ![Condition with Event BR Demo activity set](../image/condition_event_BR_demo.png)


**Parent Topic:**[Lifecycle Events evaluation interval](../concept/le-evaluation-interval1.md)

