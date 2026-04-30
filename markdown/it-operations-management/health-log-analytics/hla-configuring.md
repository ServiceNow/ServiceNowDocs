---
title: Configuring Health Log Analytics
description: As an Administrator, set up and configure Health Log Analytics for Operators to use, and carry out administration tasks to ensure that the system runs efficiently.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Health Log Analytics, data input, connector, configuration, setup]
breadcrumb: [Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Configuring Health Log Analytics

As an Administrator, set up and configure Health Log Analytics for Operators to use, and carry out administration tasks to ensure that the system runs efficiently.

## Configuration overview

Complete the following tasks for a successful setup and configuration of Health Log Analytics.

**Important:** Regardless of how you implement Health Log Analytics, for log data ingestion via a MID Server you must first configure [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) and ensure that the MID Server log ingestion capability is enabled.

For MID Server proxy requirements, see [MID Server proxy preconditions for streaming logs to Health Log Analytics](../reference/hla-mid-proxy-configure.md).

1.  [Install Health Log Analytics \(HLA\)](../task/install-health-log-analytics.md).

    Install the Health Log Analytics application.

2.  Set up log data inputs for streaming raw log messages to your ServiceNow instance.

    Use any of the following methods:

    -   [Set up integrations for Health Log Analytics from the Integrations Launchpad](hla-data-input-setup-integrations.md).

        You're encouraged to set up data input integrations from the Integrations Launchpad, which provides a unified interface for convenient integration.

    -   [Set up data inputs in Health Log Analytics using guided setup](../task/hla-data-input-setup-guided.md).
    -   [Set up data inputs in Health Log Analytics manually](../task/hla-data-input-setup-manual.md).
3.  [Identify and resolve a log streaming issue in Health Log Analytics](../task/hla-data-input-streaming.md).

    Identify and address log streaming issues to ensure that the data inputs you have configured are streaming data properly to your instance.

4.  [Edit raw log data before processing in Health Log Analytics](../task/hla-data-input-preprocess.md).

    Modify raw log messages before they are processed in the MID Server, and therefore before Health Log Analytics maps and structures it.

5.  [Map raw log data so HLA can correctly process it](../task/hla-data-input-mapping.md).

    Configure mapping for your raw log data so that Health Log Analytics can correctly parse and analyze it.

    **Note:** The user-friendly Log context mapping interface in the new HLA UI is simpler to use than Data input mapping in HLA's classic interface \(UI16\). For more information about Log context mapping, see [Map logs to service instances, components, and source types for contextual alerts in Health Log Analytics](../task/il-connector-hla-map-business-context.md).

6.  [Refine the source type structure](../task/hla-source-type-structure-refine.md).

    Fine-tune how Health Log Analytics reads your inner log messages and detects anomalies by customizing the extracted properties in the source type structure.

    Health Log Analytics enables you to reclassify auto-classified properties and change auto-mapped labels. These adjustments help the system's machine learning better understand your priorities.

7.  [Perform additional data input setup tasks](hla-data-input-setup-extra.md).

    After performing the mandatory data input setup and configuration, you can continue with optional setup tasks.

8.  [Perform advanced data input configuration tasks](hla-data-input-adv-configuration.md).

