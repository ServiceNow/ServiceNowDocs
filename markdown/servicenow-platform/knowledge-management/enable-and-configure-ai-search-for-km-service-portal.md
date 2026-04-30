---
title: Enable and configure AI Search for Knowledge Management Service Portal
description: Enable and define the AI Search experience in Knowledge Management Service Portal.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure the Knowledge Management Service Portal, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enable and configure AI Search for Knowledge Management Service Portal

Enable and define the AI Search experience in Knowledge Management Service Portal.

## Before you begin

Role required: sp\_admin or admin

## About this task

All new and existing customers must manually enable AI Search in the Knowledge portal. If you leave AI Search inactive, the portal uses Zing search by default.

## Procedure

1.  Navigate to **Service Portal** &gt; **Portals** and open the **Knowledge Portal** record.

2.  On the form, select the **Enable AI Search** check box.

3.  In the **Search Application** field, select the Knowledge Portal Search Configuration to use for the portal.

    A search application configuration defines search experience settings such as the search engine, search results limit, and suggestions limit.

4.  In the **Search Results Configuration** field, determine how search results are displayed by selecting the Knowledge Portal Search.

5.  Select **Update**.

    **Important:**

    -   The **View count** and **Rating** facets that are available in Zing search aren't available for AI Search.
    -   If you select a Knowledge Base from the Knowledge Portal, you will be directed to the AI Search results page. Because you are not entering a search term, the placeholder “\*\*\*” will be displayed instead of a search term. You can enter a search term on the search results page or select additional filters as needed to refine your results within the selected knowledge base.

## Result

AI Search is enabled throughout the Knowledge portal. Customers can use AI Search from the search bar on the portal.

