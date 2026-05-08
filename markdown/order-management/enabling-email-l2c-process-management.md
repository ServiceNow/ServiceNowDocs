---
title: Setting conditions for enabling email access in Lead-to-Cash Process Management
description: Sales process managers must be granted access to compose emails for the sales entity records that are monitored in a sales process record.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Lead-to-Cash Process Management, Order operations apps, Configure, Sales Customer Relationship Management]
---

# Setting conditions for enabling email access in Lead-to-Cash Process Management

Sales process managers must be granted access to compose emails for the sales entity records that are monitored in a sales process record.

Sales process managers can compose and send emails related to a sales process record by default. Enable sales process managers to compose emails for the related sales entities by setting the value of the **email\_client** dictionary attribute to **true** and using either of the following methods:

-   Grant the sales process manager write access to the child entity. For more information, see Enable the email client for a table.
-   Set the value of the **glide.email\_client.check\_write\_access** system property to **false** to override checking whether the user has write access to the child entity.

    **Note:** The **glide.email\_client.check\_write\_access** system property isn’t supported on Xanadu and Yokohama Glide versions. If you’re using these Glide versions, then you must grant your users write access to the child entity.


**Related topics**  


[bundle-platadm.c_EnableTheEmailClient]

[View and send emails in Lead-to-Cash Process Management](../task/view-send-emails-sales-process.md)

