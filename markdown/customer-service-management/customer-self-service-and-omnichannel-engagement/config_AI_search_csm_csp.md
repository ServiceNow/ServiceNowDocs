---
title: Configure AI Search for the Customer and Consumer Service Portals
description: You must configure the Customer and Consumer Service Portals to use AI Search.
locale: en-US
release: yokohama
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure the Customer and Consumer Service Portals, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# Configure AI Search for the Customer and Consumer Service Portals

You must configure the Customer and Consumer Service Portals to use AI Search.

## Before you begin

You must install a CSM or CSP portal and AI Search integration for CSM and CSP Portals.

Role required: admin, sp\_admin

## About this task

AI Search is inactive by default and you must enable it by updating the portal record.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Portals** and open a portal record.

2.  Configure AI search

    1.  Select **Customer Support** for csm portal or select **Customer Service** for CSP portal.

    2.  Select the **Enable AI Search** check box.

    3.  In the **Search Application** field, search and select **CSM Portal Default Search Application** for customer service portal or **CSP Portal Default Search Application** for consumer service portal.

        A search application configuration defines search experience settings, such as the search engine, search results limit, and suggestions limit. A search application configuration is selected by default, but you can select a different configuration if needed.

        **Note:** You might have to configure the form layout to add **Search Application** field on the form. For more information about adding fields to a form, see [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

    4.  In the **Search Results Configuration** field, search and select **CSM Portal Search** for customer service portal or **CSP Portal Search** for consumer service portal.

        A search result configuration defines how search results are displayed. A search result configuration is selected by default, but you can select a different configuration if needed.

        **Note:** You might have to configure the form layout to add **Search Results Configuration** field on the form. For more information about adding fields to a form, see [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

    5.  Select **Update**.

3.  Enable page route map

    1.  Navigate to **All** &gt; **Service Portal** &gt; **Page Route Maps**.

    2.  Search and Select **CSM AI Search Home Page** for customer service portal or **CSP AI Search Home Page** for consumer service portal.

    3.  Select **Active** check box.

    4.  Select **Update**.


