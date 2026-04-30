---
title: Use extension points for Knowledge Management
description: Use UI extension points to add knowledge article headers and footers to knowledge articles and to customize the email template for notifications when a knowledge article is commented on. Use scripted extension points to customize the feedback object used in the email template for notifications when a knowledge article is commented on.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Use extension points for Knowledge Management

Use UI extension points to add knowledge article headers and footers to knowledge articles and to customize the email template for notifications when a knowledge article is commented on. Use scripted extension points to customize the feedback object used in the email template for notifications when a knowledge article is commented on.

## Before you begin

The Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\) must be activated to view the KMFeedbackNotification UI extension point and the KMFeedbackObject scripted extension point. These notifications are part of the Subscriptions feature, which is activated with this plugin.

Starting with the Washington DC release, the Knowledge Management v3 homepage \(com.snc.knowledge3\) is being prepared for deprecation in a future release. It is replaced by the Knowledge Management Service Portal \(com.snc.knowledge\_serviceportal\), which is active by default for customers beginning with the Madrid release. For more information about the new experience, see [Knowledge Management Service Portal homepage features](../concept/knowledge-service-portal-pages.md).

Role required: admin

## About this task

Using extension points makes it easier to integrate customizations without actually altering the base code. You can extend standard base functionality using customized scripts.

To use UI extension points in Knowledge Management, create an implementation and change the data as required. You can create multiple implementations per extension point, but for these scenarios, the use is limited to one implementation only. Example code is provided in the extension point, which can be edited, as required.

An implementation is delivered in the base system for scripted extension points. You can change the data and add additional fields, as required.

## Procedure

1.  To use UI extension points to customize headers and footers in knowledge articles, and the email notification that is sent when a knowledge article is commented on:

    1.  Navigate to **System Extension Points** &gt; **UI Extension Points**.

    2.  Click the UI extension point you want to use.

        **Note:**

        -   Use the KMArticleViewFooter and KMArticleViewHeader UI extension points to add knowledge article headers and footers to the knowledge article view pages \(kb\_view.do\) in Knowledge Management v3.
        -   Use the KMFeedbackNotification UI extension point to customize the email template for notifications when a knowledge article is commented on.
    3.  Click **Create Implementation**.

    4.  Change the data as required.

    5.  Click **Update**.

2.  To use scripted extension points to update the feedback object used in the email template for notifications when a knowledge article is commented on:

    1.  Navigate to **System Extension Points** &gt; **Scripted Extension Points**.

        **Note:** Use the KMFeedbackObject scripted extension point to customize the feedback object used in the email template for notifications when a knowledge article is commented on.

    2.  In the **API Name** column, click global.KMFeedbackObject.

    3.  In the **Implementations** related list, click the KMFeedbackObjectBaseImpl class.

    4.  Change the data and add additional fields, as required.

    5.  Click **Update**.


**Parent Topic:**[Configuring Knowledge Management](../../../configuring-knowledge-management.md)

**Related topics**  


[Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

[Using scripted extension points in server-side scripts](https://www.servicenow.com/docs/access?context=scripted-extension-points&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

[Using UI extension points in server-side UI macros](https://www.servicenow.com/docs/access?context=ui-extension-points&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

[Using client extension points in client-side UI scripting](https://www.servicenow.com/docs/access?context=client-extension-points&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

