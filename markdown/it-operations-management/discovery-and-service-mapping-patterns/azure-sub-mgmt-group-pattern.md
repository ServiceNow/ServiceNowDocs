---
title: Azure Subscriptions Discovery For Management Group pattern-based discovery
description: Discovery and Service Mapping Patterns finds Azure Subscription entities under Management Groups on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-12-31"
reading_time_minutes: 1
keywords: [Azure Subscriptions Discovery For Management Group, Azure Subscriptions, Azure Management Groups, Azure discovery, Azure patterns]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Azure Subscriptions Discovery For Management Group pattern-based discovery

Discovery and Service Mapping Patterns finds Azure Subscription entities under Management Groups on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the Azure discovery prerequisites section in [Microsoft Azure Cloud components discovery using patterns](azure-cloud-discovery-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Azure Subscriptions Discovery For Management Group pattern.

<table id="table_cloud_service_account"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account Id \[account\_id\]

</td><td>

Subscription name or account ID.-   Subscription account: The Azure subscription name
-   Management account: The management group account ID

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the account.-   Subscription account: The display name of the subscription
-   Management account: The service account name

</td></tr><tr><td>

Discovery credentials \[discovery\_credentials\]

</td><td>

Azure credential from the Credentials \[discovery\_credentials\] table.

</td></tr><tr><td>

Datacenter URL \[datacenter\_url\]

</td><td>

The Azure management endpoint URL for the account.

</td></tr><tr><td>

Datacenter Type \[datacenter\_type\]

</td><td>

The type of datacenter: **Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]**.

</td></tr><tr><td>

Parent account \[parent\_account\]

</td><td>

References the Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] table \(Management account\).

</td></tr><tr><td>

Is management account \[is\_master\_account\]

</td><td>

Indicates whether this is a management group account. -   **true**: Management account
-   **false**: Subscription account

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Subscription name or account ID.-   Subscription account: The Azure subscription name
-   Management account: The management group account ID

</td></tr></tbody>
</table>## CI relationships

The Azure Subscriptions Discovery For Management Group pattern creates these references to support Azure Subscriptions Discovery For Management Group discovery.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] \(Subscription account\)|References|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] \(Management account\)|
|Key Value \[cmdb\_key\_value\]|References|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] \(Subscription account\)|

## Azure Tag discovery

The Azure Subscriptions Discovery For Management Group pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] table \(Subscription account\).|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

