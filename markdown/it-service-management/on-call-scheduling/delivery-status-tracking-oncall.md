---
title: Delivery status tracking for On-Call Scheduling notifications
description: Every notification that On-Call Scheduling dispatches during an escalation has its delivery status captured, providing a reliable audit trail of who was notified and whether the notification reached them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/on-call-scheduling/delivery-status-tracking-oncall.html
release: brazil
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: concept
last_updated: "2026-09-19"
reading_time_minutes: 3
breadcrumb: [Escalations in On-Call Scheduling, Defining On-Call Scheduling escalation process, On-Call Scheduling, IT Service Management]
---

# Delivery status tracking for On-Call Scheduling notifications

Every notification that On-Call Scheduling dispatches during an escalation has its delivery status captured, providing a reliable audit trail of who was notified and whether the notification reached them.

When an escalation dispatches a notification, a delivery status record is created and linked to the parent escalation. The status record captures the notification ID, recipient, channel, timestamp of dispatch, and current status.

**Note:** Delivery status tracking applies only to escalation notifications sent through On-Call Scheduling subflows. It does not apply to escalation notifications triggered through legacy workflows. For information about subflows and workflows, see [On-Call Scheduling subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/on-call-scheduling/on-call-scheduling-subflows-overview.md).

## Delivery status life cycle

A delivery status record moves through the following states. **Failed** is a terminal state that can be reached from any prior state. The **Status** field on the On-Call Escalation Notification record shows these statuses for an escalation notification.

<table id="table_delivery-status-values"><thead><tr><th>

Status

</th><th>

Icon

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sent

</td><td>

\[Omitted image "icon-single-check.png"\] Alt text:

</td><td>

The notification provider confirmed dispatch. An unrecognized provider status code also defaults to this state, and an error is logged for diagnostic review.

</td></tr><tr><td>

Delivered

</td><td>

\[Omitted image "icon-double-check.png"\] Alt text:

</td><td>

The provider returned a delivery confirmation.

</td></tr><tr><td>

Failed

</td><td>

\[Omitted image "icon-cross.png"\] Alt text:

</td><td>

The notification did not reach the recipient. Pointing to the icon shows the specific failure reason, when one is recorded.For information about how failed notifications are logged, see [Delivery failures](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/on-call-scheduling/delivery-status-tracking-oncall.md).

</td></tr></tbody>
</table>A delivery status icon in the **Contact Information** tab of the on-call escalation tracking dialog indicates the current delivery status for each notification attempt. See [Track the progress of an escalation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/on-call-scheduling/track-escalation-progress-oncall.md).

If multiple status updates for the same notification arrive out of order, for example a delivery confirmation that arrives before the sent confirmation, the system keeps the latest known state.

## Supported channels

Delivery status is tracked for notifications sent over the following channels.

-   SMS
-   Voice \(phone call\)
-   Microsoft Teams
-   Slack
-   Push notification
-   Email, when sent through [Notify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/t_ActivateNotify.md)

## Delivery failures

When a notification's status transitions to **Failed**, a system-generated work note is added to the parent record linked to the escalation \(for example, an incident\). The **Failure Reason** field on the On-Call Escalation Notification record displays the failure reason. The work note is attributed to the on-call notification engine and includes the following information.

-   Recipient name
-   Channel
-   Failure reason
-   Failure timestamp
-   Escalation step number

Only failures are written to work notes.

**Parent Topic:**[Escalations in On-Call Scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/on-call-scheduling/escalations-oncall.md)

**Related topics**  


[Designing an escalation process]()

[Track the progress of an escalation]()

[View details in an escalation log]()

[View details in an escalation log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/on-call-scheduling/view-escalation-logs-oncall.md)

[Track the progress of an escalation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/on-call-scheduling/track-escalation-progress-oncall.md)

