---
title: Set up Health Log Analytics on your ServiceNow instance
description: Implement Health Log Analytics on your ServiceNow instance.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [data input connectors]
breadcrumb: [Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Set up Health Log Analytics on your ServiceNow instance

Implement Health Log Analytics on your ServiceNow instance.

**Important:**

-   Install Health Log Analytics on your instance before implementation. For more information, see [Install Health Log Analytics \(HLA\)](../task/install-health-log-analytics.md).
-   Regardless of how you implement Health Log Analytics, you must configure [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) and ensure that the MID Server log ingestion capability is enabled.

    For MID Server proxy requirements, see [MID Server proxy preconditions for streaming logs to Health Log Analytics](../reference/hla-mid-proxy-configure.md).


## Setting up data inputs

You're encouraged to integrate data inputs with Health Log Analytics from the Integrations Launchpad. This tool provides a unified interface for convenient integration with connectors that feed raw log messages from external sources into your instance for processing and analysis. For more information, see [Set up integrations for Health Log Analytics from the Integrations Launchpad](hla-data-input-setup-integrations.md).

Alternatively, you can set up data inputs in one of the following ways:

-   Using guided setup. The guided setup provides a sequence of tasks to help you configure data inputs on your ServiceNow instance. Using the guided setup ensures that you have the minimum required setup for the data input process. For more information, see [Set up data inputs in Health Log Analytics using guided setup](../task/hla-data-input-setup-guided.md).
-   Manually. For more information, see [Set up data inputs in Health Log Analytics manually](../task/hla-data-input-setup-manual.md).

For supported data inputs, see [Supported data inputs for Health Log Analytics](../reference/hla-data-input-supported.md).

-   **[Set up data inputs in Health Log Analytics using guided setup](../task/hla-data-input-setup-guided.md)**  
The Health Log Analytics guided setup provides a sequence of tasks to help you create data inputs on your ServiceNow instance. Data input configuration is an essential step in setting up the Health Log Analytics application. Using guided setup ensures that you have the minimum required setup for the data input process.
-   **[Set up data inputs in Health Log Analytics manually](../task/hla-data-input-setup-manual.md)**  
Set up your Health Log Analytics data inputs for Health Log Analytics manually. Data input configuration is an essential step in setting up the Health Log Analytics application.
-   **[Edit raw log data before processing in Health Log Analytics](../task/hla-data-input-preprocess.md)**  
Use the Data Input Preprocessor to filter, split, or sanitize raw log data before it is treated in the MID Server and mapped and structured by Health Log Analytics.
-   **[Log data auto-mapping and mapping in Health Log Analytics](hla-data-input-automapping.md)**  
By default, the HLA Engine tries to auto-map every incoming log line to the correct tags. You can change automatic mapping results manually by defining a JavaScript function.
-   **[Source type structure adjustment in Health Log Analytics](hla-source-type-structure-adjustment.md)**  
Health Log Analytics \(HLA\) enables you to reclassify auto-classified log properties and change auto-mapped labels. These adjustments help HLA machine learning analyze your data accurately.
-   **[Health Log Analytics content packs for quicker time to value](hla-content-packs.md)**  
Shorten onboarding time for the Health Log Analytics application by installing content packs. The packs contain default source types and mapping script templates that save you the time it takes to create them from scratch.
-   **[Migrating a Health Log Analytics data input configuration between instances](hla-data-input-migration.md)**  
Export a Health Log Analytics data input and source types configuration as an update set and import it to a different ServiceNow instance. In the target environment, you can use the migrated data input for streaming and processing log data. This functionality saves time and reduces possible errors by avoiding the need to configure the settings again on the target instance.
-   **[Check gRPC and network connectivity for Health Log Analytics on the MID Server](../task/hla-grpc-connectivity-check.md)**  
Verify that Health Log Analytics can function properly by performing diagnostic tests on the MID Server to check gRPC and network connectivity.

**Parent Topic:**[Configuring Health Log Analytics](hla-configuring.md)

