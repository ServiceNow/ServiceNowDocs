---
title: Notifications
description: After the data model is defined and users are able to interact with the application, determine how the application should communicate with users. Configure notifications to alert users to important application related events, share application information in the knowledge base, and add translations to allow users to interact with the application in their native language.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create design elements, Build your application, Exploring professional development, Building pro-code applications, Developing your application, Building applications]
---

# Notifications

After the data model is defined and users are able to interact with the application, determine how the application should communicate with users. Configure notifications to alert users to important application related events, share application information in the knowledge base, and add translations to allow users to interact with the application in their native language.

The ServiceNow AI Platform can notify users by email, SMS text message, or push notifications.

## Triggers: Event Driven Notifications vs Table Updates

Configure notifications to trigger based on updates to a table or based on an event. Use event-based triggering when triggering requirements cannot be easily implemented in the notification conditions or when the notification is triggered from a Workflow. Creating specific events also enables easier notification debugging.

Use the Notification activity in a workflow or the Send an email action in Flow Designer for simple notification use cases. For complex or critical notifications, trigger an event from a workflow or a Flow Designer flow and configure a notification to fire off that event.

## Notification Content

ServiceNow notifications support static and dynamic content using email templates, email scripts, and notification variables.

[Notification variables](https://servicenow.com/docs/bundle/paris-servicenow-platform/page/administer/notification/concept/notification-variables.html) add dynamic information to the body of a notification, such as field values from the base record. The variables also support dot-walking, which allows field values from any related records to be included in the content without scripting.

For example, use the URI\_REF variable to point to the record that originated the email.

Use [email scripts](https://servicenow.com/docs/bundle/paris-servicenow-platform/page/script/server-scripting/concept/c_ScriptingForEmailNotifications.html) or dot-walk from the base record to include dynamic content that is not available in the record. Use the mail script API to set notification details, such as the recipient and sender addresses, etc.

**Note:** Scripts entered in the notification body using &lt;mail\_script&gt; tags may not always work correctly. Always create email scripts at System Notifications &gt; Email &gt; Notification Email Script and include them in the notification body with $\{mail\_script:script\_name\}.

Create [email templates](https://servicenow.com/docs/bundle/paris-servicenow-platform/page/administer/notification/concept/c_EmailTemplates.html) for content used in multiple notifications. Adding the content to an email template enables administrators to create reusable content for the subject line and message body of email notifications.

## Configure recipients

ServiceNow emails can be sent to users, groups, or individual email addresses. When sending to groups, check the **Include members** field on the group record for the notification to be sent to all members of the group in addition to the group email.

[Subscription-based notifications](https://servicenow.com/docs/bundle/paris-servicenow-platform/page/administer/notification/concept/c_SubscriptionBasedNotifications.html) - Select the **Subscribable** option on the notification to allow recipients to pick and choose the emails they want to receive.

For a subscription-based notification, the [Mandatory](https://servicenow.com/docs/bundle/paris-servicenow-platform/page/administer/notification/task/t_MakingANotificationMandatory.html) option can be set to true for the recipients to receive the notification regardless of their individual preferences. Optionally, configure [unsubscribe links](https://servicenow.com/docs/bundle/paris-servicenow-platform/page/administer/notification/concept/email-unsubscribe.html) in the outgoing email to allow users to remove themselves from the notification.

ServiceNow uses email watermarks to correctly process user responses to notifications. Email notifications automatically include watermarks unless the **Omit watermark** option is selected in the notification. Omit watermarks only when no email response is expected from the recipients.

The [Troubleshooting Outbound Email](https://hi.service-now.com/kb_view.do?sysparm_article=KB0521382) knowledge base article provides troubleshooting steps for the most common notification issues. Log in to the HI portal \([https://hi.service-now.com](https://hi.service-now.com/)\) to access the article.

**Parent Topic:**[Create design elements](create-design-elements.md)

