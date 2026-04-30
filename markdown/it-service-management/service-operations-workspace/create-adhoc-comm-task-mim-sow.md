---
title: Create an adhoc communication task
description: Create an adhoc communication task as required during the various phases of an incident in Major Incident Management.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Communicating about incidents and major incidents, Managing a major incident record, Major Incident Management in Service Operations Workspace, Manage, Service Operations Workspace for ITSM, IT Service Management]
---

# Create an adhoc communication task

Create an adhoc communication task as required during the various phases of an incident in Major Incident Management.

## Before you begin

Role required: major\_incident\_manager, itil, ia\_admin, or admin

## Procedure

1.  On the incident record page, select the **Communicate** tab.

2.  Select **New communication**.

3.  On the New communication pop-up window, fill in the details.

<table id="table_vkn_1pg_z1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Compose and sent communication

</td><td>

Indicates when the communication message must be composed and sent. Possible values are:-   Now – The communication message is composed and sent immediately.
-   Later – The communication message is composed and sent later after a definite time interval.


</td></tr><tr><td>

Frequency

</td><td>

Frequency at which the communication must be composed and sent. Possible values are:-   One time – The communication message is composed and sent only once.
-   Recurring - The communication message is composed and sent after a repeated time interval.


</td></tr><tr><td>

Due in \(minutes\)

</td><td>

Duration of time in minutes after which the communication message must be composed and sent.

 **Note:** This field is displayed only if the **Frequency** field is set to **Recurring**.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the communication task.

</td></tr><tr><td>

Channels

</td><td>

Channel that must be used to compose and sent communication messages. Possible options are:-   DEX Desktop Assistant: Compose and send the notification message through DEX Desktop Assistant. For more information on DEX Desktop Assistant, see [Use DEX Desktop Assistant](../../digital-end-user-experience/concept/use-dex-desktop-exp.md).
-   Email – Compose and send the communication message as an email.
-   SMS – Compose and send the communication message as SMS.
-   Microsoft Teams notification - Compose and send communication messages as Microsoft Teams notifications.
-   Slack - Compose and send communication message to a Slack channel.
-   SMS notifications- Compose and send communication message as SMS notifications.
-   Slack notifications – Option to compose and send communication messages as Slack notifications.


</td></tr><tr><td>

Recipients

</td><td>

User, user groups, or list of recipients to whom the communication message must be sent.

</td></tr></tbody>
</table>4.  Either save your communication or compose your communication, depending on whether the **Compose and sent communication** field has been set to **Later** or **Now**.

    -   If the **Compose and sent communication** field is set to **Later**, select **Save**. The communication task is saved and displayed in the list of communication tasks on the **Communicate** tab.
    -   If the **Compose and sent communication** field is set to **Now**, select **Compose communication** to compose your messages within your selected communication channels. The communication task record opens on a new tab within the incident view. For more information, see [Compose communications for incidents and major incidents](compose-communication-mim-sow.md).

**Parent Topic:**[Communicating with stakeholders about incidents and major incidents in SOW](../concept/communicating-with-stakeholders-sow.md)

