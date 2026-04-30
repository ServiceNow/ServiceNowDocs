---
title: Set up Health Log Analytics on your ServiceNow instance
description: Implement Health Log Analytics on your ServiceNow instance.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [data input connectors]
breadcrumb: [Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Set up Health Log Analytics on your ServiceNow instance

Implement Health Log Analytics on your ServiceNow instance.

**Important:**

-   Install Health Log Analytics on your instance before implementation. For more information, see [Install Health Log Analytics \(HLA\)](../task/install-health-log-analytics.md).
-   Regardless of how you implement Health Log Analytics, you must configure [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) and ensure that the MID Server log ingestion capability is enabled.

    For MID Server proxy requirements, see [MID Server proxy preconditions for streaming logs to Health Log Analytics](../reference/hla-mid-proxy-configure.md).


## Setting up data inputs

You're encouraged to integrate data inputs with Health Log Analytics from the Integrations Launchpad. This tool provides a unified interface for convenient integration with connectors that feed raw log messages from external sources into your instance for processing and analysis. For more information, see [Set up integrations for Health Log Analytics from the Integrations Launchpad](hla-data-input-setup-integrations.md).

Alternatively, you can set up data inputs in one of the following ways:

-   Using guided setup. The guided setup provides a sequence of tasks to help you configure data inputs on your ServiceNow instance. Using the guided setup ensures that you have the minimum required setup for the data input process. For more information, see [Set up data inputs in Health Log Analytics using guided setup](../task/hla-data-input-setup-guided.md).
-   Manually. For more information, see [Set up data inputs in Health Log Analytics manually](../task/hla-data-input-setup-manual.md).

For supported data inputs, see [Supported data inputs for Health Log Analytics](../reference/hla-data-input-supported.md).

