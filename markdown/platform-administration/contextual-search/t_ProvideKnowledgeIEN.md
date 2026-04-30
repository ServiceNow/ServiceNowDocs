---
title: Provide knowledge in incident email notification
description: Contextual search results are included in email notifications that are sent to users who create a new incident.
locale: en-US
release: yokohama
product: Contextual Search
classification: contextual-search
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Define email configuration for contextual search, Managing contextual search, Contextual search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Provide knowledge in incident email notification

Contextual search results are included in email notifications that are sent to users who create a new incident.

## Before you begin

Role required: admin

## About this task

The email notification provides links to knowledge articles that may help users resolve their issues faster. For example, if a user raises an incident when the service desk staff isn't available, the email notification provides knowledge links that may help the user.

By default, contextual search results are based on the short description in the incident. Within the automated email response, contextual search adds links to relevant knowledge articles.

## Procedure

1.  A customer sends an email to IT support with the subject `My laptop keeps crashing`.

2.  An incident is created based on this email.

3.  The email subject is inserted into the **Short description** field of the new incident.

4.  The automated email notification sent to the user includes search results based on `My laptop keeps crashing`.

    By default, notifications provide three article links.

5.  The customer may then be able to use the search results to resolve the incident.

    **Note:** The knowledge links provided are filtered to ensure that the articles are accessible to the user who submitted the email.


## What to do next

You can configure notification options, such as changing the number of links provided with notifications. You can also configure contextual search functionality to match the email notifications of your organization or you can use contextual search with notifications for other records.

**Parent Topic:**[Define email configuration for contextual search](define-email-configuration-for-cxs.md)

**Related topics**  


[Edit an email notification for the search results](t_ConfigureAnEmailNotification.md)

