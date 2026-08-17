---
title: Copy a change request
description: You can copy details of an active or canceled change request to a new change request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/change-management/copy-a-change-request.html
release: zurich
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-01-30"
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

2.  Open the change request that you want to copy.

    The Copy Change option is available from the form, and not from the list view.

3.  In the change request form header, select the Additional Actions menu icon \[Omitted image "additional-actions.png"\] Alt text: Change request form header showing the Additional Actions menu open with Copy Change highlighted and then select **Copy Change**.

    A preview of the new change record appears with values from the original source change record.

4.  Edit values on the newly created change record, as appropriate.

5.  Select **Submit** to create a new change request record.


## What to do next

After an existing change request is copied and a new one created. A user with ITIL role then reviews, approves, implements, and closes the change request as necessary.

In addition, you can [associate CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/change-management/c_AffectedCIsAndImpactedServices.md) to the newly created change request.

**Parent Topic:**[Create a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/change-management/t_CreateAChange.md)

**Related topics**  


[Create a change request from a configuration item \(CI\)]()

[Create a standard change request from the catalog]()

[Create a change task]()

[Unauthorized change request]()

[Configure ability to copy a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/change-management/configure-copy-change-request.md)

