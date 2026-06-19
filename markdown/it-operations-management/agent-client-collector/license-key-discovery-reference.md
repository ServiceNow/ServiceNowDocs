---
title: License key discovery and access control tables
description: Reference information for the tables, fields, access control, and scheduled job used by license key discovery in Agent Client Collector for Visibility - Content.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/license-key-discovery-reference.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-05-27"
reading_time_minutes: 2
keywords: [license key discovery, ACC-VC, license keys table, license registry configuration, agent client collector]
breadcrumb: [ACC-VC reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# License key discovery and access control tables

Reference information for the tables, fields, access control, and scheduled job used by license key discovery in Agent Client Collector for Visibility - Content.

## Tables

License key discovery uses the following tables.

|Table|Label|Purpose|
|-----|-----|-------|
|sn\_acc\_vis\_content\_license\_registry\_config|License Registry Configuration|Admin-managed list of registry paths and value names to collect from managed endpoints.|
|sn\_acc\_vis\_content\_license\_keys|License Keys|Stores the license key values collected from endpoint devices.|

## License Keys table fields

The **License Keys** \[sn\_acc\_vis\_content\_license\_keys\] table stores the following fields for each discovered key.

<table id="license-key-discovery-keys-fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Configuration Item**

</td><td>

Device the key was collected from. Table: cmdb\_ci\_computer.

</td></tr><tr><td>

**Product**

</td><td>

SAM product associated with this key. Table: samp\_sw\_product.

</td></tr><tr><td>

**User**

</td><td>

This field is automatically set to the user assigned to the CI. Table: sys\_user.

</td></tr><tr><td>

**License Key Config**

</td><td>

Configuration rule that discovered this key. Table: sn\_acc\_vis\_content\_license\_registry\_config.

</td></tr><tr><td>

**Resolved Registry Path**

</td><td>

Exact registry path the key was read from on the endpoint.

</td></tr><tr><td>

**License Key**

</td><td>

Discovered key value.

</td></tr><tr><td>

**Last Scanned**

</td><td>

Date the key was last detected by the agent.

</td></tr><tr><td>

**Absent**

</td><td>

Selected when the key is no longer found on the device. Records are never deleted, they are marked **Absent** instead.

</td></tr></tbody>
</table>## License Registry Configuration form fields

The following table describes the fields in the License Registry Configuration \[sn\_acc\_vis\_content\_license\_registry\_config\] table.

|Field|Description|
|-----|-----------|
|**Product**|SAM product this license key belongs to. Links to the SAM Professional product catalog.|
|**Registry Path**|Windows registry path where the key is stored. For example, `HKLM\SOFTWARE\Microsoft\Office\16.0\Registration`.|
|**Registry Value Name**|Specific registry value to read. For example, `DigitalProductId`.|
|**Name**|This field is automatically set to a combination of the **Product** and **Registry Value Name** values.|
|**Description**|Notes about this configuration record.|
|**Active**|Indicator of whether this record is included in future collections. Clearing this check box removes the record from future collections.|

**Note:** The combination of **Product**, **Registry Path**, and **Registry Value Name** must be unique across all configuration records.

## Access control

The following table shows which roles can access each license key discovery table.

|Role|License Registry Configuration table|License Keys table|
|----|------------------------------------|------------------|
|ACC application admin \(agent\_client\_collector\_admin\)|Read, write, create|Read only|
|Discovery admin \(discovery\_admin\)|Read, write, create|Read only|
|SAM admin \(sam\_admin\)|Read only|Read only|
|All other roles|No access|No access|

## Scheduled job

The following scheduled job supports license key discovery.

|Job|Schedule|Condition|
|---|--------|---------|
|Refresh License Key Config File|Daily at 8:30 a.m. UTC|Runs only when the **sn\_acc\_vis\_content.enable\_license\_key\_discovery** property is set to `true` and the SAM Professional plugin \(com.snc.samp\) is activated.|

**Parent Topic:**[Agent Client Collector for Visibility - Content reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/agent-client-collector-for-visibility-references.md)

