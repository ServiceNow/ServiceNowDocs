---
title: Email client
description: Send email directly from any record, such as an incident, change request, or problem record.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Exploring email client, Email client, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Email client

Send email directly from any record, such as an incident, change request, or problem record.

## Using the email client

You can use the email client either from a form or the record view in a workspace.

-   To open the email client from a form, open a record and click the more options menu \(![More options menu](../image/more-options-menu.png)\). Click the email icon \(![Email icon](../image/email_icon.png)\).
-   To open the email client in a workspace, open a record and click the menu icon \(![More UI Actions menu](../../workspace/image/agent-workspace-more-ui-actions-icon.jpg)\). Click **Compose Email**.

The email client looks like a standard email interface, which contains a toolbar for text formatting and adding attachments.

The email client uses the multipart/mixed content type and supports HTML markup in the message body.

**Note:** The **Subject** field on the email client allows a larger character count than the default setting for the **Subject** field on the Email \[sys\_email\] table. If the subject text from the client is being truncated, increase the **Max length** value for the **Subject** field on the Email table.

For more information on using the email client in a workspace, see [Communicating via email in workspace](https://www.servicenow.com/docs/access?context=using-email&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

## Activation information

The email client is activated with the Email Client plugin \(com.glide.email\_client\), which is active by default on the ServiceNow AI Platform.

The email client is enabled by default on the incident table. To enable the email client for another table, add the **email\_client** dictionary attribute on the table's collection record. For more information, see [Enable the email client for a table](../task/enable-email-client.md).

The email client is enabled by default on the change table.

Give users access to the email client by assigning them the email\_composer role.

## More setup

You can configure the email client by creating an Email Client Configuration \[sys\_email\_client\_configuration\] record. For more information, see [Email client configurations](email-client-configuration.md).

You can also create email client templates or quick messages to use predefined content in email client messages. For more information, see the following:

-   [Create an email client template](../task/t_CreateAnEmailClientTemplate.md#)
-   [Composing emails with quick messages](quick-message.md)

Optionally, you can give users the option to send email client messages as SMS text messages. For more information, see [Enable SMS delivery with the email client](../reference/r_EnableTheSMSDeliveryOption.md).

