---
title: Cloud Configuration Governance Scan configuration form
description: The Cloud Configuration Governance Scan configuration form displays detailed information about the scan configuration.
locale: en-US
release: yokohama
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Cloud Configuration Governance reference, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud Configuration Governance Scan configuration form

The Cloud Configuration Governance Scan configuration form displays detailed information about the scan configuration.

|Field|Description|
|-----|-----------|
|Name|Name that uniquely identifies the scan configuration.|
|Description|Brief description of the scan configuration.|

## Configuration tab

Define the configuration settings, such as cloud provider, policy sets, target service accounts, and datacenters for the scan.

<table id="table_ogb_3lv_gsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cloud provider type

</td><td>

Cloud that hosts the resources to be scanned.

</td></tr><tr><td>

Policy sets

</td><td>

Policy sets for the scan.Select one or more policy sets for the scan, and then save the form.

</td></tr><tr><td>

Datacenter filters

</td><td>

Service account or service-account datacenter combination for the scan.1.  In the empty row of the Datacenter Filters list, double-click the service account cell, and then select a service account.

You can select an Amazon Web Services \(AWS\) management account, and then add all of its member accounts to the scan configuration, subject to the fulfillment of the following conditions:

    -   An assume role configuration exists for the management account.
    -   Cloud Discovery has completed the datacenter discovery for the member accounts.
For more information on creating assume role configurations, see [Configure access using temporary credentials based on trusted AWS accounts with AWS credentials](../../it-operations-management/task/configure-iam-role-aws-account.md).

2.  Save the form.
3.  In the empty row of the Datacenter Filters list, double-click the datacenter cell, and then select a datacenter.

If you do not select a datacenter, Cloud Configuration Governance scans all the datacenters that are associated with the service account.


</td></tr></tbody>
</table>## Filters tab

\(Optional\) Specify criteria to filter the cloud resources, and then import their configuration data from the cloud. If specified, Cloud Configuration Governance only fetches the configuration of the resources that match the filter criteria. Otherwise, it fetches the configuration of all the cloud resources.

<table id="table_lbp_2mv_gsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tag filters

</td><td>

Cloud resource tags to filter the cloud resources.

 -   Enter the tag name in the **Name** field.
-   Enter the tag value in the **Value** field.

</td></tr><tr><td>

Freeform

</td><td>

Option to specify a comma-separated list of cloud identifiers to filter the cloud resources.

</td></tr><tr><td>

Resources

</td><td>

Comma-separated list of the cloud identifiers.This field appears only when the **Freeform** option is selected.

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Configuration Governance reference](ccg-reference.md)

