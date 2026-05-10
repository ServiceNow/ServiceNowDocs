---
title: Mail script variables
description: Certain variables are available when processing mail\_script scripts.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Scripting for email notifications, Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Mail script variables

Certain variables are available when processing mail\_script scripts.

For examples of mail scripts, see [Example scripting for email notifications](r_ExScptEmlNtfn.md).

<table id="table_psj_g1q_rq"><thead><tr><th>

Variable

</th><th>

Object Description

</th></tr></thead><tbody><tr><td>

template

</td><td>

Handles printing from the mail script to the email message.

 `template.print("message"); //outputs message to the email body.`

 `template.space("number of spaces"); //outputs spaces to the email body.`

</td></tr><tr><td>

email\_action

</td><td>

GlideRecord object for the email notification \(sysevent\_email\_action\).

</td></tr><tr><td>

event

</td><td>

GlideRecord object for the event that fired the notification \(sysevent\).

</td></tr><tr><td>

email

</td><td>

EmailOutbound object

 Available methods:

-   `addAddress(String type, String address, String displayname):` type can be cc or bcc.
-   `setFrom(String address):` override the sender address.
-   `setReplyTo(String address):` override the reply to address.
-   `setSubject(String subject):` override the subject of the message.
-   `setBody(String message):` override the body of the message.

The email address that is passed by `setFrom` and `setReplyTo` needs to be in a valid form such as `helpdesk@sn.com` or `Display Name <helpdesk@sn.com>`. If the email address includes a 'Display Name', then that value overrides the instance's display name.

 For more information, see [GlideEmailOutbound - Scoped](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_GlideEmailOutboundScopedAPI.md).

</td></tr></tbody>
</table>**Parent Topic:**[Scripting for email notifications](../concept/c_ScriptingForEmailNotifications.md)

**Related topics**  


[JavaScript in emails](../concept/c_UseJavaScriptInEmails.md)

[Example scripting for email notifications](r_ExScptEmlNtfn.md)

[Useful attachment scripts](../../useful-scripts/reference/r_UsefulAttachmentScripts.md)

