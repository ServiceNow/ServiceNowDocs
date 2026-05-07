---
title: Configure AI Search Assist Actions for authenticated external users
description: Enable the AI Search Assist Actions to search knowledge articles in the Customer and Consumer Service Portals. It applies for authenticated external users with the snc\_external role.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [AI Search Assist for authenticated external users, Customer and Consumer Service Portals, Set up self-service, Configure, Customer Service Management]
---

# Configure AI Search Assist Actions for authenticated external users

Enable the AI Search Assist Actions to search knowledge articles in the Customer and Consumer Service Portals. It applies for authenticated external users with the snc\_external role.

## Before you begin

[Activate Customer Service Management](t_ActivateCustomerService.md)

You must configure AI Search for the Customer and Consumer Service Portals. For more information, see [Enable and configure AI Search in Service Portal](https://www.servicenow.com/docs/access?context=enable-ais-sp&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

You must enable the Typeahead Search and AI Search Assist for the authenticated external users to use the AI search feature. For more information on the widgets, see [Typeahead Search widget](https://www.servicenow.com/docs/access?context=typeahead-search-widget&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) and [AI Search Assist widget](https://www.servicenow.com/docs/access?context=ais-assist-widget&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

Role required: web\_service\_admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted Web Services** &gt; **Scripted REST APIs**.

2.  On the Scripted REST APIs page, search and select **AI Search Assist Action \(Internal API\)**.

3.  On the AI Search Assist Actions \(Internal API\) page, in the Resources related list, select **Order \[sc\_cat\_item\]**.

4.  On the Order \[sc\_cat\_item\] page, in the **Security** tab, do the following:

    1.  Select the **Requires authentication** to turn on the authentication.

    2.  Clear the **Requires SNC Internal** checkbox to turn off the feature.

    3.  Select **Update**.

5.  On the AI Search Assist Actions \(Internal API\) page, in the Resources related list, select **Resolves my issue**.

6.  On the Resolves my issue page, do the following:

    1.  Select the **Requires authentication** to turn on the authentication to access resource.

    2.  Clear the **Requires SNC Internal** check box.

    3.  Select **Update**.

7.  Select **Update**.


**Parent Topic:**[AI Search Assist for authenticated external users](../concept/enable-ai-search-for-portal-auth-external.md)

