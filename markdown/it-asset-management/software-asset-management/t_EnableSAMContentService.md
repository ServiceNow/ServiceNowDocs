---
title: Enable sharing information with Software Asset Management content service
description: Opt in to share unnormalized software installation data from your organization with Software Asset Management Content Service. You can opt out at any time.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Software Asset Management administration, Software Asset Management, IT Asset Management]
---

# Enable sharing information with Software Asset Management content service

Opt in to share unnormalized software installation data from your organization with Software Asset Management Content Service. You can opt out at any time.

## Before you begin

Role required: sam\_admin

## About this task

**Note:** If you are managing a National Security Cloud \(NSC\) Department of Defense \(DOD\) Impact Level 5 \(IL5\) deployment, you cannot share any unnormalized software installation data with ServiceNow even if you opt to participate in the Software Asset Management Content Service. If a software product does not exist in the Software Asset Management Content Library, you can create a software content request for it manually. For detailed instructions, see [Create IT Asset Management content request](create-itam-content-request.md).

**Important:** If you're using the Software Asset Management application on-premise, you can set up your ServiceNow instance to connect directly to the Content Service. For detailed instructions, see the knowledge base article [KB1585263](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1585263).

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Administration** &gt; **Content Service Setup**.

2.  Select **Opt-In Agreement** to read the agreement.

3.  After reading the agreement, select **Done**.

4.  Select the **Yes, I have read and accept the Opt-In Agreement** check box and then select **Opt-In**.

    After you opt in, the Software Discovery Models, Software Product Lifecycles, Part Numbers and Discovery Maps, Processor Names, and Product License Exception Rules KPIs are automatically enabled. The Custom Software Products KPI is automatically disabled.

5.  To enable or disable a KPI, select the toggle button next to the KPI and then select **Save**.

6.  To opt out, select **I would like to opt my company out of the Software Asset Management Content Service Program** and then select **Opt-Out**.

    The Software Discovery Models, Software Product Lifecycles, Part Numbers and Discovery Maps, Processor Names, Product License Exception Rules, and Custom Software Products are disabled and your unique normalization content is no longer provided to the Software Asset Management content service.


**Parent Topic:**[Software Asset Management administration](../concept/c_SAMAdministration.md)

**Related topics**  


[Software Asset Management Content Service](../concept/c_SAMContentService.md)

