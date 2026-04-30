---
title: Email client configurations
description: Use email client configurations to manage the behavior of your email client. Each configuration consists of different email controls for setting allowable email recipients and email addresses.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, Email client, Notifications, Configure core features, Administer]
---

# Email client configurations

Use email client configurations to manage the behavior of your email client. Each configuration consists of different email controls for setting allowable email recipients and email addresses.

The Email Client Configuration module is activated by default through the Email Client plugin \(com.glide.email\_client\).

## How email client configurations work

Email client configurations determine how your email client behaves, such as whether the From address or Reply-To address should be displayed. A configuration applies to a specific ServiceNow table, which enables you to define email client behavior for a specific context, purpose, or application. For example, if you have email client users who send email about Customer Service case records, you can create a configuration that applies email client controls specific to customer service. You can also select the email client recipient qualifiers for controlling the auto-complete recipient results from a selected table, such as the Customer Contact table.

An email client configuration consists of the following components:

-   **Email client recipient qualifiers**

    Recipient qualifiers control the email recipients returned in the auto-complete results for the To, Cc, and Bcc fields of the email client. You can provide additional qualifiers displayed in the auto-complete results to differentiate recipients that have the same names and narrow the results.

    **Note:** Use the **To is Optional** field in the Email Client Configuration form to make the **To:** field optional to send an email.

-   **Email client From addresses**

    This control enables the display of the From and Reply-To addresses. Use the Email Client Template to create a set of allowable From addresses that can be used when a user sends an email with the email client. You can provide a specific From address to be used in the email client, or you can choose to hide it entirely.

-   **Email client attachment handling**

    By default, attachments that are sent from the email client are attached to the target record. Instead, you can select to attach files to the Email \[sys\_email\] record, or you can set conditions that define which email client attachments are added to the target record. To see the status of all email attachments, go to the Email Attachments \[sys\_email\_attachment\] table.


You can also use an [Email Client Template](../task/t_CreateAnEmailClientTemplate.md#) to define the content of an email client message and set other message characteristics, such as an email sender \(From address\) configuration.

## Email client configuration process

Users with the admin role define and edit email client configurations. Users with the email\_client\_admin role can edit configuration information in selected tables.

-   **1. Build the various email client controls that can be used to create an email client configuration.**
    -   [Define email client recipient qualifiers](../task/define-email-recipient-qualifiers.md)
    -   [Define email client from addresses](../task/define-email-client-from-addresses.md)
-   **2. [Create the email client configuration.](../task/create-email-client-config.md)**

    Define an email client configuration that determines how your email client behaves when users create an email message.


-   **[Define email client recipient qualifiers](../task/define-email-recipient-qualifiers.md)**  
Create a configuration that controls the auto-complete list of recipients displayed in the email client.
-   **[Define email client from addresses](../task/define-email-client-from-addresses.md)**  
Set an allowable email address that is displayed in the From address of a message sent from the email client.
-   **[Create an email client configuration](../task/create-email-client-config.md)**  
Define a configuration that controls the display and behavior of the email client that is based on a selected ServiceNow table.

**Parent Topic:**[Configure email client](configuring-email-client.md)

