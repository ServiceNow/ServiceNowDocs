---
title: Configure license key discovery
description: Enable license key discovery and define the registry paths and values you want the Agent Client Collector for Visibility - Content Windows agent to collect from managed endpoints.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/configure-license-key-discovery.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-06-01"
reading_time_minutes: 1
keywords: [license key discovery, ACC-VC, Windows registry, software license, agent client collector]
breadcrumb: [License key discovery, ACC Discovery, ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Configure license key discovery

Enable license key discovery and define the registry paths and values you want the Agent Client Collector for Visibility - Content Windows agent to collect from managed endpoints.

## Before you begin

The SAM Professional plugin \(com.snc.samp\) must be active.

The Agent Client Collector for Visibility - Content Windows agent must be deployed on the endpoints.

Role required: agent\_client\_collector\_admin or discovery\_admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Search for the **sn\_acc\_vis\_content.enable\_license\_key\_discovery** property.

3.  Set the **Value** field to `true`.

    The default value is `false`. Setting this property to `true` enables license key collection.

4.  Select **Save**.

5.  Navigate to the **License Registry Configuration** \[sn\_acc\_vis\_content\_license\_registry\_config\] table and create a record for each registry entry you want to collect.

    Enter the appropriate values in the fields for each record. For details about the fields, see the [License Registry Configuration form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/license-key-discovery-reference.md) table.

6.  Select **Submit** to save the configuration record.

7.  To apply configuration changes immediately, navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**, search for the `Refresh License Key Config File` scheduled job, and select **Execute Now**.

    By default, this job runs daily at 8:30 a.m. UTC.


## Result

The **Refresh License Key Config File** scheduled job reads all active configuration records and publishes them to the agent as `LicenseKeyConfig.json`. On the next agent run, the Windows agent queries the defined registry paths on each managed endpoint and sends the collected key values to your instance. Discovered keys are stored in the **License Keys** \[sn\_acc\_vis\_content\_license\_keys\] table, linked to the device CI, the associated SAM product, and the user assigned to the CI. If a key that was previously detected is no longer found, it is marked as **Absent**.

**Parent Topic:**[License key discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/license-key-discovery.md)

