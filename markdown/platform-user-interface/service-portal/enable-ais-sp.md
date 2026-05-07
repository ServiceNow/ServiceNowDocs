---
title: Enable and configure AI Search in Service Portal
description: Enable and define the AI Search experience in your portal.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-04-21"
reading_time_minutes: 2
breadcrumb: [AI Search in Service Portal, Configuring search in a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Enable and configure AI Search in Service Portal

Enable and define the AI Search experience in your portal.

## Before you begin

AI Search is only supported in Service Portal, Employee Center \(ESC\), Consumer Service Portal, Business Portal and Customer Service Portal. Custom portals must be built off a baseline of one of these portals to have the AI Search capability. The **glide.service\_portal.enable\_ais\_portal.allow\_list** property contains a list of supported baseline portals.

Role required: sp\_admin or admin

## About this task

AI Search is enabled in Service Portal for all new and zBoot customers by default.

If you're upgrading to Australia as an existing customer, AI Search is inactive in Service Portal by default. You can enable it by updating the portal record.

If you leave AI Search inactive, the portal uses the legacy search experience.

## Procedure

1.  Navigate to **Service Portal** &gt; **Portals** and open a portal record.

2.  On the form, select **Enable AI Search**.

3.  In the **Search Application** field, select the search application configuration to use for the portal.

    A search application configuration defines search experience settings, such as the search engine, search results limit, and suggestions limit. A search application configuration is selected by default, but you can select a different configuration if needed.

    For more information on defining a search application configuration, see [Defining search application configurations](https://www.servicenow.com/docs/access?context=defining-search-app-cfgs-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

4.  In the **Search Results Configuration** field, select the search results configuration to enable for the portal.

    A search results configuration defines how search results are displayed. A search results configuration is selected by default, but you can select a different configuration if needed.

    For more information on defining a search results configuration, see [Create an EVAM definition](https://www.servicenow.com/docs/access?context=define-composite-dataset&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

5.  Select **Update**.


## Result

AI Search is enabled throughout the portal. Employees or customers can use AI Search the next time they log in.

The Search Sources related list is hidden from the portal record. You now define search sources in the AI Search application. For more information, see [Defining search sources](https://www.servicenow.com/docs/access?context=search-sources-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

To use AI Search for knowledge articles, you can keep the default **Knowledge Bases** search source or select a custom one.

**Note:** If you're experiencing issues using AI Search for knowledge articles, check that the associated search profile is linked to a knowledge bases search source. For more information, see [Link a search source to a search profile](https://www.servicenow.com/docs/access?context=link-search-source-profile-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## What to do next

Search widgets that you cloned or customized before a system upgrade may not be compatible with AI Search. You can resolve this issue by running a fix script that reclassifies search widget instances. For more information, see [Reclassify cloned or customized search widgets](reclassify-search-widgets.md).

**Parent Topic:**[AI Search in Service Portal](../concept/ai-search.md)

