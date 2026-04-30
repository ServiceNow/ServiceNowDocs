---
title: Inbound email actions
description: Define an inbound email action to script how the system responds to an inbound email.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Inbound email actions, Inbound email, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Inbound email actions

Define an inbound email action to script how the system responds to an inbound email.

**Note:** Inbound email flows take priority over inbound email actions. If you create flows with inbound email triggers, emails are first processed by the inbound email triggers before they are processed by inbound email actions.

Inbound email actions are similar to business rules: both use conditions and scripts that take action on a target table. An inbound email action checks the email for a watermark that associates it with a task and checks for other conditions. If the conditions are met, the system takes the inbound email action that you configure. The system can take two types of actions:

-   Record action: setting a value for a field in the target table.
-   Email reply: sending an email back to the source that triggered the action.

By default, if an email has no identifiable watermark, an inbound email action attempts to create an incident from the message. If the email has a watermark of an existing incident, an inbound email action updates the existing incident according to the action's script.

## Inbound email receive types

The system classifies all incoming email into one of three types: forward, reply, or new.

<table id="table_pzp_cx2_bx"><thead><tr><th>

Order

</th><th>

Type

</th><th>

Criteria

</th></tr></thead><tbody><tr><td>

1

</td><td>

Forward

</td><td>

The system classifies an email as a forward only when it meets all these criteria:

-   The subject line contains a recognized forward prefix such as **FW:**.
-   The email body contains a recognized forward string such as **From:**.

 The system classifies any email that meets these criteria as a forward, even if the message contains a watermark or record number that otherwise classifies it as a reply.

</td></tr><tr><td>

2

</td><td>

Reply

</td><td>

The system classifies an email as a reply when it fails to match it to the forward receive type and it meets any one of these criteria:-   The subject line or email body contains a recognized watermark such as **Ref:MSG0000008**.
-   There is no watermark and the subject line contains a recognized reply prefix such as **RE:** and a recognized record number such as **INC0005574**
-   There is no watermark and the Reply-To header contains a recognized message ID of an email with watermark.

</td></tr><tr><td>

3

</td><td>

New

</td><td>

The system classifies an email as new when it fails to match it to the forward and reply receive types.

</td></tr></tbody>
</table>**Note:** From Paris release and beyond, if an email body has multiple watermarks, the last watermark in the email body is considered.

![Flowchart showing how the system determines the type of incoming email as forward, reply, or new](../image/inbound-action-type.png "Determining the type of incoming email")

## Attachments

If an inbound email contains one or more email attachments, the inbound email action adds the attachments to the first record the action produces.

## Character encoding

-   If the email encoding is ASCII-7 or UTF-8, inbound email actions preserve the character encoding in any associated task records they produce.
-   If the email encoding is ISO-8859-1, the inbound email action attempts to convert the email to Windows 1252.
-   Inbound email actions convert any other encodings \(for example, Mac OS Roman\) to plain text, which may or may not be readable.

See the [System email log and mailboxes](../../time/reference/r_EmailLogs.md) for examples of what you might see if a notification or inbound email action is not processed.

**Note:** The state of all incoming emails that have been run against inbound email actions, even if there is no matching action, is changed to **Processed**.

## Domain separation

The system ignores the domain that the inbound email action record is in when it creates a record based on the inbound email action. Keep inbound actions in the global domain. For example, if your inbound email action creates an incident, the system creates the incident in the same domain as the user in the **Caller** field. If that user is not in the User \[sys\_user\] table, the incident is in the global domain.

**Parent Topic:**[Inbound email actions](actions-inbound-email.md)

**Related topics**  


[Notification variables](notification-variables.md)

[Watermarks on notification emails](c_WorkingWithWatermarks.md)

