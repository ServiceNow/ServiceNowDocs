---
title: View and use the Condition with Event BR \(Demo\) business rule
description: You can view and use the Condition with Event BR \(Demo\) business rule to trigger an evaluation of your activity set faster.
locale: en-US
release: xanadu
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2022-08-04"
reading_time_minutes: 1
breadcrumb: [Lifecycle Events evaluation interval, Configure a lifecycle event, Building a lifecycle event, Lifecycle Events, HR Service Delivery, Employee Service Management]
---

# View and use the Condition with Event BR \(Demo\) business rule

You can view and use the Condition with Event BR \(Demo\) business rule to trigger an evaluation of your activity set faster.

## Before you begin

To evaluate the trigger conditions for an activity set via the Condition with Event BR \(Demo\) business rule, the **Trigger type** field in the corresponding Activity Set record must be set to **Condition**.

Role required: admin

## Procedure

1.  Navigate to **Lifecycle Events** &gt; **Lifecycle Events Cases**.

2.  Select a case that was created from the New Hire Onboarding \(Demo\) lifecycle event.

3.  Select the Additional actions \(![Additional actions icon](../image/additional-actions-icon.png) icon.

4.  Select **Configure** and then **Business Rules**.

5.  Search and select **Condition with Event BR \(Demo\)**.

    **Note:** The **Condition with Event BR \(Demo\)** business rule runs after the State changes to Work in Progress.

6.  Select the **Advanced** tab.

    In the Script field, you can view how this business rule works. It looks for the running flows for the LE/HR case. When it finds the HR Activity Set Trigger Check workflow, it broadcasts the check\_activity\_set\_trigger event to the flow. This is what triggers the evaluation of an activity set faster rather than wait for the value \(default is four hours\) in the **Evaluation interval** field.![Condition with Event BR demo business rule](../image/condition-event-BR-buss-rule.png)

7.  When you change the state of the LE/HR case to **Work in Progress**, the activity set triggers.

8.  Return to the LE/HR case and select the **Show Workflow** related link.

9.  Select the **HR Activity Set Trigger Check** tab.

    The Timer was cancelled when the LE/HR case state was changed to **Work in Progress** and the **check\_activity\_set\_trigger** event was fired.

    ![HR Activity Set Trigger Check workflow](../image/le-case-act-set-trigger-check.png)


**Parent Topic:**[Lifecycle Events evaluation interval](../concept/le-evaluation-interval1.md)

