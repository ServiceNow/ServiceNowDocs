---
title: Configure AI Search for the Customer and Consumer Service Portals
description: You must configure the Customer and Consumer Service Portals to use AI Search.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customer and Consumer Service Portals, Set up self-service, Configure, Customer Service Management]
---

# Configure AI Search for the Customer and Consumer Service Portals

You must configure the Customer and Consumer Service Portals to use AI Search.

## Before you begin

You must install a CSM or CSP portal and AI Search integration for CSM and CSP Portals.

Role required: sp\_admin

## About this task

AI Search is inactive by default and you must enable it by updating the portal record.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Portals** and open a portal record.

2.  Select **Customer Support** for CSM portal or select **Customer Service** for CSP portal.

3.  Select the **Enable AI Search** check box.

4.  In the **Search Application** field, search and select either **CSM Portal Default Search Application** or **CSP Portal Default Search Application** for CSM and CSP portals respectively.

    A search application configuration defines search experience settings, such as the search engine, search results limit, and suggestions limit. A search application configuration is selected by default, but you can select a different configuration if needed.

    **Note:** You might have to configure the form layout to add **Search Application** field on the form. For more information about adding fields to a form, see [Configuring the form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configure-form-layout.md).

5.  In the **Search Results Configuration** field, search and select either **CSM Portal Search** or **CSP Portal Search**.

    A search result configuration defines how search results are displayed. A search result configuration is selected by default, but you can select a different configuration if needed.

    **Note:** You might have to configure the form layout to add **Search Results Configuration** field on the form. For more information about adding fields to a form, see [Configuring the form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configure-form-layout.md).

6.  Select **Update**.

7.  Navigate to **Page Route Maps** and enable the **CSM AI Search Home Page** route map for CSM and **CSP AI Search Home Page** for CSP as they’re inactive by default.


