---
title: Configure AI Search Assist for authenticated external users in the Business Portal
description: Enable the AI Search Assist to search knowledge articles in the Business Portal.
locale: en-US
release: zurich
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [AI Search Assist for authenticated external users, Configure Business Portal, Set up self-service, Configure, Customer Service Management]
---

# Configure AI Search Assist for authenticated external users in the Business Portal

Enable the AI Search Assist to search knowledge articles in the Business Portal.

## Before you begin

Role required: Authenticated external users with snc\_external role

[Activate Customer Service Management](t_ActivateCustomerService.md)

You must configure AI Search for the Business Portal. For more information, see [Enable and configure AI Search in Service Portal](https://www.servicenow.com/docs/access?context=enable-ais-sp&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

You must enable the Typeahead Search and AI Search Assist for the authenticated external users to use the AI Search feature. For more information on the widgets, see [Typeahead Search widget](https://www.servicenow.com/docs/access?context=typeahead-search-widget&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) and [AI Search Assist widget](https://www.servicenow.com/docs/access?context=ais-assist-widget&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted Web Services** &gt; **Scripted REST APIs**.

2.  On the Scripted REST APIs page, search and select **AI Search Assist \(Internal API\).**

3.  On the AI Search Assist \(Internal API\) page, in the Resources related list, select **search**.

4.  On the search page, in the **Security** tab, do the following:

    -   Select the **Requires authentication** to turn on the authentication to access resource.
    -   Clear the **Requires SNC Internal** check box.
    -   Select **Update**.
5.  Select **Update**.


**Parent Topic:**[AI Search Assist for authenticated external users](../concept/enable-ai-search-for-business-portal-auth-external.md)

