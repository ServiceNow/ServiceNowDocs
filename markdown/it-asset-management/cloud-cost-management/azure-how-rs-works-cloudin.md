---
title: Rightsizing analysis for Microsoft Azure
description: Cloud Cost Management uses an optimized Rightsizing process for Azure to identify optimization opportunities specific to your environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/cloud-cost-management/azure-how-rs-works-cloudin.html
release: brazil
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Rightsizing resources, Explore, Cloud Cost Management, IT Asset Management, Asset Management]
---

# Rightsizing analysis for Microsoft Azure

Cloud Cost Management uses an optimized Rightsizing process for Azure to identify optimization opportunities specific to your environment.

## How Rightsizing analysis works for Microsoft Azure

Cloud Cost Management generates recommendations that appear in the Rightsizing reports from multiple sources. The recommendations module consolidates insights from both cloud provider APIs and Cloud Cost Management analysis engines.

-   **Cloud Cost Management-generated recommendations**

    These recommendations are based on analysis of billing data, usage metrics, and configuration policies. These are updated after each billing download job runs.

-   **Cloud provider-sourced recommendations:**

    These recommendations are integrated from Azure Advisor service and are refreshed when the integration job completes.


For details on how the values are generated, see the Azure Advisor documentation at [Microsoft Learn](https://docs.microsoft.com).

