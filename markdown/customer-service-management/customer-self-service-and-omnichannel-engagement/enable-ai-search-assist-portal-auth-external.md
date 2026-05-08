---
title: Configure AI Search Assist in the Customer and Consumer Service Portals for authenticated external users
description: Enable the AI Search Assist to search knowledge articles in the Customer and Consumer Service Portals. It applies for authenticated external users with snc\_external role.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [AI Search Assist for authenticated external users, Customer and Consumer Service Portals, Set up self-service, Configure, Customer Service Management]
---

# Configure AI Search Assist in the Customer and Consumer Service Portals for authenticated external users

Enable the AI Search Assist to search knowledge articles in the Customer and Consumer Service Portals. It applies for authenticated external users with snc\_external role.

## Before you begin

[Activate Customer Service Management](t_ActivateCustomerService.md)

You must configure AI Search for the Customer and Consumer Service Portals. For more information, see Enable and configure AI Search in Service Portal.

You must enable the Typeahead Search and AI Search Assist for the authenticated external users to use the AI Search feature. For more information on the widgets, see Typeahead Search widget and AI Search Assist widget.

Role required: web\_service\_admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted Web Services** &gt; **Scripted REST APIs**.

2.  On the Scripted REST APIs page, search and select **AI Search Assist \(Internal API\).**

3.  On the AI Search Assist \(Internal API\) page, in the Resources related list, select **search**.

4.  On the search page, in the **Security** tab, do the following:

    -   Select the **Requires authentication** to turn on the authentication to access resource.
    -   Clear the **Requires SNC Internal** check box.
    -   Select **Update**.
5.  Select **Update**.


**Parent Topic:**[AI Search Assist for authenticated external users](../concept/enable-ai-search-for-portal-auth-external.md)

