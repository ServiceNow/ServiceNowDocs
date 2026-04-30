---
title: Google Cloud Platform \(GCP\) Cloud Functions discovery using patterns
description: Discovery and Service Mapping Patterns uses the Google Cloud Platform \(GCP\) - Cloud Functions pattern to discover Cloud Functions in a Google Cloud Platform \(GCP\) deployment during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-06-26"
reading_time_minutes: 3
keywords: [Cloud Functions, GCP Cloud Functions, Google Cloud Platform Cloud Functions, Google Cloud Platform \(GCP\) Cloud Functions, Cloud Functions pattern, GCP Cloud Functions pattern, Google Cloud Platform Cloud Functions pattern, Google Cloud Platform \(GCP\) Cloud Functions pattern]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Google Cloud Platform \(GCP\) Cloud Functions discovery using patterns

Discovery and Service Mapping Patterns uses the Google Cloud Platform \(GCP\) - Cloud Functions pattern to discover Cloud Functions in a Google Cloud Platform \(GCP\) deployment during horizontal discovery. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the GCP discovery prerequisites**

    For more information, see the prerequisites section in [Google Cloud Platform \(GCP\) Cloud components discovery using Patterns](gcp-cloud-discovery-patterns.md).

-   **Enable the relevant pattern**

    The pattern for this service is disabled by default. Starting with Visibility Content version 6.28.0, activating or deactivating a pattern won't be considered a customization, and it will continue to receive updates. Patterns that were previously activated or deactivated will reset to the latest predefined version after upgrading while retaining the last active field value. For more information on enabling patterns, see [Activate a disabled pattern](../task/activate-disabled-pattern.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Google Cloud Platform \(GCP\) - Cloud Functions pattern.

|Field|Description|
|-----|-----------|
|Account Id \[account\_id\]|Name of the project used for the discovery.|
|Object ID \[object\_id\]|Name of the project used for the discovery.|
|Datacenter Type \[datacenter\_type\]|Datacenter type: Google Datacenter \[cmdb\_ci\_google\_datacenter\].|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the availability zone.|
|Description \[short\_description\]|Description of the availability zone.|
|State \[state\]|State of the Availability Zone. Possible values are Available or Terminated.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Datacenter or region name.|
|Region \[region\]|Datacenter or region name.|
|Object ID \[object\_id\]|Unique identifier allocated by GCP for this resource.|
|Description \[short\_description\]|Datacenter or region description.|

<table id="table_fnf_dw2_5fc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Version \[version\]

</td><td>

Version ID of the function, available only for Gen1 Cloud Functions.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Name fetched from the API response.For example: `projects/automation-226410/locations/us-central1/functions/auto-labeller`.

</td></tr><tr><td>

Name \[name\]

</td><td>

Name parsed from the API response.For example: `auto-labeller`.

</td></tr><tr><td>

Function Last Modified \[function\_last\_modified\]

</td><td>

Timestamp indicating the last time the function was updated.

</td></tr><tr><td>

CodeSha256 \[codesha256\]

</td><td>

SHA-256 hash algorithm of the function's code used to verify the integrity of the build.For example: `273a583f-ef1c-49c2-9bae-7d21bf3b5f7a`.

</td></tr><tr><td>

Language \[language\]

</td><td>

Runtime environment or programming language used for the function.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the function. Default value is Installed.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the function. Default value is Operational.

</td></tr></tbody>
</table>On the Dependency Views map, you can view all discovered GCP Cloud Functions resources in your organization and the relationships between them.

![GCP Cloud Functions CIs and connections on a Dependency Views map](../image/gcp-cloud-functions-dependency-view.png "GCP Cloud Functions dependency view")

## CI relationships

Discovery creates these relationships to support the GCP Cloud Functions discovery.

|CI|Relationship|CI|
|---|------------|---|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Contains::Contained by|Availability Zone \[cmdb\_ci\_availability\_zone\]|
|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Cloud Function \[cmdb\_ci\_cloud\_function\]|Hosted on::Hosts|Google Datacenter \[cmdb\_ci\_google\_datacenter\]|
|Key Value \[cmdb\_key\_value\]|References|Cloud Function \[cmdb\_ci\_cloud\_function\]|

## Tag discovery

The Google Cloud Platform \(GCP\) - Cloud Functions pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Cloud Function \[cmdb\_ci\_cloud\_function\] table.|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

