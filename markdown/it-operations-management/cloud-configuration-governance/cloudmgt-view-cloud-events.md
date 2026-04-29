---
title: View cloud events
description: You can view the events that are generated from your cloud resources if your administrator configured Cloud Provisioning and Governance to monitor them. All events are listed on the Cloud Events tab on the stack details page.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Using the Activities page, Cloud User Portal, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# View cloud events

You can view the events that are generated from your cloud resources if your administrator configured Cloud Provisioning and Governance to monitor them. All events are listed on the Cloud Events tab on the stack details page.

## Before you begin

Role required: sn\_cmp.cloud\_service\_user

## Procedure

1.  View the cloud events page using either of the following methods:

    -   On the **Activities** page, click **Monitor** &gt; **Cloud Events**.
    -   On the **Stack Details** page, click the **Cloud Events** tab in the **Activities** section.
    The **Cloud Events** section lists all events for the stack.

<table id="table-activities"><tbody><tr><td>

Created

</td><td>

Timestamp of the arrival of the event.

</td></tr><tr><td>

Source

</td><td>

Source of the event:-   **azure**: Azure Alert
-   **aws**: AWS Config
-   **vmware**: VMware Events


</td></tr><tr><td>

Event name

</td><td>

Name that is provided by Amazon, Azure, or VMware.

</td></tr><tr><td>

Subject

</td><td>

Text that describes the event.

</td></tr><tr><td>

Event time

</td><td>

Timestamp of the event.

</td></tr><tr><td>

Resource ID

</td><td>

Unique ID of the resource that received the life cycle state change or configuration change event.

</td></tr></tbody>
</table>2.  Click an entry to view full details.


