---
title: Filter ignorable DevOps events
description: Filter out ignorable DevOps events before they trigger a Flow execution to improve performance.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage, DevOps Change Velocity, IT Service Management]
---

# Filter ignorable DevOps events

Filter out ignorable DevOps events before they trigger a Flow execution to improve performance.

Azure DevOps and GitHub tool integrations have a filtering mechanism that determines if any incoming event can be ignored before it causes a Flow to be triggered. Both the integrations have their own filters, which may be deactivated or overridden to alter the filtering criteria. These filters check whether the tool is connected, referenced object is tracked and is present in the system.

You can activate or deactivate these filters.

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points** and search for DevOps.
2.  Select **sn\_devops.DevOpsEventFilterAPI**.
3.  From the **Extension Instances** section under **Related links**, select the extension instance of the tool for which you want to activate or disable the filter.
4.  Select the **Active** check box to enable the filter.

    By default, the check box is selected. If you want to disable the filter, clear the check box.


**Parent Topic:**[Managing DevOps Change Velocity](using-devops-change-velocity.md)

