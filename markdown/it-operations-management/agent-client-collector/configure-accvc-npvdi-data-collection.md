---
title: Configure ACC-VC data collection for NPVDI endpoints
description: Choose which Enhanced Discovery modules Agent Client Collector for Visibility Content \(ACC-VC\) skips on Windows non-persistent virtual desktop infrastructure \(NPVDI\) endpoints. Optionally, choose whether installed software scan results are cached within the same session.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/configure-accvc-npvdi-data-collection.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-10-01"
reading_time_minutes: 1
keywords: [Agent Client Collector for Visibility, ACC-VC, non-persistent VDI, NPVDI, system properties]
breadcrumb: [ACC-VC NPVDI endpoints, ACC deployment - endpoints, Agent Client Collector, IT Operations Management]
---

# Configure ACC-VC data collection for NPVDI endpoints

Choose which **Enhanced Discovery** modules Agent Client Collector for Visibility Content \(ACC-VC\) skips on Windows non-persistent virtual desktop infrastructure \(NPVDI\) endpoints. Optionally, choose whether installed software scan results are cached within the same session.

## Before you begin

-   Verify that your instance is prepared for NPVDI agents and that the agent is installed on the golden image as a non-persistent agent. For details, see [Prepare agent deployment on a non-persistent virtual desktop infrastructure machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/npvdi-agent-instance-prep.md) and [Enable a non-persistent virtual desktop infrastructure agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/enable-npvdi-agent.md).
-   ACC-VC version 2.1.1 or later must be installed.
-   Role required: admin

## About this task

Two system properties control how ACC-VC collects data on NPVDI endpoints. These settings apply only to Windows endpoints that are configured as non-persistent. On all other endpoints, the full **Enhanced Discovery** and installed software scan run every time, regardless of these settings. For details on each property, see [ACC-VC NPVDI system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/accvc-npvdi-properties.md).

## Procedure

1.  Navigate to **All** and enter `sys_properties.list` in the filter.

2.  Open the **sn\_acc\_vis\_content.np\_vdi.enhanced\_discovery\_skip\_modules** property.

3.  Set the **Value** field to a comma-separated list of the **Enhanced Discovery** modules to skip.

    Valid values are:

    -   `file_systems`
    -   `network_adapters`
    -   `storage_devices`
    -   `local_users`
    -   `intel_ema`
    -   `memory_modules`
    By default, all six modules are listed. To collect a module on NPVDI endpoints, remove it from the list. Any other value is ignored.

4.  Select **Update**.

5.  Cache the installed software inventory on NPVDI endpoints.

    1.  Open the **sn\_acc\_vis\_content.np\_vdi.cache\_installed\_software\_enabled** property.

    2.  Set the **Value** field to `true`.

    3.  Select **Update**.

    When caching is enabled, the full installed software scan runs one time for each golden image, and later check runs reuse the cached results. Software usage metrics are still collected on every check run.


## Result

When you update either property, the instance regenerates the NPVDI configuration file \(`NPVDIConfig.json`\) that ACC-VC uses on NPVDI agents. A daily scheduled job also refreshes this file.

