---
title: Migrating Health Log Analytics data input configurations between instances
description: Export a Health Log Analytics data input and source types configuration as an update set and import it to a different ServiceNow instance. In the target environment, you can use the migrated data input for streaming and processing log data. This functionality saves time and reduces possible errors by avoiding the need to configure the settings again on the target instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/it-operations-management/health-log-analytics/hla-data-input-migration.html
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
keywords: [ServiceNow, Health Log Analytics, HLA, data input, source types, migration, configuration, update set, import, settings, mapping]
breadcrumb: [Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Migrating Health Log Analytics data input configurations between instances

Export a Health Log Analytics data input and source types configuration as an update set and import it to a different ServiceNow instance. In the target environment, you can use the migrated data input for streaming and processing log data. This functionality saves time and reduces possible errors by avoiding the need to configure the settings again on the target instance.

The migrated configuration includes mapping and all other relevant settings, except credentials. Depending on the data input that you're exporting, you may need to configure credentials in the target environment. For example, when exporting Amazon CloudWatch or Amazon S3 data inputs, you must configure Amazon Web Services \(AWS\) credentials.

This feature is supported in the Health Log Analytics application, Version 25.0.17 - November 2022 and later, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

**Note:** Using HLA configuration migration with ServiceNow AI Platform versions prior to the Tokyo release requires you to import an update set. For more information, see the [HLA Configuration Migration Enablement \[KB1274850\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1274850) article in the Now Support Knowledge Base.

For general information about update sets in the ServiceNow AI Platform, see [System update sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/application-development/system-update-sets/system-update-sets.md).

-   **[Export a data input configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/health-log-analytics/hla-data-input-migrate.md)**  
Export the configuration of a Health Log Analytics data input with or without the related source types to an update set. You can then import the update set to the target environment.
-   **[Import a data input to a target instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/health-log-analytics/hla-data-input-import.md)**  
Import a Health Log Analytics data input configuration that you've exported from another instance as an update set.
-   **[Export source types to an update set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/health-log-analytics/hla-source-types-migrate.md)**  
Export source types to an update set separate from the Health Log Analytics data input configuration. You can then import the update set to the target environment.
-   **[Import source types to a target instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/health-log-analytics/hla-source-types-import.md)**  
Import source types that you've exported separate from the Health Log Analytics data input configuration.

**Parent Topic:**[Configuring Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/health-log-analytics/hla-configuring.md)

