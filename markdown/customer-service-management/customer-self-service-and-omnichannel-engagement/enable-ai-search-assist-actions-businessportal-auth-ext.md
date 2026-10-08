---
title: Configure AI Search Assist Actions for authenticated external users in Business and Consumer Portal
description: Configure AI Search Assist Actions to let authenticated external users search knowledge articles in the Business and Consumer portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/customer-self-service-and-omnichannel-engagement/enable-ai-search-assist-actions-businessportal-auth-ext.html
release: brazil
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [AI Search, Assist Actions, authenticated users, Business Portal, external users]
breadcrumb: [AI Search Assist for authenticated external users, Configure Business and Consumer Portal, Configure portals, Set up self-service, Configure, Customer Service Management]
---

# Configure AI Search Assist Actions for authenticated external users in Business and Consumer Portal

Configure AI Search Assist Actions to let authenticated external users search knowledge articles in the Business and Consumer portal.

## Before you begin

You must configure AI Search for the Business and Consumer portal. For more information, see [Enable and configure AI Search in Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/enable-ais-sp.md).

You must enable the Typeahead Search and AI Search Assist for the authenticated external users to use the AI search feature. For more information on the widgets, see [Typeahead Search widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/typeahead-search-widget.md) and [AI Search Assist widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/ais-assist-widget.md).

Role required: web\_service\_admin

## About this task

\[Omitted video\] Description: Configure AI Search Assist Actions for authenticated external users in Business and Consumer Portal

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted Web Services** &gt; **Scripted REST APIs**.

2.  On the Scripted REST APIs page, search and select **AI Search Assist Action \(Internal API\)**.

3.  On the AI Search Assist Actions \(Internal API\) page, in the Resources related list, select the first resource: **Order \[sc\_cat\_item\]**.

4.  On the Order \[sc\_cat\_item\] page, in the **Security** tab, do the following:

    1.  Select the **Requires authentication** checkbox to enable authentication.

    2.  Clear the **Requires SNC Internal** checkbox to disable this restriction.

    3.  Select **Update**.

5.  Return to the AI Search Assist Actions \(Internal API\) page, and in the Resources related list, select the second resource: **Resolves my issue**.

6.  On the Resolves my issue page, repeat the same configuration:

    1.  Select the **Requires authentication** checkbox to enable authentication for this resource.

    2.  Clear the **Requires SNC Internal** checkbox to disable this restriction.

    3.  Select **Update**.

7.  On the AI Search Assist Actions \(Internal API\) page, select **Update** to save all changes.


**Parent Topic:**[AI Search Assist for authenticated external users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/customer-self-service-and-omnichannel-engagement/enable-ai-search-for-business-portal-auth-external.md)

