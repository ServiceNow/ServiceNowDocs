---
title: Join workflow activity
description: The Join activity unites multiple execution paths into one transition.
locale: en-US
release: australia
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Utility workflow activities, Workflow activities reference, Workflow activities, Classic Workflow, Build workflows]
---

# Join workflow activity

The **Join** activity unites multiple execution paths into one transition.

Use this activity to cause a workflow to wait for all activities in multiple paths to finish before continuing. If multiple concurrent workflow paths meet without a **Join** activity, any subsequent activities execute twice.

To add Join to the canvas, click **Submit**. On the canvas, connect incoming transitions from each activity you want to act as a predecessor to the Join activity. Then connect outgoing transitions to the two exit conditions: Complete and Incomplete.

## Results

Provide an Incomplete transition out of a **Join** whenever it is possible for any predecessor activities to follow a transition path that does not lead to the **Join** activity.

|Result|Description|
|------|-----------|
|Complete|**Join** exits along the Complete path when the system has determined that all predecessor activities have completed and transitioned to the **Join**.|
|Incomplete|**Join** exits along the Incomplete path when the system determines that at least one predecessor activity completed but transitioned along a path that bypassed the **Join** activity.|

