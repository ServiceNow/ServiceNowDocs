---
title: Email filters
description: Specify which inbound emails to ignore or move to a particular mailbox.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Creating an email account, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Email filters

Specify which inbound emails to ignore or move to a particular mailbox.

When an email is ignored, the email is saved to your instance but is not processed. You can access an ignored email by viewing its Email \[sys\_email\] record.

The Email Filters \(com.glide.email\_filter\) plugin is active by default for releases after Kingston, for releases before Kingston, it needs to be activated, for more information see [Activate email filters](../task/t_ActivateEmailFilters.md).

## Default email filters

By default, the following filters are available from the **System Mailboxes** &gt; **Administration** &gt; **Filters** module:

|Filter|Description|
|------|-----------|
|Ignore VCAL|Ignores all email containing vCalendar requests. This filter prevents [inbound email actions](c_InboundEmailActions.md) from creating unnecessary incident records when the instance receives a response to sent email. vCalendar requests in email responses are identified by the EmailUtils script include.|
|Ignore header|Ignores email that contains specific headers. This filter overrides the **glide.pop3.ignore\_headers** property.|
|Junk email - sender equals recipient|Filters out emails that are from the same user as the SMTP user to the Junk folder.|
|Ignore subject|Ignores email with specific terms or phrases in the subject line. This filter overrides the **glide.pop3.ignore\_subjects** property. This filter might not apply to emails arriving from unknown users. Unknown users can be locked out.|
|Move spam to junk folder|Moves email identified as spam to the Junk folder. This filter checks for the value of the ServiceNow spam header. If the header is `X-ServiceNow-Spam-Status:Yes`, the filter moves the email to the Junk folder|

**Note:** Filter action should be configured to indicate how the system should react when the conditions of this filter evaluate to true. The two choices in the base system are: Mark as Ignored and Move to Junk. You can use the Action script to perform additional email tasks.

To learn more about enabling spam scoring and filtering, see [Email spam scoring and filtering \(instance security hardening\)](https://www.servicenow.com/docs/access?context=sc-email-spam-scoring-and-filtering&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) in Instance Security Hardening Settings.

## Email filter script include

Email filters use a script include called `EmailUtils` that contains a simple utility function to determine if `vCalendar` is in the body of the response email. The results of this query are used in a condition script in the Ignore VCAL email filter.

## Spam scoring and virus scanning

Every message sent through email servers is assessed for the likelihood of being spam. Based on this assessment, the instance adds headers to each message that can be used for filtering within the customer instance using the Email Filters plugin.

The system also adds the `X-ServiceNow-Virus:INFECTED` header to an email that contains one or more virus-infected attachments. The system ignores the email.

Spam scoring and virus scanning are available only for instances that use the ServiceNow email infrastructure. For more information on spam scoring and filtering, see [KB0549426](https://support.servicenow.com/kb_view.do?sysparm_article=KB0549426).

-   **[Create an email filter](../task/t_CreateAnEmailFilter.md)**  
You can create email filters to apply a custom action script or filter actions when email matches your filter's conditions.

**Parent Topic:**[Creating an email account](using-email-admin.md)

**Related topics**  


[Create an email filter](../task/t_CreateAnEmailFilter.md)

