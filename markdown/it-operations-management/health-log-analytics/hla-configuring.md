---
title: Configuring Health Log Analytics
description: As an Administrator, set up and configure Health Log Analytics for Operators to use, and carry out administration tasks to ensure that the system runs efficiently.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2025-01-26"
reading_time_minutes: 4
keywords: [Health Log Analytics, data input, connector, configuration, setup]
breadcrumb: [Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Configuring Health Log Analytics

As an Administrator, set up and configure Health Log Analytics for Operators to use, and carry out administration tasks to ensure that the system runs efficiently.

## Configuration overview

Complete the following tasks for a successful setup and configuration of Health Log Analytics.

**Important:** Regardless of how you implement Health Log Analytics, you must first configure [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) and ensure that the MID Server log ingestion capability is enabled.

For MID Server proxy requirements, see [MID Server proxy preconditions for streaming logs to HLA](../reference/hla-mid-proxy-configure.md).

1.  [Install Health Log Analytics \(HLA\)](../task/install-health-log-analytics.md).

    Install the Health Log Analytics application.

2.  Set up log data inputs or connectors for streaming raw log messages to your ServiceNow instance.

    Use any of the following methods:

    -   [Set up data inputs using Health Log Analytics guided setup](../task/hla-data-input-setup-guided.md).

        The guided setup provides a sequence of tasks to help you create data inputs on your instance. Using this method ensures that you have the minimum required setup for the data input process.

    -   [Set up data inputs for Health Log Analytics manually](../task/hla-data-input-setup-manual.md).
    -   [Set up integrations from Integrations Launchpad](hla-data-input-setup-integrations.md).

        The ServiceNow Integrations Launchpad provides a unified interface for convenient integration with log data connectors that feed raw log messages into your instance.

    When the data input configuration process is complete, log data starts streaming to your instance.

3.  [Identify and resolve log streaming issues](../task/hla-data-input-streaming.md).

    Identify and address log streaming issues to ensure that the data inputs you have configured are streaming data properly to your instance.

4.  [Edit raw log data before processing](../task/hla-data-input-preprocess.md).

    Modify raw log messages before they are processed in the MID Server, and therefore before Health Log Analytics maps and structures it.

5.  [Map raw log data](../task/hla-data-input-mapping.md).

    Map raw log data that streams into your instance to determine how the data is handled.

    Health Log Analytics tries to [auto-map](hla-data-input-automapping.md) every incoming log line to the correct tag. If properties aren't discovered automatically, you can map the data input sources manually.

6.  [Refine the source type structure](../task/hla-source-type-structure-refine.md).

    Fine-tune how Health Log Analytics reads your inner log messages and detects anomalies by customizing the extracted properties in the source type structure.

    Health Log Analytics enables you to reclassify auto-classified properties and change auto-mapped labels. These adjustments help the system's machine learning better understand your priorities.

7.  [Perform additional data input setup tasks](hla-data-input-setup-extra.md).

    After performing the mandatory data input setup and configuration, you can continue with optional setup tasks.

8.  [Perform advanced data input configuration tasks](hla-data-input-adv-configuration.md).

## Using guided setup to implement Health Log Analytics

Guided setup provides a sequence of tasks that help you configure Health Log Analytics on your ServiceNow instance. To open guided setup for Health Log Analytics, navigate to **All** &gt; **Guided Setup** &gt; **ITOM Guided Setup** &gt; **Health Log Analytics**.

-   **[Install Health Log Analytics \(HLA\)](../task/install-health-log-analytics.md)**  
Install Health Log Analytics by requesting ServiceNow HLA installation from ServiceNow Customer Support.
-   **[Setting up Health Log Analytics on your ServiceNow instance](hla-implement.md)**  
Implement Health Log Analytics on your ServiceNow instance by setting up the data input process.
-   **[Administering Health Log Analytics](hla-administer.md)**  
This section covers tasks involved in Health Log Analytics administration. It provides system administrators with information needed to keep Health Log Analytics running efficiently.

**Parent Topic:**[ITOM AIOps](../../it-operations-management/reference/itom-health-landing-page.md)

