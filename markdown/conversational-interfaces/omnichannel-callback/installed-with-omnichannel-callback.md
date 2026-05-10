---
title: Components installed with Omnichannel Callback
description: Several types of components are installed with activation of the Omnichannel Callback plugin, including user roles, scheduled jobs, and tables.Read/write from the \[sys\_cs\_callback\] table.
locale: en-US
release: australia
product: Omnichannel Callback
classification: omnichannel-callback
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Omnichannel Callback reference, Omnichannel Callback, Manage people and work, Conversational Interfaces]
---

# Components installed with Omnichannel Callback

Several types of components are installed with activation of the Omnichannel Callback plugin, including user roles, scheduled jobs, and tables.

## Scheduled jobs installed

<table id="table_wrn_11n_vvb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Callback Scheduler - Scheduled

</td><td>

Executes the callback task of type Scheduled a minute before the scheduled start time.

</td></tr><tr><td>

Callback Scheduler - ASAP

</td><td>

Executes the callback task of type ASAP after creation of the callback task or at the next retry attempt.

</td></tr><tr><td>

Omnichannel Callback Close expired tasks

</td><td>

Marks the callback tasks as Closed Abandoned in the following scenarios.

-   ASAP callback: If the current time is past the expiry time or the number of callback attempts exceeds the maximum retry attempts.
-   Scheduled callback: When the callback task is not closed one hour after the scheduled end time.

</td></tr></tbody>
</table>## Tables installed

<table id="table_yrn_11n_vvb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Callback Properties

 \[sn\_omni\_callback\_st\_callback\_properties\]

</td><td>

Lists the callback properties that determine the callback behavior.

</td></tr><tr><td>

Callback

 \[sys\_cs\_callback\]

</td><td>

Lists the callback tasks of type Scheduled and ASAP.

</td></tr></tbody>
</table>## Roles installed

To learn more about managing subscriptions, see [Managing per-user subscriptions in Subscription Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/managing-user-subscriptions-v2.md) and contact your account representative.

**Parent Topic:**[Omnichannel Callback reference](../concept/omnichannel-callback-reference.md)

## Callback API role \[sn\_omni\_callback.callback\_api\]

Read/write from the \[sys\_cs\_callback\] table.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

