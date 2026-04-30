---
title: Repair AI Search for Next Experience after activating a new ServiceNow AI Platform language
description: Install translated search UI element labels for a newly activated ServiceNow AI Platform language by repairing the AI Search for Next Experience application.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring AI Search for Next Experience, AI Search for Next Experience, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Repair AI Search for Next Experience after activating a new ServiceNow AI Platform language

Install translated search UI element labels for a newly activated ServiceNow AI Platform language by repairing the AI Search for Next Experience application.

## Before you begin

You must have activated a new ServiceNow AI Platform language plugin after AI Search for Next Experience was installed in your instance. For details on activating language plugins, see [Activate a language](../../localization/task/t_ActivateALanguage.md).

Role required: admin

## About this task

At installation time, the AI Search for Next Experience application includes search UI element translations for all languages currently active in your ServiceNow AI Platform instance. These translations include language-specific labels for the Unified Navigation search field, source facet buckets, and other elements of the global search and configurable workspace search user interfaces.

If you activate a new ServiceNow AI Platform language plugin in an instance that already has AI Search for Next Experience installed, the application doesn't automatically update to include UI element translations for the newly added language. To install these translations, you can repair the AI Search for Next Experience application.

For more details on repairing applications, see [Repair a ServiceNow application](../../application-manager/task/repair-app.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Locate the AI Search for Next Experience and select its menu icon ![](../../../build/applications/image/menu-icon.png).

3.  In the Activate Plugin dialog box, select **Repair**.


## Result

The AI Search for Next Experience application and its dependencies are reinstalled. After reinstallation, the application includes search UI element translations for all languages activated in your ServiceNow AI Platform instance.

**Parent Topic:**[Configuring AI Search for Next Experience](../concept/configuring-ais-next-experience.md)

