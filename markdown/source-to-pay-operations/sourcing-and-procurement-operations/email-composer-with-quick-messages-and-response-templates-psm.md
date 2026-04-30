---
title: Email composer with quick messages and response templates in Source-to-Pay Workspace
description: Insert predefined content into the message body of emails that you send from the email client in Source-to-Pay Workspace.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Procurement Case Management, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Email composer with quick messages and response templates in Source-to-Pay Workspace

Insert predefined content into the message body of emails that you send from the email client in Source-to-Pay Workspace.

You can use this feature to send emails for all procurement objects, which include purchase requisitions, sourcing requests, negotiations, sourcing events, procurement cases, and tasks. To open the email client, select **Compose Email** from the More Actions icon on the procurement object. A draft email appears with pre-populated data in the **To**, **Subject**, and email body fields.

## Using quick messages

In the email client, you can select a quick message to fill the email body with the content that is specified in the quick message. After you define one or more quick messages, the Quick Messages contextual pane appears in the email client so that you can draft an email with a quick message of your choice. For Sourcing and Procurement Operations, Disclaimer is the only default quick message provided.

On selecting **Insert**, the quick message content is inserted at the place of the cursor. It doesn't replace the content that you created before selecting the quick message. To replace existing content with a quick message, highlight the text to replace and then select a quick message.

## Creating quick message content

Define quick messages by creating records in the Email Client Canned Messages \[sys\_email\_canned\_message\] table.

When you define a quick message, you can add any of the following types of content into the message body:

-   Icons
-   Logos
-   Images
-   Rich-text HTML
-   Hyperlinks
-   Variables
-   Any other HTML constructs

Assign the email\_client\_quick\_message\_author role to business managers so that they can create quick messages for users in their group.

For more information on how to create a quick message, see [Define a quick message](https://www.servicenow.com/docs/access?context=t_QuickMessages&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Using response templates

Resolve cases faster and more efficiently with response templates. Response templates are reusable messages that can be copied to draft emails to provide quick and consistent messages to users. Each template is associated with a table that is an extension of the Task \[task\] or Interaction \[interaction\] table. Response templates include a short name for specifying a shortcut that can be used to identify the message.

Open the response template that you want to use for your email and select **Copy to clipboard**. You can now paste the contents of this template at the place of the cursor. It doesn't replace the content that you created before selecting the response template. To replace existing content with a response template content, highlight the text to replace and then select a response template.

By default, the following response templates are provided for these standard procurement objects:

-   Procurement case: Standard closure response, procurement contacts, policy instructions, and additional information.
-   Purchase requisition: Placing of purchase order is in process, procurement contacts, and policy instructions.
-   Sourcing request: Placing of purchase order is in process, procurement contacts, and policy instructions.
-   Negotiation: Procurement contacts, and policy instructions.
-   Sourcing event: Procurement contacts, and policy instructions.
-   Task: Procurement contacts, and policy instructions.

While users with the response template reader \[sn\_templated\_snip.template\_snippet\_reader\] role can only read response template content, those with the response template writer \[sn\_templated\_snip.template\_snippet\_writer\] role can read, create, update, and delete response template content.

For more information on how to work with response templates, see [Create or modify a response template](https://www.servicenow.com/docs/access?context=create-modify-templated-snippet&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

## Emailed message in activity log

After your email is composed, sent, and most importantly received by the intended recipient, you can see the email message in the **Activity** section of the procurement object record. You can continue to work with this email from the activity log by replying to or forwarding the email as required.

## Email composer setup configurations

To view email composer and all its associated features, which include viewing your emailed message in the activity log, verify that you have the following configurations in place:

-   Sent email should be in Received state, for the email log to show up in the activity stream of the procurement object.
-   The formatter update of the activity stream of the procurement objects should have the **Emails - autogenerated** and **Emails - correspondence** formats applied.
-   The Email client attribute should be updated to the procurement object type, for the email composer feature to be enabled for that object.
-   The email\_composer role should be added as a contained role for the base fulfiller or agent \[sn\_spend\_sdc.agent\] role, for the user to view the email composer feature.
-   The response template reader \[sn\_templated\_snip.template\_snippet\_reader\] role should be added for the user to view the response template feature.

**Parent Topic:**[Procurement Case Management](psd-overview.md)

