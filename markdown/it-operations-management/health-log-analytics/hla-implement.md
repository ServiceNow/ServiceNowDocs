---
title: Setting up Health Log Analytics on your ServiceNow instance
description: Implement Health Log Analytics on your ServiceNow instance by setting up the data input process.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
keywords: [data input connectors]
breadcrumb: [Configuring Health Log Analytics, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Setting up Health Log Analytics on your ServiceNow instance

Implement Health Log Analytics on your ServiceNow instance by setting up the data input process.

**Note:** For information about installing the ServiceNow Health Log Analytics application, see [Install Health Log Analytics \(HLA\)](../task/install-health-log-analytics.md).

**Important:** Regardless of how you implement Health Log Analytics, you must first configure [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) and ensure that the MID Server log ingestion capability is enabled.

For MID Server proxy requirements, see [MID Server proxy preconditions for streaming logs to HLA](../reference/hla-mid-proxy-configure.md).

## Setting up the data input process

You can set up data inputs or integrations for Health Log Analytics in the following ways:

-   Using guided setup. The guided setup provides a sequence of tasks to help you configure data inputs on your ServiceNow instance. Using the guided setup ensures that you have the minimum required setup for the data input process. For more information, see [Set up data inputs using Health Log Analytics guided setup](../task/hla-data-input-setup-guided.md).
-   Manually. For more information, see [Set up data inputs for Health Log Analytics manually](../task/hla-data-input-setup-manual.md).
-   From the Event Management Integrations Launchpad in Service Operations Workspace for ITOM. The Integrations Launchpad enables you to quickly and conveniently set up integrations and start receiving log data. For more information, see [Set up integrations from Integrations Launchpad](hla-data-input-setup-integrations.md).

    **Note:** Currently, integrations are available for Elasticsearch, ServiceNow System Logs Retriever, UDP, TCP, REST API, MID Server, Apache Kafka, Splunk UDP, Splunk TCP, Splunk Poller, Microsoft Azure Log Analytics, and Amazon Data Firehose.


-   **[Set up data inputs using Health Log Analytics guided setup](../task/hla-data-input-setup-guided.md)**  
The Health Log Analytics guided setup provides a sequence of tasks to help you create data inputs on your ServiceNow instance. Data input configuration is an essential step in setting up the Health Log Analytics application. Using guided setup ensures that you have the minimum required setup for the data input process.
-   **[Set up data inputs for Health Log Analytics manually](../task/hla-data-input-setup-manual.md)**  
Set up your Health Log Analytics data inputs for Health Log Analytics manually. Data input configuration is an essential step in setting up the Health Log Analytics application.
-   **[Identify and resolve log streaming issues](../task/hla-data-input-streaming.md)**  
Identify and address log streaming issues to ensure that the data inputs you have configured for Health Log Analytics are streaming data properly to your ServiceNow instance.
-   **[Edit raw log data before processing](../task/hla-data-input-preprocess.md)**  
You can modify raw log data and drop or break up log messages before they are processed in the MID Server, and therefore before Health Log Analytics maps and structures it. For example, you could prevent sensitive data from reaching the system by replacing user names and passwords with an asterisk \(\*\).
-   **[Log data auto-mapping and mapping](hla-data-input-automapping.md)**  
By default, the Health Log Analytics AI engine tries to auto-map every incoming log line to the correct tags. You can change automatic mapping results manually by defining a JavaScript function.
-   **[Source type structure adjustment](hla-source-type-structure-adjustment.md)**  
Health Log Analytics enables you to reclassify auto-classified properties and change auto-mapped labels. These adjustments help Health Log Analytics machine learning to better understand your priorities.
-   **[Additional data input setup tasks](hla-data-input-setup-extra.md)**  
After performing the initial data input setup and configuration, continue with the remaining data input setup tasks.
-   **[Advanced data input configuration](hla-data-input-adv-configuration.md)**  
When you have configured a data input successfully, Health Log Analytics adds a record to the Data Inputs table and attaches the configuration file to it. You can configure advanced settings for your data input. Configuring advanced settings is optional.
-   **[Health Log Analytics content packs for quicker time to value](hla-content-packs.md)**  
Shorten onboarding time for the Health Log Analytics application by installing content packs. The packs contain default source types and mapping script templates that save you the time it takes to create them from scratch.
-   **[Stop or restart a data input in Health Log Analytics](../task/hla-data-input-stop-start.md)**  
You can stop using a data input for streaming log messages to your ServiceNow instance. Restart the data input if you want it to resume streaming data.
-   **[Migrating Health Log Analytics data input configurations between instances](hla-data-input-migration.md)**  
Export a Health Log Analytics data input and source types configuration as an update set and import it to a different ServiceNow instance. In the target environment, you can use the migrated data input for streaming and processing log data. This functionality saves time and reduces possible errors by avoiding the need to configure the settings again on the target instance.
-   **[Check gRPC and network connectivity on the MID Server](../task/hla-grpc-connectivity-check.md)**  
Verify that Health Log Analytics can function properly by performing diagnostic tests on the MID Server to check gRPC and network connectivity.

**Parent Topic:**[Configuring Health Log Analytics](hla-configuring.md)

**Related topics**  


[Supported data inputs for Health Log Analytics](../reference/hla-data-input-supported.md)

