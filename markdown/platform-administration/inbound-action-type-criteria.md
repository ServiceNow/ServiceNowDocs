---
title: Criteria for matching email to inbound actions
description: Default conditions of active inbound actions are used to manage incoming email. Inbound email actions are classified as forward, reply, or new based on subject line, record matching, and email headers
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Inbound email actions, Inbound email, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Criteria for matching email to inbound actions

Default conditions of active inbound actions are used to manage incoming email. Inbound email actions are classified as forward, reply, or new based on subject line, record matching, and email headers

![Flowchart showing how inbound email actions are classified as forward, reply, or new based on subject line, record matching, and email headers](../image/inbound-email-action-type.png "Default matching criteria")

If you customize or deactivate the default inbound actions, the conditions of the active inbound actions are checked. If an inbound action with matching conditions cannot be found, the state is set to Processed.

![Flowchart showing how inbound emails are processed when default inbound email actions are enabled or when an email matches an active inbound email action](../image/processing-email-no-matching-inbound-action.png "Custom matching criteria")

<table id="table_axb_pk4_m4"><thead><tr><th>

Inbound email action type

</th><th>

Required matching criteria

</th><th>

Name of default action \(Incident table\)

</th><th>

Result of default action

</th></tr></thead><tbody><tr><td>

Forward

</td><td>

The email contains the following conditions: -   A subject starting with a recognized forward prefix even if a watermark or an In-Reply-To header is present.
-   From &lt;user email&gt; appears anywhere in the email body.

</td><td>

Create Incident \(Forwarded\)

</td><td>

Create new record

</td></tr><tr><td>

Reply

</td><td>

The email contains one of the following conditions and the table specified in the email matches the table of the inbound action: 1.  A valid watermark that matches an existing record.
2.  A subject line starting with a recognized reply prefix when no watermark is present and a valid record number that matches an existing record.
3.  An In-Reply-To email header when neither a watermark nor a valid record number is present that matches an existing record.
4.  A thread-index in an email header when the email does not meet any of the previous conditions that matches an existing record.

**Note:** To enable thread indexing, create the system property **glide.inbound.email.classify.by.thread\_index** and set it to **true**.

</td><td>

Update Incident \(BP\)

</td><td>

Update existing record

</td></tr><tr><td>

New

</td><td>

The email does not meet the conditions for either a reply or forward type inbound email action

</td><td>

Create Incident

</td><td>

Create new record

</td></tr></tbody>
</table>If more than one inbound action is available for a particular type of email, the instance uses the Table field to match the email to a particular table. If there is also more than one action for the inbound action's table, the instance uses the **Order** field to determine the order in which the actions run.

**Parent Topic:**[Inbound email actions](actions-inbound-email.md)

