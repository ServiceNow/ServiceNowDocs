---
title: Composing emails with quick messages
description: Insert predefined content into the message body of emails that you send from the email client.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Email client, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Composing emails with quick messages

Insert predefined content into the message body of emails that you send from the email client.

## Using quick messages

In the email client, you can select a quick message to fill the email body with the content that is specified in the quick message. After you define one or more quick messages, the Quick Message selector appears in the email client so that you can construct an email with multiple quick messages.

By default, the quick message content is inserted at the place of the cursor. It doesn't replace the content that you created before selecting the quick message. To replace message content with a quick message, highlight the text to replace and then select a quick message.

**Note:** To instead have quick message content replace all existing content in an email draft, set the **glide.email\_client.quick\_message.insert** property to **false**.

![Adding quick messages](../image/quick-message-demo.gif "Adding quick messages to an email")

## Creating quick message content

Define quick messages by creating records in the Email Client Canned Messages \[sys\_email\_canned\_message\] table.

When you define a quick message, you can add any of the following types of content into the message body:

-   Icons
-   Logos
-   Pictures
-   Rich-text HTML
-   Hyperlinks
-   Variables
-   Any other HTML constructs

**Note:** If you add attachments to the quick message, the attachments aren’t sent as part of the email distribution.

Assign the email\_client\_quick\_message\_author role to business managers so that they can create quick messages for users in their group.

## Setting quick message conditions

When you define a quick message, you can limit the availability of the quick message according to:

-   The user who launches the email client
-   The group of the user who launches the email client
-   The table of the record from which you launch the email client
-   The target record from which you launch the email client

For example, if you designate Beth Anglin as the user for a certain quick message, the quick message is available in the email client only for Beth Anglin.

If you associate a quick message to the Incident \[incident\] table, the quick message is available in the email client only after you launch from an incident record. If you specify a target record from the Incident table for the quick message, the quick message becomes available in the email client only for matching incident records.

-   **[Define a quick message](../task/t_QuickMessages.md)**  
Create predefined content to add in the email client so that users can write emails consistently and efficiently.

**Parent Topic:**[Configure email client](configuring-email-client.md)

