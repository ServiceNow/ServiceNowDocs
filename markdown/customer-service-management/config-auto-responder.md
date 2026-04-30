---
title: Configure Auto-Responder notifications
description: Configure the Auto-Responder feature for sharing relevant content in email notifications for deflecting cases.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Configure Auto-Responder notifications

Configure the Auto-Responder feature for sharing relevant content in email notifications for deflecting cases.

## Before you begin

Role required: admin

Activate the Predictive Intelligence for Customer Service Management plugin \(com.snc.csm\_ml\). For more information, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) and [Predictive Intelligence for CSM solution definitions](../concept/predictive-intelligence-for-csm.md).

## About this task

When you install and activate the Predictive Intelligence for Customer Service Management plugin \(com.snc.csm\_ml\), the following related plugins are also activated:

-   Customer Service plugin \(com.sn\_customerservice\)
-   Predictive Intelligence for Contextual Search plugin \(com.snc.contextual\_search\_ml\)
-   Email Notification Script for Contextual Search Results plugin \(com.snc.adv\_cxs\_results\_email\_script\)

You can also configure the Auto-Responder feature for tasks other than customer service cases. For more information, see [Configure Auto-Responder for tasks other than cases](config-auto-responder-other-tasks.md).

## Procedure

1.  Follow the steps in this link: [Enable Auto-Responder](enable-auto-responder.md).

2.  Follow the steps in this link: [Train the similarity solution for finding Auto-Responder notification content](train-sol-defn-auto-responder.md).

3.  Follow the steps in this link: [Configure the search context for Auto-Responder](../concept/config-context-auto-responder.md).

4.  Follow the steps in this link: [Limit the number of articles in Auto-Responder notifications for cases](config-limit-auto-responder.md).

5.  Follow the steps in this link: [Include advanced contextual search results in Auto-Responder notifications](use-extension-point-auto-responder.md).

    **Note:** By default, any knowledge articles viewed in the last 30 days by the user are not included in the email notification. You can use the getViewedContent extension point to modify the filter out by the duration of the last viewed content.

6.  Follow the steps in this link: [Enable text search recommendations in Auto-Responder notifications](enable-text-based-auto-responder.md).

7.  Follow the steps in this link: [Include cases logged using specified communication channels in Auto-Responder notifications](config-auto-responder-channels.md).

8.  Follow the steps in this link: [Include knowledge articles from custom portals in Auto-Responder notifications](config-auto-responder-custom-portal.md).

    **Note:** When you configure the Auto-Responder feature to use a custom portal, the default configuration for the customer service portal and consumer service portal are not used. Ensure that you use this configuration when you have your own custom portal and don't want to use the customer service portal or consumer service portal.


**Related topics**  


[Using Auto-Responder for case deflections](../concept/auto-responder-case.md)

