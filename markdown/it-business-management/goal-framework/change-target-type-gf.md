---
title: Change the type of a target
description: Change the type of an existing target when the way that you measure the target changes, for example, from Maximize to Maintain above. Depending on the old and new types, the change can clear the actual value and progress of the target.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/goal-framework/change-target-type-gf.html
release: brazil
product: Goal Framework
classification: goal-framework
topic_type: task
last_updated: "2026-10-06"
reading_time_minutes: 2
keywords: [target type, change target type, Maintain above, Maintain below, Maintain constant]
breadcrumb: [Create targets for a goal, Manage goals, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Change the type of a target

Change the type of an existing target when the way that you measure the target changes, for example, from Maximize to Maintain above. Depending on the old and new types, the change can clear the actual value and progress of the target.

## Before you begin

Role required: sn\_gf.goal\_user or sn\_gf.goal\_admin

You must be the owner or a contributor of the goal that the target belongs to.

## About this task

You can change the **Type** field of a target at any time, including after actual values are recorded. What happens to the existing values depends on the old and new types:

|Change|Effect on the target|
|------|--------------------|
|From one Maintain type to another, for example, from **Maintain above** to **Maintain constant**|The actual values are kept, and progress is recalculated for the new type.|
|Between **Maximize**, **Minimize**, and a Maintain type|The actual value and progress of the target are cleared. If the target has target breakdowns, they are regenerated with planned targets for the new type and no actual values.|
|To or from **Milestone**|The **Unit of measure** field changes to match the new type: a qualitative unit of measure for **Milestone**, and a quantitative unit of measure for the other types. When you change to **Milestone**, any target breakdowns are deleted.|

When the change clears or resets values, a confirmation message appears before the change is applied. If you rely on the existing actual values, record them before you continue.

## Procedure

1.  Navigate to **Enterprise Goal Management** &gt; **Targets**.

2.  Open the target that you want to change.

3.  In the **Type** field, select the new type.

    For information on choosing a type, see [Target types and achievement strategies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/goal-framework/target-types-gf.md).

4.  If a confirmation message appears, select **OK** to apply the new type.

    To keep the previous type, select **Cancel**. The **Type** field returns to its previous value, and the target is not changed.

5.  Select **Update**.


## Result

The target uses the new type to calculate progress. If the target has target breakdowns and the new type is a Maintain type, the planned target of every target breakdown is set to the final target value.

## What to do next

If the actual value was cleared, enter the actual values again. For more information, see [Update the progress of the target](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/goal-framework/update-progress-of-target.md) or [Update the actual value of a target breakdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/goal-framework/update-the-actual-value-of-a-target-breakdown-gf.md).

