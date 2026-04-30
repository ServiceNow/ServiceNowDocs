---
title: Disable the creation of an unauthorized change request
description: You can choose to disable the generation of unauthorized change requests that you receive on any unauthorized change event. When a configuration item \(CI\) that is part of an application service is updated, the system identifies this update and verifies whether the updated CI is part of an open change request.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Unauthorized change request, Create a change request, Using Change Management, Change Management, IT Service Management]
---

# Disable the creation of an unauthorized change request

You can choose to disable the generation of unauthorized change requests that you receive on any unauthorized change event. When a configuration item \(CI\) that is part of an application service is updated, the system identifies this update and verifies whether the updated CI is part of an open change request.

## Before you begin

Role required: admin or change\_manager

## About this task

If the updated CI is not part of an open change request, then the system triggers a change request, and sends a notification. The Change Management application uses this event to create an unauthorized change. If there are many CI changes with no open change request created to include the CIs, then the system creates unauthorized change requests on these CIs. When this event occurs, numerous unauthorized change requests are triggered, and notifications are sent to the members of the group. To avoid this situation, you can disable the **Enable event processing** property before you perform the updates. For more information on additional unauthorized change properties, see [Unauthorized change properties](../reference/unauth-change-properties.md).

**Note:** Enable the property when you finish your updates. If this property is disabled, unauthorized change requests are not created.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Administration** &gt; **Unauthorized Change Properties**.

2.  Clear the **Enable event processing** property check box.

3.  Click **Update**.


## Result

The creation of an unauthorized change request is disabled, and no notifications are sent.

**Parent Topic:**[Unauthorized change request](../concept/unauthorized-change-request.md)

**Related topics**  


[Unauthorized change properties](../reference/unauth-change-properties.md)

