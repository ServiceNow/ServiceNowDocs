---
title: Troubleshoot Desktop Assistant notification delivery
description: Check notification records, queue processing, event handling, logs, and the endpoint client to identify why Desktop Assistant notifications aren't delivered.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/resolve-da-notification-issues.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 2
breadcrumb: [Customizing Desktop Assistant notifications using API parameters, Set up Desktop Assistant, Configure, Digital End-User Experience, IT Service Management]
---

# Troubleshoot Desktop Assistant notification delivery

Check notification records, queue processing, event handling, logs, and the endpoint client to identify why Desktop Assistant notifications aren't delivered.

## Before you begin

Role required: admin

## Procedure

1.  Verify the notification record.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

    2.  Open the Desktop Assistant Notification \(sn\_dex\_desktop\_assistant\_notification\) table and filter for records created within the last hour.

    3.  Verify that the notification record is valid.

        -   The **Notification message**, **Recipient list**, and **Notification source** columns contain values.
        -   The **Active** column is set to **True**.
        -   The **Expiry date** column is set to the current date plus the configured time-to-live \(TTL\) value.
    4.  If no record exists and the insert operation fails, verify the following:

        -   The invoking account has the sn\_dex\_desktop.admin role.
        -   The system property **sn\_dex\_desktop.enable\_push\_notification** is set to true.
2.  Check the notification delivery queue.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Tables** and open the Desktop Assistant Notification Queue \(sn\_dex\_desktop\_notify\_queue\) table.

    2.  Filter for records where value of the **Notification** column matches the sys\_id of the corresponding notification record.

        Each queue record represents a delivery attempt to a single device and can have one of the following statuses:

        -   Pending: Queued and not yet delivered to the Desktop Assistant client.
        -   Sent: Retrieved by the Desktop Assistant client.
        -   Failed: Delivery failed due to an Agent Client Collector \(ACC\) agent timeout or push service error.
    3.  If no queue records exist, verify that the desktop\_assistant\_notification\_call flow is active — notification delivery does not proceed if the flow did not trigger.

3.  Review event processing.

    1.  Navigate to **System Logs** &gt; **Events** and search for the **sn\_dex\_desktop.trigger\_checkdef** event.

    2.  If the event is not present, check if the **sn\_dex\_desktop.poll\_glide\_for\_notification** property is set to true.

        If this property is enabled, the event queue path is skipped and the event is not generated.

4.  Review application logs.

    1.  Navigate to **System Logs** &gt; **Application Logs** and filter for entries with a source that contains **\[DEX Notification\]**`[DEX Notification]`.

    2.  Check the log messages to identify the failure point.

        The following log messages indicate common failure points.

        |Log message|Description|
        |-----------|-----------|
        |`[`DEX`Notification] Executing REST request:`|Push service REST call initiated.|
        |`[`DEX`Notification] Response body: OK`|Push service acknowledged the request.|
        |`[`DEX`Notification] Error during REST API call:`|Push service REST call failed.|
        |`DesktopAppNotificationUtils: ERROR, invalid notification`|Stored notification payload is invalid JSON.|

5.  If the log shows `[DEX Notification] Error during REST API call:`, check network connectivity and verify the **sn\_dex\_desktop.push\_notification\_service\_info** property.

6.  If the queue status is **Sent** but the user reports no visible notification, validate the endpoint and ACC agent.

    1.  Confirm that the Desktop Assistant client is running and the user is signed in.

    2.  Review the ACC logs to confirm that the agent is running and communicating with the ServiceNow instance.

        For information about accessing ACC logs, see [View the Agent Client Collector logs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-view-log.md).

    3.  Open the Desktop Assistant \(sn\_dex\_desktop\_assistant\_notification\) table.

    4.  Filter by **Created** or **Recipient list** to locate the notification record.

    5.  Check the value in the **Expiry date** field on the record.

    6.  Compare the **Expiry date** value with the current system date and time.

        -   If the expiry date is earlier than the current date and time, the notification has expired and is no longer delivered to the Desktop Assistant client.
        -   If the expiry date is in the future, the notification is still eligible for delivery.

