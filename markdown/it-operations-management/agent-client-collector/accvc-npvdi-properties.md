---
title: ACC-VC NPVDI system properties
description: System properties that control how Agent Client Collector for Visibility Content \(ACC-VC\) runs Enhanced Discovery and installed software checks on Windows non-persistent virtual desktop infrastructure \(NPVDI\) endpoints.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/accvc-npvdi-properties.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-10-01"
reading_time_minutes: 1
keywords: [Agent Client Collector for Visibility, ACC-VC, non-persistent VDI, NPVDI, system properties]
breadcrumb: [Agent Client Collector for Visibility Content reference, Agent Client Collector, IT Operations Management]
---

# ACC-VC NPVDI system properties

System properties that control how Agent Client Collector for Visibility Content \(ACC-VC\) runs **Enhanced Discovery** and installed software checks on Windows non-persistent virtual desktop infrastructure \(NPVDI\) endpoints.

**Note:** These properties apply only to Windows endpoints that are configured as non-persistent. On all other endpoints, they have no effect. For details on how ACC-VC behaves on NPVDI endpoints, see [ACC-VC NPVDI endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/accvc-npvdi-support.md).

<table id="table-npvdi-properties"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_acc\_vis\_content.np\_vdi.enhanced\_discovery\_skip\_modules**

</td><td>

-   Type: string
-   Default value: `file_systems,network_adapters,storage_devices,local_users,intel_ema,memory_modules`

Comma-separated list of **Enhanced Discovery** modules to skip on NPVDI endpoints. Only the following values are valid:-   `file_systems`
-   `network_adapters`
-   `storage_devices`
-   `local_users`
-   `intel_ema`
-   `memory_modules`

Any other value is ignored.The following inventory areas run on every check and can't be skipped:

-   **Basic Inventory**
-   **Enhanced Inventory**
-   **TCP Connections**
-   **Running Processes**

</td></tr><tr><td>

**sn\_acc\_vis\_content.np\_vdi.cache\_installed\_software\_enabled**

</td><td>

-   Type: true \| false
-   Default value: false

 Caches the full installed software scan on NPVDI endpoints so that it runs only one time for each golden image. Later check runs reuse the cached results instead of scanning again.

 Software usage metrics, such as last used date and total usage duration, are still collected on every check run.

</td></tr></tbody>
</table>When you update either property, the instance regenerates the NPVDI configuration file \(`NPVDIConfig.json`\) that ACC-VC uses on NPVDI agents. A daily scheduled job also refreshes this file.

