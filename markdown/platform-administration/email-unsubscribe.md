---
title: Email unsubscribe links
description: Administrators can enable your users to stop receiving particular email messages by adding unsubscribe links to notifications.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Email unsubscribe links

Administrators can enable your users to stop receiving particular email messages by adding unsubscribe links to notifications.

**Note:** Base system notifications include unsubscribe and notification preferences links.

The two types of unsubscribe links are:

-   An unsubscribe link that creates an email message to the instance.
-   An unsubscribe link that opens the notification preferences for the user on the instance.

The available parameter for both of these unsubscribe links is **link\_text**, used to specify the text to display as a link within quotation marks.

<table id="table_e1j_5wv_cx"><thead><tr><th>

Unsubscribe type

</th><th>

Macro used

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Unsubscribe by email

 \(Unauthenticated\)

</td><td>

$\{NOTIF\_UNSUB\}

</td><td>

The system generates an HTML **mailto** hyperlink. When users select the link, their browser or email client creates a preformatted unsubscribe email message to the instance.

</td></tr><tr><td>

Unsubscribe by notification preferences

 \(Authenticated\)

</td><td>

$\{NOTIF\_PREFS\}

</td><td>

The system generates an instance link directly to the notification preferences for this notification type.

</td></tr></tbody>
</table>Administrators can add unsubscribe macros to the following notification record types:

-   Email layouts
-   Email templates
-   Email notifications

## Unsubscribe by email

You can enable users to unsubscribe from emails either by using the list unsubscribe header or a preformatted email message.

-   **Unsubscribe using list unsubscribe header**

    Unsubscribing from email notification using the list unsubscribe header provides users with an unsubscribe link that appears next to the email address. It sends an unsubscribe request and a preformatted email message is automatically sent.

    **Note:** The unsubscribe option or the placement of the button can vary based on the email client being used.

-   **Unsubscribe with preformatted email message**

    Unsubscribing by email requires the user email client or browser to create a preformatted email message containing the following elements:

    -   The **To** field includes the email address of the instance.
    -   The **Subject** starts with the string **Unsubscribe from**.
    -   The **Body** has a JSON string with a name-value pair consisting of **Unsubscribe** and an array value that contains two more name-value pairs.
        -   The **notification\_id** parameter specifies the sys\_id of the notification that the user wants to unsubscribe from.
        -   The **unsub\_token** parameter specifies an instance ID that the system uses to verify that the email came from a ServiceNow instance.

**Note:** Some email clients and web browsers, such as Gmail on Chrome, require extra client configuration to support mailto hyperlinks. Administrators can provide an alternative unsubscribe method for users whose email client or browser doesn’t support mailto links.

The **Unsubscribe from Notification** inbound action processes the email and unsubscribes the sender from the listed notification. Unsubscribing by email message doesn’t require users to authenticate with the instance first.

For translation-enabled emails, if the unsubscribe option does not work, follow these steps:

1.  Create a system property named **glide.email.translation.unsubscribe.prefix** and set it to **true**. Enabling this property adds the prefix **\[UNSUB\] :** to the preformatted email subject line.
2.  Activate the **Unsubscribe from Translated Notifications** inbound email action, or update the existing **Unsubscribe from Notification** inbound email action to include the **\[UNSUB\] :** prefix in the subject line using conditions or a script.

**Note:** Users with multiple subscribed email addresses who unsubscribe from the primary email address are automatically unsubscribed from all other email addresses. Unsubscribing through secondary email addresses is supported beginning with the Xanadu release. The request is fulfilled only for that secondary email address.

## Unsubscribe by notification preferences

Unsubscribe by notification preferences requires the user's browser to navigate to the notification preferences page on the instance. After logging in, the system displays the notification preferences for this particular notification.

You can set preferences for this notification such as disabling notifications for a particular device and save the notification preferences for changes to take effect.

## Unsubscribe links

This email layout adds several unsubscribe links to the bottom of each email notification.

```
${NOTIF_UNSUB} from this notification by email or ${NOTIF_UNSUB+link_text="click
      here"}.
Manage your ${NOTIF_PREFS} or ${NOTIF_PREFS+link_text="click here"}.
```

When rendered in an email notification, the unsubscribe links display only the link text.

![An email wiith unsubscribe and notification preferences links.](../image/example-unsubscribe-links.png "Sample email with unsubscribe links")

If the **Unsubscribe** link is selected, the email client creates a message similar to the one shown in the following figure.

![An email that shows how the email client works after the unsubscribe link is selected.](../image/example-unsubscribe-by-email.png "Sample unsubscribe by email message")

**Parent Topic:**[Create an email notification](../task/t_CreateANotification.md)

