---
title: Configure AI Search for the Customer and Consumer Service Portals
description: You must configure the Customer and Consumer Service Portals to use AI Search.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure the Customer and Consumer Service Portals, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# Configure AI Search for the Customer and Consumer Service Portals

You must configure the Customer and Consumer Service Portals to use AI Search.

## Before you begin

You must install CSM or CSP portal.

Role required: admin, sp\_admin

## About this task

AI Search is disabled by default and you must enable it by updating the portal record.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Portals** and open a portal record.

2.  Click **Customer Support** for csm portal or click **Customer Service** for csp portal.

3.  Select the **Enable AI Search** check box.

4.  In the **Search Application** field, search and click either **CSM Portal Default Search Application** or **CSP Portal Default Search Application** for CSM and CSP portals respectively.

    A search application configuration defines search experience settings, such as the search engine, search results limit, and suggestions limit. A search application configuration is selected by default, but you can select a different configuration if needed.

    **Note:** You may need to configure the form layout to add **Search Application** field on the form. For more information about adding fields to a form, see [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

5.  In the **Search Results Configuration** field, search and click either **CSM Portal Search** or **CSP Portal Search**.

    A search result configuration defines how search results are displayed. A search result configuration is selected by default, but you can select a different configuration if needed.

    **Note:** You may need to configure the form layout to add **Search Results Configuration** field on the form. For more information about adding fields to a form, see [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

6.  Click **Update**.

7.  Navigate to **Page Route Maps** and enable the **CSM AI Search Home Page** route map for CSM and **CSP AI Search Home Page** for CSP as they are disabled by default.


