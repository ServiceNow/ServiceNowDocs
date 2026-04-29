---
title: Email Notification API - ServiceNow Fluent
description: The Email Notification API defines notifications \[sysevent\_email\_action\] that send automated emails based on database operations, custom events, or manual triggers.Create an email notification \[sysevent\_email\_action\] specifying when to send it, who receives it, what it contains, and if it can be delivered in an email digest.Configure the conditions that must be met for the notification to be sent.Configure the contents of an email notification.Configure the contents of an email digest that summarizes the activity for a selected notification and its target records during a specified time interval.Configure who receives an email notification.
locale: en-US
release: australia
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 15
keywords: [servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api]
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Email Notification API - ServiceNow Fluent

The Email Notification API defines notifications \[sysevent\_email\_action\] that send automated emails based on database operations, custom events, or manual triggers.

**Note:** For the latest ServiceNow Fluent API documentation and examples, see the [ServiceNow Fluent API reference](https://servicenow.github.io/sdk/) and [ServiceNow SDK examples repository](https://github.com/ServiceNow/sdk-examples) on GitHub.

For general information about email notifications, see [Email and SMS notifications](https://www.servicenow.com/docs/access?context=c_EmailNotifications&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## EmailNotification object

Create an email notification \[sysevent\_email\_action\] specifying when to send it, who receives it, what it contains, and if it can be delivered in an email digest.

For general information about creating email notifications, see [Create an email notification](https://www.servicenow.com/docs/access?context=t_CreateANotification&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

<table id="table_yys_jdh_33c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

table

</td><td>

Reference or String

</td><td>

Required. The variable identifier or name of a table to which the notification applies. To define a table, use the [Table API - ServiceNow Fluent](table-api-now-ts.md#).**Note:** Don’t select the Task \[task\] table, which is for extending other tables. Notifications that run on the Task table directly aren’t supported.

</td></tr><tr><td>

triggerConditions

</td><td>

Object

</td><td>

Required. The conditions that trigger the notification. For more information, see [triggerConditions object](fluent-email-notification-api.md#).

</td></tr><tr><td>

name

</td><td>

String

</td><td>

A unique name for the email notification.

</td></tr><tr><td>

description

</td><td>

String

</td><td>

A description of the purpose of the email notification.

</td></tr><tr><td>

category

</td><td>

Reference or String

</td><td>

The variable identifier or name of a notification category for grouping notifications. To define a notification category, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).Default: The default email category \(c97d83137f4432005f58108c3ffa917a\)

</td></tr><tr><td>

notificationType

</td><td>

String

</td><td>

The type of notification.Valid values:

-   email: A standard email.
-   vcalendar: A meeting invitation. Meeting invitations aren't supported with email digests.

Default: email

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the notification is active.Default: true

</td></tr><tr><td>

mandatory

</td><td>

Boolean

</td><td>

Flag that indicates whether the notification is required.Default: false

</td></tr><tr><td>

enableDynamicTranslation

</td><td>

Boolean

</td><td>

Flag that indicates whether to enable dynamic translation for the notification.Default: false

</td></tr><tr><td>

emailContent

</td><td>

Object

</td><td>

The email content and formatting. For more information, see [emailContent object](fluent-email-notification-api.md#).

</td></tr><tr><td>

recipientDetails

</td><td>

Object

</td><td>

The email recipients. For more information, see [recipientDetails object](fluent-email-notification-api.md#).

</td></tr><tr><td>

digest

</td><td>

Object

</td><td>

The email digest content and formatting. For more information, see [digest object](fluent-email-notification-api.md#).

</td></tr><tr><td>

$meta

</td><td>

Object

</td><td>

Metadata for the application metadata.With the installMethod property, you can map the application metadata to an output directory that loads only in specific circumstances.

```javascript
$meta: {
      installMethod: 'String'
}
```

Valid values for installMethod:

-   demo: Outputs the application metadata to the `metadata/unload.demo` directory to be installed with the application when the **Load demo data** option is selected.
-   first install: Outputs the application metadata to the `metadata/unload` directory to be installed only the first time an application is installed on an instance.

</td></tr></tbody>
</table>```javascript
import { EmailNotification } from '@servicenow/sdk/core'

EmailNotification({
    table: 'incident',
    name: 'Custom Event Notification',
    description: 'Triggered by custom event',
    category: 'c97d83137f4432005f58108c3ffa917a',  // Default email category sys_id
    triggerConditions: {
        generationType: 'event',
        eventName: 'custom.incident.escalated',
        order: 100
    },
    recipientDetails: {
        recipientUsers: ['6816f79cc0a8016401c5a33be04be441'],  // Admin user sys_id
        eventParm1WithRecipient: true,  // Event param 1 contains recipient
        isSubscribableByAllUsers: true
    },
    emailContent: {
        contentType: 'text/html',
        subject: 'Incident Escalated',
        messageHtml: '<p>An incident has been escalated.</p>'
    }
})
```

## triggerConditions object

Configure the conditions that must be met for the notification to be sent.

**Note:** If the same trigger generates multiple notifications, the system sends only one notification. The system considers all other notifications, even if they have a different subject and body, as duplicates. The Ignore Duplicates business rule controls this functionality.

<table id="table_fhs_wfh_33c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

generationType

</td><td>

String

</td><td>

Required. The method of triggering the email notification.Valid values:

-   engine: Sends the notification when a record is inserted or updated.
-   event: Sends the notification when custom events occur.
-   triggered: Manually triggered notifications. The following properties don't apply if this property is set to `triggered`.

</td></tr><tr><td>

onRecordInsert

</td><td>

Boolean

</td><td>

Flag that indicates whether to send the notification when a record is inserted. **Note:** Either this property or the onRecordUpdate property must be true.

Default: false

</td></tr><tr><td>

onRecordUpdate

</td><td>

Boolean

</td><td>

Flag that indicates whether to send the notification when a record is updated.**Note:** Either this property or the onRecordInsert property must be true.

Default: false

</td></tr><tr><td>

eventName

</td><td>

String

</td><td>

The name of a custom event to trigger sending the notification.This property is required if the value of the generationType property is `event`.

</td></tr><tr><td>

affectedFieldOnEvent

</td><td>

String

</td><td>

The event parameter that contains the affected field.This property applies only if the generationType property is set to `event`.

Valid values:

-   parm1
-   parm2

</td></tr><tr><td>

weight

</td><td>

Number

</td><td>

The notification priority relative to duplicate notifications.Notifications that have the same target table and recipients are considered duplicates if the weights are different. If weights are same, an additional evaluation is done to check if the subject and the body \(excluding watermark\) are the same to qualify as duplicate notification. When there are duplicate notifications, the system only sends the notification with the highest weight. All other notifications are moved from the Outbox to the Skipped mailbox. The default value of 0 causes the system to send the notification \(assuming the conditions are met\).

Maximum value: 1000

Default: 0

</td></tr><tr><td>

condition

</td><td>

String

</td><td>

A filter query that specifies the fields and values that must be true for users to access the object. For more information, see [Operators available for filters and queries](https://www.servicenow.com/docs/access?context=r_OpAvailableFiltersQueries&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

advancedCondition

</td><td>

String

</td><td>

A JavaScript conditional statement that must return true or set a global answer variable to true to send the notification. For more information, see [Advanced conditions for email notifications](https://www.servicenow.com/docs/access?context=c_OptSpecifyingAdvancedCond&version=australia&pubname=australia-platform-administration&ft:locale=en-US).**Note:** This property is evaluated in addition to other conditions that you set on the notification. Both the condition and advanced condition must evaluate to true to send the notification.

</td></tr><tr><td>

itemTable

</td><td>

Reference or String

</td><td>

The variable identifier or name of the table to which the notification item refers. To define a table, use the [Table API - ServiceNow Fluent](table-api-now-ts.md#).

</td></tr><tr><td>

item

</td><td>

String

</td><td>

The item to use for the notification context.

</td></tr><tr><td>

order

</td><td>

Number

</td><td>

The execution order of the notification.Maximum value: 9999

Default: 100

</td></tr></tbody>
</table>```javascript
triggerConditions: {
    generationType: "engine",
    onRecordInsert: false,
    onRecordUpdate: true,
    weight: 100,
    condition: "priority=1^ORpriority=2^state!=6^state!=7", // High/Critical priority, not resolved/closed
    order: 100
}
```

## emailContent object

Configure the contents of an email notification.

<table id="table_fhs_wfh_33c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

contentType

</td><td>

String

</td><td>

The type of email content. Valid values:

-   text/html
-   text/plain
-   multipart/mixed

Default: text/html

</td></tr><tr><td>

template

</td><td>

Reference or String

</td><td>

The variable identifier or sys\_id of an email template \[sysevent\_email\_template\]. To define an email template, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).You can only specify an email template that meets one of the following conditions:

-   The template has the same scope and table as the notification.
-   The template has the same scope but has no specified table.
-   The template has the same table and is in the global scope.

</td></tr><tr><td>

style

</td><td>

Reference or String

</td><td>

The variable identifier or sys\_id of an email style \[sys\_email\_style\]. To define an email style, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).

</td></tr><tr><td>

subject

</td><td>

String

</td><td>

A subject line for the email. If empty, the system uses the Subject value from the email template.You can use the `\${variable}` format for variable references. Variables map to column names available from the notification table, its parent tables, and reference tables. Use variables to include values from a record in the table, such as the short description or comments and work notes.

</td></tr><tr><td>

smsAlternate

</td><td>

String

</td><td>

A notification message to send specifically to SMS devices. The SMS alternate message is limited to 140 characters. If empty, the system uses the SMS alternate value from the email template.You can use the `\${variable}` format for variable references. Variables map to column names available from the notification table, its parent tables, and reference tables. Use variables to include values from a record in the table, such as the short description or comments and work notes.

</td></tr><tr><td>

importance

</td><td>

String

</td><td>

The level of importance of the message. Valid values:

-   low
-   high

</td></tr><tr><td>

includeAttachments

</td><td>

Boolean

</td><td>

Flag that indicates whether to include attachments from the notification trigger record with the email.Default: false

</td></tr><tr><td>

omitWatermark

</td><td>

Boolean

</td><td>

Flag that indicates whether to omit the watermark attached to each email. For more information, see [Watermarks on notification emails](https://www.servicenow.com/docs/r/7LhbZn3yz3Q58qhjZoU9iQ/kTwHRtaHawJF_Sz_AA_tnA).Default: false

</td></tr><tr><td>

from

</td><td>

String

</td><td>

The email address from which to send the notification.

</td></tr><tr><td>

replyTo

</td><td>

String

</td><td>

The email address to which recipients can reply.

</td></tr><tr><td>

pushMessageOnly

</td><td>

Boolean

</td><td>

Flag that indicates whether to send the notification only as a push notification to a mobile device.Default: false

</td></tr><tr><td>

pushMessageList

</td><td>

Array

</td><td>

A list of variable identifiers or sys\_ids of push messages \[sys\_push\_notif\_msg\] to associate with the notification. To define a push notification, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).**Note:** The push message and notification must be for the same table.

</td></tr><tr><td>

forceDelivery

</td><td>

Boolean

</td><td>

Flag that indicates whether to bypass user notification preferences that would prevent a notification and send the notification anyway.Default: false

</td></tr><tr><td>

messageHtml

</td><td>

String

</td><td>

The HTML content of the notification message. If empty, the system uses the message HTML from the email template.You can use the `\${variable}` format for variable references. Variables map to column names available from the notification table, its parent tables, and reference tables. Use variables to include values from a record in the table, such as the short description or comments and work notes.

This property is required if the value of the contentType property is `text/html` or `multipart/mixed`.

</td></tr><tr><td>

messageText

</td><td>

String

</td><td>

The plain text content of the notification message. If empty, the system uses the message text from the email template.You can use the `\${variable}` format for variable references. Variables map to column names available from the notification table, its parent tables, and reference tables. Use variables to include values from a record in the table, such as the short description or comments and work notes.

This property is required if the value of the contentType property is `text/plain` or `multipart/mixed`.

</td></tr><tr><td>

message

</td><td>

String

</td><td>

Deprecated. Message contents.

</td></tr></tbody>
</table>```javascript
emailContent: {
    contentType: "text/html",
    subject: "CRITICAL: Incident \${number} - \${short_description}",
    messageHtml: `
            <div style="background-color: #ff4444; color: white; padding: 10px; border-radius: 5px;">
                <h2>CRITICAL INCIDENT ALERT</h2>
                <p><strong>Incident:</strong> \${number}</p>
                <p><strong>Priority:</strong> \${priority}</p>
                <p><strong>Description:</strong> \${short_description}</p>
                <p><strong>Assigned To:</strong> \${assigned_to.name}</p>
                <p><strong>Created:</strong> \${sys_created_on}</p>
                <p><a href="\${instance_url}/incident.do?sys_id=\${sys_id}" style="color: #ffffff; text-decoration: underline;">View Incident</a></p>
            </div>
        `,
    smsAlternate:
      "CRITICAL: Incident \${number} - \${short_description}. Priority: \${priority}. Assigned: \${assigned_to.name}",
    pushMessageList: ["mobile_push_notification_sys_id"], 
    forceDelivery: true, 
    importance: "high"
}
```

## digest object

Configure the contents of an email digest that summarizes the activity for a selected notification and its target records during a specified time interval.

For general information about email digests, see [Email digests](https://www.servicenow.com/docs/access?context=email-digests&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

<table id="table_fhs_wfh_33c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

allow

</td><td>

Boolean

</td><td>

Flag that indicates whether users to receive this notification as a digest. If false, all other properties of the digest object are ignored.Default: false

</td></tr><tr><td>

default

</td><td>

Boolean

</td><td>

Flag that indicates whether digest mode is enabled by default for this notification.Default: false

</td></tr><tr><td>

type

</td><td>

String

</td><td>

The type of digest. Valid values:

-   single: Sends the notification in an email digest when it’s triggered multiple times during the selected interval for a single target record, for example INC001 only.
-   multiple: Sends the notification in an email digest when it’s triggered multiple times during the selected interval for a multiple target record, for example INC001, INC002, and more.

</td></tr><tr><td>

defaultInterval

</td><td>

Reference or String

</td><td>

The variable identifier or sys\_id of a digest interval \[sys\_email\_digest\_interval\] to use as the default time interval for digest delivery. To define a digest interval, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).

</td></tr><tr><td>

subject

</td><td>

String

</td><td>

A subject line for the email digest. If empty, the system uses the Subject value from the email template.You can use the `\${variable}` format for variable references. Variables map to column names available from the notification table, its parent tables, and reference tables. Use variables to include values from a record in the table, such as the short description or comments and work notes.

</td></tr><tr><td>

html

</td><td>

String

</td><td>

The HTML content of the email digest. You can use the `\${variable}` format for variable references. Variables map to column names available from the notification table, its parent tables, and reference tables. Use variables to include values from a record in the table, such as the short description or comments and work notes.

</td></tr><tr><td>

text

</td><td>

String

</td><td>

The plain text content of the email digest. You can use the `\${variable}` format for variable references. Variables map to column names available from the notification table, its parent tables, and reference tables. Use variables to include values from a record in the table, such as the short description or comments and work notes.

</td></tr><tr><td>

template

</td><td>

String

</td><td>

The variable identifier or sys\_id of an email template \[sysevent\_email\_template\]. To define an email template, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).

</td></tr><tr><td>

separatorHtml

</td><td>

String

</td><td>

An HTML separator that appears between each item summarized in the digest.You can use the `\${variable}` format for variable references. Variables map to column names available from the notification table, its parent tables, and reference tables. Use variables to include values from a record in the table, such as the short description or comments and work notes.

Default: `<p>&nbsp;</p>\n<hr>\n<p>&nbsp;</p>`

</td></tr><tr><td>

separatorText

</td><td>

String

</td><td>

A plain text separator that appears between each item summarized in the digest.You can use the `\${variable}` format for variable references. Variables map to column names available from the notification table, its parent tables, and reference tables. Use variables to include values from a record in the table, such as the short description or comments and work notes.

Default: `--------------------------------------------------------------------------------\n`

</td></tr><tr><td>

from

</td><td>

String

</td><td>

The email address from which to send the notification.

</td></tr><tr><td>

replyTo

</td><td>

String

</td><td>

The email address to which recipients can reply.

</td></tr></tbody>
</table>```javascript
digest: {
    allow: true,
    defaultInterval: hourlyDigest,
    template: escalationTemplate,
    subject: "Incident Escalation Digest - \${digest_count} incidents require attention",
    html: `<div>
           <div>Incident Escalation Digest</div>
           </div>`,
    separatorHtml: '<hr style="margin: 15px 0;">',
    from: "noreply@company.com",
    replyTo: "itsupport@company.com"
}
```

## recipientDetails object

Configure who receives an email notification.

Notification recipients must be active users defined as active users in the User \[sys\_user\] table. They must also have a valid email address defined for their primary channel \(device\) in the Notification Device \[cmn\_notif\_device\] table. Your notification recipients must also have the appropriate notification preferences enabled.

<table id="table_fhs_wfh_33c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

recipientUsers

</td><td>

Array

</td><td>

A list of variable identifiers or sys\_ids of users \[sys\_user\] or a list of email addresses to receive the notification. To define a user, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).

</td></tr><tr><td>

recipientFields

</td><td>

Array

</td><td>

A list of fields that reference the users or user groups to receive the notification. The fields must be reference fields.For example, if a notification uses the Incident \[incident\] table, you can specify the `opened_by` field to send the notification to users or groups who opened the incident. This list of users or groups is variable and depends on the values of the associated task record. You can also select a field that includes an email address string to send a notification to that address.

</td></tr><tr><td>

recipientGroups

</td><td>

Array

</td><td>

A list of variable identifiers or sys\_ids of user groups \[sys\_user\_group\] to receive the notification. To define a user group, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).**Note:** Group members receive individual notifications only if **Include members** is selected in the group record.

</td></tr><tr><td>

excludeDelegates

</td><td>

Boolean

</td><td>

Flag that indicates whether to exclude delegated users. Set this property to true to help prevent the instance from sending email notifications to delegates of the users and members of the groups you selected.Default: false

</td></tr><tr><td>

isSubscribableByAllUsers

</td><td>

Boolean

</td><td>

Flag that indicates whether to allow all users to subscribe to the notification. For more information, see [Subscription-based notifications](https://www.servicenow.com/docs/access?context=c_SubscriptionBasedNotifications&version=australia&pubname=australia-platform-administration&ft:locale=en-US).**Note:** If the record contains sensitive or protected data, consider restricting the recipient list only to those users and groups who normally have access to it, leaving the value of this property as false. You can also configure your notification content so that private or sensitive data isn’t exposed. For example, you could insert a link back to the associated record, so that details aren’t revealed in the notification.

Default: false

</td></tr><tr><td>

sendToCreator

</td><td>

Boolean

</td><td>

Flag that indicates whether to send the notification to the person who performed the action that started the notification process, if the person is also a recipient. If the event creator isn’t specified in one of the recipient fields, the event creator doesn’t receive a notification regardless of the setting in this field.Default: false

</td></tr><tr><td>

eventParm1WithRecipient

</td><td>

Boolean

</td><td>

Flag that indicates whether the event parameter 1 contains one or more notification recipients.This property only applies to event-based notifications.

</td></tr><tr><td>

eventParm2WithRecipient

</td><td>

Boolean

</td><td>

Flag that indicates whether the event parameter 2 contains one or more notification recipients.This property only applies to event-based notifications.

</td></tr></tbody>
</table>```javascript
recipientDetails: {
    recipientGroups: ["d625dccec0a8016700a222a0f7900d06"], // IT Support group sys_id
    recipientFields: ["assigned_to", "caller_id"],
    sendToCreator: false,
    isSubscribableByAllUsers: false
}
```

