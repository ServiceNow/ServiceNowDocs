---
title: Configuring Health Log Analytics
description: As an administrator, set up and configure Health Log Analytics for operators to use, and carry out administration tasks to confirm that the system runs efficiently.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Health Log Analytics, data input, connector, configuration, setup]
breadcrumb: [Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Configuring Health Log Analytics

As an administrator, set up and configure Health Log Analytics for operators to use, and carry out administration tasks to confirm that the system runs efficiently.

## Configuration overview

Complete the following tasks for a successful setup and configuration of Health Log Analytics.

**Important:** Regardless of how you implement Health Log Analytics, for log data ingestion via a MID Server you must first configure [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) and ensure that the MID Server log ingestion capability is enabled.

For MID Server proxy requirements, see [MID Server proxy preconditions for streaming logs to Health Log Analytics](../reference/hla-mid-proxy-configure.md).

Setup and configuration tasks:

1.  [Install Health Log Analytics \(HLA\)](../task/install-health-log-analytics.md).

    Install the Health Log Analytics application.

2.  Set up log data inputs for streaming raw log messages from external sources into your ServiceNow instance.

    You're encouraged to integrate data inputs with Health Log Analytics from the Integrations Launchpad. This tool provides a unified interface for convenient integration setup:

    -   [Set up integrations for Health Log Analytics from the Integrations Launchpad](hla-data-input-setup-integrations.md).

        Alternatively, you can set up data inputs in one of the following ways:

    -   [Set up data inputs in Health Log Analytics using guided setup](../task/hla-data-input-setup-guided.md).
    -   [Set up data inputs in Health Log Analytics manually](../task/hla-data-input-setup-manual.md).
3.  [Identify and resolve a log streaming issue in Health Log Analytics](../task/hla-data-input-streaming.md).

    Identify and address log streaming issues to confirm that the data inputs you have configured are streaming data properly to your instance.

4.  [Edit raw log data before processing in Health Log Analytics](../task/hla-data-input-preprocess.md).

    Modify raw log messages before they are processed in the MID Server, and therefore before Health Log Analytics maps and structures it.

5.  [Map your logs to service instances and components for log context](../task/il-connector-hla-map-business-context.md).

    Map your logs to service instances and components so that Health Log Analytics can generate alerts in context.

    If you turn off automatic mapping, you must define a mapping script manually in the **Data Input Mapping** page. For more information, see [Map raw log data in Health Log Analytics](../task/hla-data-input-mapping.md).

6.  [Refine the source type structure in Health Log Analytics](../task/hla-source-type-structure-refine.md).

    Fine-tune how Health Log Analytics reads your inner log messages and detects anomalies by customizing the extracted properties in the source type structure.

    Health Log Analytics enables you to reclassify auto-classified properties and change auto-mapped labels. These adjustments help the system's machine learning better understand your priorities.

7.  [Perform additional data input setup tasks](hla-data-input-setup-extra.md).

    After performing the mandatory data input setup and configuration, you can continue with optional setup tasks.

8.  [Perform advanced data input configuration tasks](hla-data-input-adv-configuration.md).

For a brief explanation of key terms and concepts used in HLA, see the [Health Log Analytics terminology](../reference/hla-glossary.md).

-   **[Install Health Log Analytics \(HLA\)](../task/install-health-log-analytics.md)**  
Install Health Log Analytics by requesting ServiceNow HLA installation from ServiceNow Customer Support.
-   **[Set up Health Log Analytics on your ServiceNow instance](hla-implement.md)**  
Implement Health Log Analytics on your ServiceNow instance.
-   **[Administering Health Log Analytics](hla-administer.md)**  
This section covers tasks involved in Health Log Analytics administration. It provides you with information needed to keep Health Log Analytics running efficiently.

**Parent Topic:**[ITOM AIOps](../../it-operations-management/reference/itom-health-landing-page.md)

