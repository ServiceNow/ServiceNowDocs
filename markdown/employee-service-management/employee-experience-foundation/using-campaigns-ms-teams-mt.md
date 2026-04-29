---
title: Sending notifications to employees using Microsoft Teams
description: Integrate Microsoft Teams with the Employee Center to enable content managers to send notifications to employees through Microsoft Teams.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration for Employee Experience, Setup for integrating pre-published apps, Setup the Servicenow instance, Integrating ServiceNow with Microsoft Teams and Microsoft 365, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Sending notifications to employees using Microsoft Teams

Integrate Microsoft Teams with the Employee Center to enable content managers to send notifications to employees through Microsoft Teams.

Send messages on Microsoft Teams to drive employee action, such as to read an article, watch a video, or perform a task.

![Message sent to employees from Microsoft Teams](../../employee-center/images/ec-teams-notification.png)

The Employee Center contains two features, which content managers can use to send communications to employees:

-   **[Creating employee communications](../../employee-center/concept/ec-publish-content.md)**

    Content Publishing provides a workflow to create and publish employee communications.

-   **[Content Experiences](../../employee-center/concept/ecpro-campaigns.md)**

    Content Experiences provides a robust publishing configuration which controls the content availability, duration, and audience.


## Integrating Microsoft Teams with Employee Center

You must have the following plugins installed in your environment:

-   Employee Center Pro \[com.snc.employee\_center\_pro\]
-   IT Service Management for Microsoft 365 \[sn\_now\_teams\_it\]
-   Glide Virtual Agent \[com.glide.cs.chatbot\]
-   HR Service Delivery for Microsoft 365 \[sn\_now\_teams\_hr\]
-   Conversational Integration with Microsoft Teams \[sn\_va\_teams\]
-   Content Publishing \[sn\_cd\]
-   Content Experiences \[sn\_ca\]

## Configuring a Microsoft Teams notification

1.  [Create notification content for Microsoft Teams](../task/create-campaign-content-publish-teams-mt.md)
2.  \(Optional\) [Translate the notification content](campaign-translation-support-mt.md)
3.  Publish the content:
    -   Use **Content Publishing** &gt; **Schedule Content** to make the content available to employees: [Schedule delivery of Microsoft Teams notification content](../task/schedule-delivery-content-mt.md#)
    -   To include the content in a multi-stage, multi-channel campaign, use **Content Experiences** &gt; **Content Experience Builder**: [Create Microsoft Teams notification content with Content Experience Builder](../task/create-notification-content-exp-builder-mt.md#)

-   **[Send automatic campaign notifications in Microsoft Teams](../task/enable-activity-feed-mt.md)**  
Automatically send campaign notifications in Microsoft Teams for better collaboration and efficient communication.
-   **[Create a Microsoft Teams campaign with content publishing](create-campaign-content-publishing-mt.md)**  
Create and distribute the Microsoft Teams campaigns using direct content publishing if you have the admin role.
-   **[Create Microsoft Teams campaigns with the Content Experience Builder](create-campaign-content-exp-builder-mt.md)**  
If you have the admin role, you can create campaigns using the Content Experience Builder to distribute content to employees.

**Parent Topic:**[Setup for integrating pre-published apps with Microsoft Teams for Employee Experience](c_employee_ex_tnt.md)

