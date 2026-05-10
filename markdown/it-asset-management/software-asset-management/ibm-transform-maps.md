---
title: Transform maps for IBM License Metric Tool \(ILMT\) and BigFix Inventory integration v1 APIs
description: When you import data from the IBM License Metric Tool \(ILMT\) or BigFix Inventory using version 1 of the ILMT and BigFix Inventory integration APIs, your ServiceNow instance uses transform maps to process this data into ServiceNow tables.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [ILMT, BigFix Inventory, transform map]
breadcrumb: [Integrating using v1 APIs, ILMT and BigFix Inventory integrations, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Transform maps for IBM License Metric Tool \(ILMT\) and BigFix Inventory integration v1 APIs

When you import data from the IBM License Metric Tool \(ILMT\) or BigFix Inventory using version 1 of the ILMT and BigFix Inventory integration APIs, your ServiceNow instance uses transform maps to process this data into ServiceNow tables.

## Default ILMT and BigFix Inventory transform maps

By default, ServiceNow provides the following transform maps for ILMT and BigFix Inventory data when you are using version 1 of the ILMT and BigFix Inventory APIs:

<table id="table_q4n_vhh_rmb"><thead><tr><th>

Transform Map

</th><th>

Source Table

</th><th>

Target Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ILMT Computer Identity V1

</td><td>

Computer \[imp\_samp\_ilmt\_computer\_system\]

</td><td>

Computer \[cmdb\_ci\_computer\]

</td><td>

Processes identification data for your virtual machines \(VMs\) and hosts.

 The ILMT Computer Identity V1 transform map uses the CMDB IRE API to create a configuration item \(CI\) record for each VM or host in the Computer \[cmdb\_ci\_computer\] table. If a VM uses the same hardware serial number as its host, the transform map creates a CI record for only the host. For more information on the CMDB IRE API, see [Identification and Reconciliation engine \(IRE\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/ire.md).

 **Note:** ServiceNow does not support hardware serial numbers containing periods \(.\).

</td></tr><tr><td>

ILMT Software Instance

</td><td>

ILMT Software Instance \[imp\_samp\_ilmt\_sw\_instance\]

</td><td>

Global \[global\]

</td><td>

Processes installation data for each IBM software component and product on your VMs and hosts.

 Software components are the independent units of software that you install or run on a VM. You can identify but not license software components individually. Software products are the units of software packaging on a host that can comprise of a collection of software components. You can license the software product as a whole. For more information on software components and products, refer to the [IBM Knowledge Center](https://www.ibm.com/support/knowledgecenter/SS8JFY_9.2.0/com.ibm.lmt.doc/Inventory/overview/c_offerings_software_products_components.html).

 The ILMT Software Instance transform map creates a record for each IBM software component and product installation in the IBM Peak Consumption \[samp\_ilmt\_sw\_install\] table.

 **Note:** Although software products are not actual software installations, the transform map treats them as installations so that you can update and track license usage against each software product for reconciliation and compliance purposes.

</td></tr><tr><td>

ILMT Software License Usage

</td><td>

License Consumption \[imp\_samp\_ilmt\_license\_usage\]

</td><td>

Global \[global\]

</td><td>

Processes license usage data for your IBM software products. You can use this data to reconcile your IBM software products and verify compliance.

 **Note:** License usage data is reported against physical hosts only, as IBM software products are licensed based on physical host usage and not virtual machine \(VM\) usage.

 The ILMT Software License Usage transform map updates license usage data on corresponding records in the IBM Peak Consumption \[samp\_ilmt\_sw\_install\] table. If a corresponding record does not exist, the transform map creates a record for your license usage data with the `version` set to `Not reported`.

</td></tr></tbody>
</table>## ILMT and BigFix Inventory data processing

Each ILMT and BigFix Inventory transform map processes data using field maps or transform map scripts.

-   **ILMT Computer Identity V1 transform map**

    The ILMT Computer Identity V1 transform map processes data from the source Computer \[imp\_samp\_ilmt\_computer\_system\] table to the target Computer \[cmdb\_ci\_computer\] table using both field maps and a transform map script.

    By default, the ILMT Computer Identity V1 transform map includes the following field maps:

    |Source Field|Target Field|Description|
    |------------|------------|-----------|
    |u\_ip\_address|ip\_address|IP address of the host or virtual machine.|
    |u\_dns\_name|dns\_domain|Domain name of the host or virtual machine.|
    |u\_server\_processors|cpu\_count|Number of CPUs or virtual CPUs \(vCPUs\) on the host or virtual machine.|
    |u\_host\_name|name|Name of the host or virtual machine.|
    |u\_processor\_brand\_string|cpu\_name|Brand name of the CPU or vCPU on the host or virtual machine \(for example, IBM\).|
    |u\_server\_cores|cpu\_core\_count|Number of CPU or vCPU cores on the host or virtual machine.|
    |\[Script\]|discovery\_source|Discovery source that pulls in IBM software installation data. Possible values are `ILMT` or `BigFix Inventory`.|
    |\[Script\]|virtual|Option indicating whether a machine is virtual.|
    |u\_processor\_brand|cpu\_type|Type of CPU or vCPU on the host or virtual machine \(for example, dual core CPU\).|
    |u\_hardware\_serial\_number|serial\_number|Serial number that identifies the host.|

    In addition to using field maps, the transform map processes data using the onAfter transform map script, which is an event script that processes at the end of each row transformation. For more information on this transform map script, see [Map with transformation event scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/r_MapWithTransformationEventScripts.md).

-   **ILMT Software Instance transform map**

    The ILMT Software Instance transform map processes data from the source ILMT Software Instance \[imp\_samp\_ilmt\_sw\_instance\] table to the target IBM Peak Consumption \[samp\_ilmt\_sw\_install\] table using the onComplete transform map script. The onComplete transform map script is an event script that processes at the end of an import. For more information on this transform map script, see [Map with transformation event scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/r_MapWithTransformationEventScripts.md).

-   **ILMT Software License Usage transform map**

    The ILMT Software License Usage transform map processes data from the source License Consumption \[imp\_samp\_ilmt\_license\_usage\] table to the target IBM Peak Consumption \[samp\_ilmt\_sw\_install\] table using the onStart transform map script. The onStart transform map script is an event script that processes at the beginning of an import. For more information on this transform map script, see [Map with transformation event scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/r_MapWithTransformationEventScripts.md).


**Parent Topic:**[Integrating with the IBM License Metric Tool \(ILMT\) or BigFix Inventory using v1 APIs](integrating-ilmt-bigfix-v1-apis.md)

