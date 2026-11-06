---
title: OCI sub account pattern-based discovery
description: Discovery and Service Mapping Patterns finds sub accounts \(compartments\) in your OCI environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-sub-account-pattern.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-10-29"
reading_time_minutes: 3
keywords: [Oracle OCI - Sub Account \(LP\), sub account, compartment, OCI discovery, Oracle patterns]
breadcrumb: [OCI discovery, Available cloud discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# OCI sub account pattern-based discovery

Discovery and Service Mapping Patterns finds sub accounts \(compartments\) in your OCI environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

-   **Verify the REST API permissions**

    Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

-   **Verify the OCI discovery prerequisites**

    For more information, see the prerequisites section in [Oracle Cloud Infrastructure \(OCI\) discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-cloud-infrastructure-discovery.md).

-   **Configure the Discovery schedule to support GovCloud**

    Discovering OCI GovCloud accounts requires using a datacenter URL when setting up an OCI service account. For more information, see [Create OCI service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/create-oci-service-accounts.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Oracle OCI - Sub Account \(LP\) pattern.

<table id="table_subaccount_service_account"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the compartment.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Oracle Cloud Identifier \(OCID\) of the compartment.

</td></tr><tr><td>

Account Id \[account\_id\]

</td><td>

Unique identifier of the account. -   For sub accounts: the value is the OCID of the compartment
-   For the management account: the value is the account ID of the tenancy that you entered when you added the account

</td></tr><tr><td>

Datacenter Type \[datacenter\_type\]

</td><td>

Type of datacenter that the account belongs to. The value is set to OCI Datacenter \[cmdb\_ci\_oci\_datacenter\].

</td></tr><tr><td>

Datacenter URL \[datacenter\_url\]

</td><td>

URL of the datacenter. The value is inherited from the management account.

</td></tr><tr><td>

Organization Id \[organization\_id\]

</td><td>

Organization ID. The value is inherited from the management account.

</td></tr><tr><td>

Is management account \[is\_master\_account\]

</td><td>

Indicator of whether the account is the management account.-   For sub accounts: the value is false
-   For the management account: the value is true

</td></tr><tr><td>

Parent account \[parent\_account\]

</td><td>

Reference to the Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] table.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the resource. Default value is Operational.

</td></tr></tbody>
</table>## CI relationships and references

The Oracle OCI - Sub Account \(LP\) pattern creates the following relationships and references to support OCI sub account discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|Members::Member of|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|Parent account \[parent\_account\]|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

## OCI tag discovery

The pattern extension section collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|Reference to the Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] table.|

**Parent Topic:**[Oracle Cloud Infrastructure \(OCI\) discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/oracle-cloud-infrastructure-discovery.md)

