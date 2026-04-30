---
title: Enable text search recommendations in Auto-Responder notifications
description: Configure the Auto-Responder feature to send recommendations that match a text search of a case short description to resolve a customer service case when Predictive Intelligence results are insufficient or unavailable.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Auto-Responder notifications, Machine learning solutions for Customer Service Management, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Enable text search recommendations in Auto-Responder notifications

Configure the Auto-Responder feature to send recommendations that match a text search of a case short description to resolve a customer service case when Predictive Intelligence results are insufficient or unavailable.

## Before you begin

-   Activate the Predictive Intelligence for Customer Service Management plugin \(com.snc.csm\_ml\). For more information, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) and [Predictive Intelligence for CSM solution definitions](../concept/predictive-intelligence-for-csm.md).
-   Set the application scope to Email Notification Script for Contextual Search Results using the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

Role required: admin

## About this task

By default, the Auto-Responder feature is configured to send contextual search results based on Predictive Intelligence. Knowledge articles that have significant text similarity with the short description of a case are sent as Auto-Responder recommendations.

You can configure the Auto-Responder feature to send knowledge article recommendations that match a text search of the case short description when the recommendations sent through the Predictive Intelligence feature aren't sufficient or the feature is disabled.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  Search for the **sn\_adv\_emailscript.textsearch.enable** property.

3.  In the **Value** field, enter `true`.

4.  Click **Update**.


