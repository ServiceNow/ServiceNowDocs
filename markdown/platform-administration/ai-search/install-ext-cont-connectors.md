---
title: Install External Content Connectors
description: Install the External Content Connectors applications from the ServiceNow Store.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Install External Content Connectors

Install the External Content Connectors applications from the ServiceNow® Store.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   To run crawls for external content connectors, your instance must have inbound mTLS support enabled. For details on verifying that this feature is enabled on your instance, see [Verify whether inbound mTLS support is enabled for your instance](verify-adcv2-inbound-mtls-enabled.md).

Role required: admin

## About this task

To make content from your external source systems accessible in AI Search, you need to install the External Content Connectors Application Suite plugin from the ServiceNow Store. When you install this plugin, it automatically installs plugins for the following applications:

-   External Content Connectors
-   External Content Connectors Admin
-   All available External Content Connectors connector applications

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the External Content Connectors Application Suite application \(sn\_ext\_conn\_suite\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can't find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Select **Install**.


## What to do next

With the External Content Connectors applications installed, ServiceNow AI Platform admins can configure connectors to crawl content, metadata, users, and group memberships from supported external content repositories, and AI Search administrators can configure crawl settings and create and schedule crawls for those connectors. For details on external content connector configuration, see [Configuring External Content Connectors](../concept/configuring-ext-cont-connectors.md).

-   **[Verify whether inbound mTLS support is enabled for your instance](verify-adcv2-inbound-mtls-enabled.md)**  
Check whether inbound mTLS support is enabled for your ServiceNow AI Platform® instance. You need this feature enabled in order to run crawls for external content connectors.

**Parent Topic:**[External Content Connectors](../reference/ext-cont-connectors-landing-page.md)

