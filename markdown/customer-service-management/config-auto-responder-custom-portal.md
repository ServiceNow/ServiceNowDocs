---
title: Include knowledge articles from custom portals in Auto-Responder notifications
description: Configure the Auto-Responder feature to suggest knowledge articles from a custom portal.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Auto-Responder notifications, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Include knowledge articles from custom portals in Auto-Responder notifications

Configure the Auto-Responder feature to suggest knowledge articles from a custom portal.

## Before you begin

Role required: admin

Activate the Predictive Intelligence for Customer Service Management plugin \(com.snc.csm\_ml\). For more information, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateAPlugin.md) and [Predictive Intelligence for CSM solution definitions](../concept/predictive-intelligence-for-csm.md).

## About this task

By default, the Auto-Responder feature is configured to suggest knowledge articles from customer service portal and consumer service portal. Use this procedure only when you have your own custom portal and don't want to use the default customer service portal or consumer service portal.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Properties**.

2.  In the text box for the **Custom portal URL containing the knowledge article parameter** property \(**sn\_customerservice.case.autoresponder.customportal**\), enter your custom portal URL containing a knowledge article parameter such as sys\_kb\_id or kb\_number.

    Example format: `https://<instance-name>.service-now.com/csm?id=kb_article_view&sys_kb_id=<sys_kb_id>`

3.  Click **Save**.


## What to do next

After you configure the **sn\_customerservice.case.autoresponder.customportal** property, you must configure the Similar Knowledge Articles All similarity solution definition to use the knowledge base of the custom portal. For more information, see [Train the similarity solution for finding Auto-Responder notification content](train-sol-defn-auto-responder.md).

