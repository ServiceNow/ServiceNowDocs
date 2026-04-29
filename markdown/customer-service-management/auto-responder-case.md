---
title: Using Auto-Responder for case deflections
description: Deflect cases by automatically sending relevant content through the Auto-Responder feature after a customer contact or consumer creates a case.​
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customer communication, Use, Customer Service Management]
---

# Using Auto-Responder for case deflections

Deflect cases by automatically sending relevant content through the Auto-Responder feature after a customer contact or consumer creates a case.​

Whenever a case is created, the Auto-Responder feature sends an email notification containing a list of relevant knowledge articles. The email notifications are sent to the case submitter and watchlist users associated with the case.

By default, the feature sends the email notification for customer service cases logged using emails by users with the snc\_external role. Your administrator can also configure the feature for customer service cases logged using other communication channels such as web, phone, chat, social, community, alert, and virtual agent.

The knowledge articles in an Auto-Responder email notification are included based on contextual search results of the short description of the case. By default, the articles that a case submitter viewed in the last 30 days aren't included. Your administrator can configure the duration of last viewed content by using a scripted extension point. For more information, see [Include advanced contextual search results in Auto-Responder notifications](../task/use-extension-point-auto-responder.md).

As a case submitter or watchlist user, you can determine whether you receive any Auto-Responder notifications by setting notification preferences. For more information, see [Set Auto-Responder notification preferences](../task/set-auto-responder-notification.md).

## Activation information

Activate the Predictive Intelligence for Customer Service Management plugin \(com.snc.csm\_ml\) and enable the **Enable auto-responder recommendations** property \(**sn\_customerservice.case.autoresponder.enable**\). For more information, see [Configure Auto-Responder notifications](../task/config-auto-responder.md).

