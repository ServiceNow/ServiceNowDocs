---
title: Copy a change request
description: You can copy details of an active or canceled change request to a new change request.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a change request, Use, Change Management, IT Service Management]
---

# Copy a change request

You can copy details of an active or canceled change request to a new change request.

## Before you begin

Role required: itil, admin, or sn\_change\_write

## About this task

The administrator configures which of the following items are copied to the new change request.

-   The content that is copied.
-   The attributes or fields and values that are copied. All non-copied attributes are reset to default values.
-   The configured related tables that are copied.

**Note:** You cannot copy change details from a standard change.

New change tasks can be created when a change is copied. If your change record has associated workflows that create change tasks, then these change tasks may not be copied because the workflow creates them. Only manually created tasks are copied, if the workflow when creating the task sets the **created\_from** field on the **change\_task** table to **workflow**. The **created\_from** field has a default value of **manual**.

## Procedure

1.  Navigate to **Change** &gt; **Open**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

2.  Select the change request to be copied.

3.  Select the Additional Actions menu icon \(![](../../enterprise-dev-ops/image/additional-actions.png)\) and then select **Copy Change** to copy change request details.

    A preview of the new change record appears with values from the original source change record.

4.  Edit values on the newly created change record, as appropriate.

5.  Click **Submit** to create a new change request record.


## What to do next

After an existing change request is copied and a new one created. A user with ITIL role then reviews, approves, implements, and closes the change request as necessary.

In addition, you can [associate CIs](../concept/c_AffectedCIsAndImpactedServices.md#) to the newly created change request.

**Parent Topic:**[Create a change request](t_CreateAChange.md)

**Related topics**  


[Create a change request from a configuration item \(CI\)](t_CreateAChangeFromACI.md)

[Create a standard change request from the catalog](t_RaiseNewStdCngeFmTempl.md)

[Create a change task](create-a-change-task.md)

[Unauthorized change request](../concept/unauthorized-change-request.md)

[Configure ability to copy a change request](configure-copy-change-request.md)

