---
title: Construct an email message with a template
description: Email templates provide a list of the fields from database tables that are available for constructing an email message.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Email templates, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Construct an email message with a template

Email templates provide a list of the fields from database tables that are available for constructing an email message.

An email template can include a **mailto** automatic response link, which enables the email recipient to simply choose a link that sends a preformatted response back to the instance. An example is the email template used for notification that an approval is required. The following example shows the base email:

![The Approval Request notification uses the change.itil.approve.role email template.](../../../administer/notification/image/approval_request_notification.png "Email notification with the template specified")

In this case, when a change request approval is requested, an update is made to the `sysapproval_approval` table. The "approval events" business rule is then executed, which creates the "approval.inserted" event. The "Approval Request" email event is defined to process the approval.inserted event, and this email event is defined to use the following change.itil.approve.role email template. Notice that this template has two mailto: items specified. One for "mailto.approval" and one for "mailto.rejection." This email template builds an automatic response that lets the email receiver simply click a link in the email to either approve or reject the change request.

Here is what the **change.itil.approve.role** template looks like using the rich HTML editor:

![The change.itil.approve.role template specifies the HTML message contents in the approval request email.](../image/EmailTemplateChangeApproval.png "change.itil.approve.role template")

The selection list on the right shows the available fields from the `sysapproval_approver` table.

Notice the **change.itil.approve.role** template also uses a predefined email layout \(Unsubscribe and Preferences\), which provides links for the recipient to unsubscribe from approval notifications and set notification preferences.

And here is the **mailto.approval** template:

![The mailto.approval template defines the approval notification link.](../image/MailtoApprovalTemplate.png "mailto approval template")

**Note:** If you put text on the lines following the **Click here to approve $\{sysapproval\}** line, this text forms the actual body of the email.

The combination of templates used would generate an email similar to the following example:

![The example generated email contains the content determined by the change.itil.approve.role template.](../image/TemplateGeneratedEmailExample.png "Template generated email message")

Notice that the email recipient can use the following links in the mail:

-   A link to view all the details of the change request
-   A link to view the approval record
-   A link that generates an automatic email response to approve the change
-   A link that generates an automatic email response to reject the change
-   A link to unsubscribe from approval notifications and another link to set notification preferences

-   **[Add blank lines in an email template](r_AddBlankLinesInAnEmailTemplate.md)**  
You can easily add blank lines in an email template using HTML tags.

**Parent Topic:**[Email templates](../../../administer/notification/concept/c_EmailTemplates.md)

**Related topics**  


[Email layouts](../../../administer/notification/concept/email-layouts.md)

