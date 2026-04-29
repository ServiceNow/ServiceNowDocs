---
title: Email connector
description: The Email connector lets an RPA Desktop Design Studio automation work with email. For example, an automation can send, retrieve, and reply to email messages, and can automatically download attachments.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Connectors, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Email connector

The Email connector lets an RPA Desktop Design Studio automation work with email. For example, an automation can send, retrieve, and reply to email messages, and can automatically download attachments.

**Note:** The Email connector works only with IMAP mail servers, including Microsoft Outlook, Yahoo! Mail, and many others. It is not possible to access Gmail at this time.

![Infographic for using the Email connector. For the text description, refer to the text that follows.](../image/email-automation-example.png "Example automation using the Email connector")

In this example automation, the SetConfig method of the Email connector logs in to the mail server using the account holder's credentials. The GetMail method then retrieves all the unread messages from the inbox of the account. By using a For Each loop, the automation iterates through the retrieved messages and saves each message's attachments to a specified location on the local drive.

-   For information about using connectors in RPA Desktop Design Studio, see [Use a connector in RPA Desktop Design Studio](../task/use-connector.md).
-   For information about making connector methods visible in RPA Desktop Design Studio, see [Use connector method](../task/use-connector-method.md).
-   To learn how to use connector methods, see [Use a component in RPA Desktop Design Studio](../task/configure-components.md).

-   **[Email connector methods](../reference/email-connector-methods.md)**  
The methods in the Email connector retrieve, send, and reply to email messages, and can download attachments. Use the SetConfig method first to set up the connection to your mail server.
-   **[Email method properties](../reference/email-method-properties.md)**  
The following properties can be set for each of the Email connector methods. To set the properties, double-click a method and enter the values in the **Properties** pane.

**Parent Topic:**[Connectors](connectors.md)

