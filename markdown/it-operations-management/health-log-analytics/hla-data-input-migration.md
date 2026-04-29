---
title: Migrating a Health Log Analytics data input configuration between instances
description: Export a Health Log Analytics data input and source types configuration as an update set and import it to a different ServiceNow instance. In the target environment, you can use the migrated data input for streaming and processing log data. This functionality saves time and reduces possible errors by avoiding the need to configure the settings again on the target instance.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [ServiceNow, Health Log Analytics, HLA, data input, source types, migration, configuration, update set, import, settings, mapping]
breadcrumb: [Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Migrating a Health Log Analytics data input configuration between instances

Export a Health Log Analytics data input and source types configuration as an update set and import it to a different ServiceNow instance. In the target environment, you can use the migrated data input for streaming and processing log data. This functionality saves time and reduces possible errors by avoiding the need to configure the settings again on the target instance.

The migrated configuration includes mapping and all other relevant settings, except credentials. Depending on the data input that you're exporting, you may need to configure credentials in the target environment. For example, when exporting Amazon CloudWatch or Amazon S3 data inputs, you must configure Amazon Web Services \(AWS\) credentials.

This feature is supported in the Health Log Analytics application, Version 25.0.17 - November 2022 and later, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

Starting with Health Log Analytics Version - December 2025, you can also export all source types related to one or more selected log sources to the update set together. For more information, see

For general information about update sets in the ServiceNow AI Platform, see [System update sets](https://www.servicenow.com/docs/access?context=system-update-sets&version=australia&pubname=australia-application-development&ft:locale=en-US).

-   **[Export a Health Log Analytics data input configuration](../task/hla-data-input-migrate.md)**  
Export the configuration of a Health Log Analytics data input with or without the related source types to an update set. You can then import the update set to the target environment.
-   **[Import a Health Log Analytics data input to a target instance](../task/hla-data-input-import.md)**  
Import a data input configuration that you've exported from another instance as an update set.
-   **[Export source types to an update set in Health Log Analytics](../task/hla-source-types-migrate.md)**  
Export source types to an update set separate from the Health Log Analytics data input configuration. You can then import the update set to the target environment.
-   **[Export source types to an update set by log source in Health Log Analytics](../task/hla-export-sourcetypes-by-source.md)**  
Export all source types related to one or more selected log sources to an update set together. You can then import the update set to the target environment.
-   **[Import Health Log Analytics source types to a target instance](../task/hla-source-types-import.md)**  
Import source types that you've exported separate from the Health Log Analytics data input configuration.

**Parent Topic:**[Set up Health Log Analytics on your ServiceNow instance](hla-implement.md)

