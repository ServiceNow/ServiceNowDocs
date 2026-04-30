---
title: Configure AI Search for Business Portal
description: Configure Business Portal to use AI Search.
locale: en-US
release: zurich
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Business Portal, Set up self-service, Configure, Customer Service Management]
---

# Configure AI Search for Business Portal

Configure Business Portal to use AI Search.

## Before you begin

Role required: admin, sp\_admin

## About this task

AI Search is disabled by default. You can enable it by updating the portal record.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Portals** and open a portal record.

2.  Select **Business Portal**.

3.  Select the **Enable AI Search** check box.

4.  In the **Search Application** field, search and select the required search application.

    A search application configuration defines search experience settings, such as the search engine, search results limit, and suggestions limit. A search application configuration is selected by default, but you can select a different configuration if needed.

    You can modify existing search application configurations such as CSM Portal Default Search Application, or create and configure your own search application configurations with AI Search specified as the search engine. For details, see [Create a search application configuration for AI Search](https://www.servicenow.com/docs/access?context=create-search-app-config-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

    **Note:** You may need to configure the form layout to add **Search Application** field on the form. For more information about adding fields to a form, see [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

5.  In the **Search Results Configuration** field, search and select the required search results configuration.

    A search result configuration defines how search results are displayed. A search result configuration is selected by default, but you can select a different configuration if needed.

    You can modify existing search results configuration record such as CSM Search or create and configure your own search results configuration.

    **Note:** You may need to configure the form layout to add **Search Results Configuration** field on the form. For more information about adding fields to a form, see [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

6.  Select **Update**.


