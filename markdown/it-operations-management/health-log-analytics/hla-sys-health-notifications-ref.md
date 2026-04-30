---
title: Health Log Analytics system health notifications
description: Health Log Analytics system health notifications help to ensure that you're aware of potentially dangerous conditions. You can manually adjust the status of a notification as the issue is being addressed.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Health Log Analytics system health notifications

Health Log Analytics system health notifications help to ensure that you're aware of potentially dangerous conditions. You can manually adjust the status of a notification as the issue is being addressed.

Health Log Analytics uses self-health checks to monitor the health of its components. When it discovers a system health issue, a notification is created and an email sent to all subscribers. The Health Log Analytics Administration **System Health - Notifications** list displays all HLA system health notifications, including those about internal errors. You can ask your admin to subscribe you to the system health notifications.

<table id="table_ozm_mz2_wmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Notification header.

</td></tr><tr><td>

Description

</td><td>

Description of the notification.

</td></tr><tr><td>

Created

</td><td>

Date when the notification was created.

</td></tr><tr><td>

State

</td><td>

State of the notification.-   **New**: The notification was newly added.
-   **Acknowledged**: The notification record was read.
-   **Work in progress**: The issue described in the notification is being addressed. Adjust the value manually.
-   **Closed**: The issue is no longer active. Adjust the value manually.

**Note:** Changing the state of a notification does not affect the state of the issue described in it. A notification in the Closed state will still display in the table. The notification is automatically filtered out of the table only when the issue is detected as fixed \(that is, when the Healthy status is **True**\).

</td></tr><tr><td>

Healthy

</td><td>

Field that indicates the status of the issue mentioned in the notification.The table shows only notifications with a Healthy value of **False**. When the issue is detected as fixed, the value is automatically changed to **True** and the notification is filtered out of the table.

</td></tr></tbody>
</table>**Parent Topic:**[Health Log Analytics reference](../concept/hla-reference.md)

