---
title: Health Log Analytics content packs for quicker time to value
description: Shorten onboarding time for the Health Log Analytics application by installing content packs. The packs contain default source types and mapping script templates that save you the time it takes to create them from scratch.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [ServiceNow, Health Log Analytics, HLA, content packs, default source types, mapping script templates]
breadcrumb: [Setting up Health Log Analytics on your ServiceNow instance, Configuring Health Log Analytics, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Health Log Analytics content packs for quicker time to value

Shorten onboarding time for the Health Log Analytics application by installing content packs. The packs contain default source types and mapping script templates that save you the time it takes to create them from scratch.

After installing a content pack, Health Log Analytics begins to stream and parse your log data immediately. The application recognizes and analyzes the data, generates more relevant alerts, and reduces noise from the moment of the integration. You can still customize the mapping configuration later on, if needed.

You can integrate content packs in two different ways:

-   Select a content pack when you're configuring a data input. Health Log Analytics activates the selected pack automatically and uses its mapping script for mapping the data input sources.
-   [Activate a content pack before you configure a data input](../task/hla-content-pack-activate.md). When you have configured the data input and you're mapping the raw log data, select the content pack’s mapping script from the **Data Input Mapping** form.

Currently, a content pack is available for streaming logs from Linux using Filebeat.

**Note:** All configurations in content packs exist in the global domain. If you're using domain separation, the content pack content is only available for logs in the global domain.

This feature is supported in the Health Log Analytics application, Version 25.0.17 - November 2022 and later, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

-   **[Activate a content pack in Health Log Analytics](../task/hla-content-pack-activate.md)**  
You can activate a content pack before configuring a data input.

**Parent Topic:**[Setting up Health Log Analytics on your ServiceNow instance](hla-implement.md)

