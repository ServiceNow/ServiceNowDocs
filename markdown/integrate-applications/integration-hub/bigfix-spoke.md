---
title: BigFix Inventory Spoke
description: Manage hardware, software, and licenses in BigFix Inventory from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# BigFix Inventory Spoke

Manage hardware, software, and licenses in BigFix Inventory from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

BigFix Inventory spoke v1.5.4 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Action Template - Data Streaming \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Action Step - Get Connection Info \(com.glide.hub.action\_step.get\_connection\_info​\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported versions

This spoke was built for BigFix Inventory version 9.2.16.0, but may be compatible with later versions.

## Spoke requirements

BigFix Inventory Management account.

## Spoke flow

The BigFix Inventory spoke provides a sample flow, Configure End of Support Date for Software Component to demonstrate setting the end of support date for software component when the Set Software Support End Date service catalog request is created. You can customize the sample flow as per your requirement by creating a copy of it in the required scope.

## Spoke subflow

The BigFix Inventory spoke provides a sample subflow, Send an Email Notification for BigFix Inventory Report to demonstrate sending an email notification with the received BigFix Inventory report attachment. To customize the sample subflow, copy it to the required application scope.

## Spoke remote table

ServiceNow provides a sample remote table that you can use to connect to BigFix Inventory, and view, pull, and manipulate data from the BigFix Inventory. The name of the sample remote table is Computers. You can create custom remote tables based on the sample remote table. To access the remote table, on your instance, navigate to **All** &gt; **BigFix Inventory Spoke** &gt; **Software Inventories** &gt; **Remote Table**, and then select **Computers**.

For more information on remote tables, see [Remote tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/remote-tables/remote-tables.md).

## Spoke actions

The BigFix Inventory spoke provides actions to automate BigFix Inventory tasks when events occur in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Hardware Management|Look up BIOS Details by Computer ID|Retrieves the BIOS details of a computer.|
|Look up BIOS Details Stream|Retrieves the list of BIOS Details of the scanned systems|
|Look up Computer Hardware Fields by Computer ID|Retrieves list of logical partitions associated with a computer.|
|Look up Hardware Inventories Stream|Lists summary information about hardware records in the BigFix Inventory system.|
|Look up IP Addresses by Computer ID|Retrieves the list of IP addresses associated with a computer.|
|Look up IP Addresses Stream|Retrieves the list of IP address details of the computers in the Infrastructure.|
|Look up Logical Partitions by Computer ID|Retrieves the list of logical partitions associated with a computer.|
|Look up Logical Partitions Stream|Retrieves the list of logical partition details of the computers in the infrastructure.|
|Look up Memory Details by Computer ID|Retrieves the memory details of a computer.|
|Look up Memory Details Stream|Retrieves the list of system memory details of the scanned systems.|
|Look up Network Adapters by Computer ID|Retrieves the list of network adapters associated with a computer.|
|Look up Network Adapters Stream|Retrieves the list of network adapters.|
|Look up Operating System Details by Computer ID|Retrieves the operating system details of a computer.|
|Look up Operating System Details Stream|Retrieves details of the operating system of the scanned computers.|
|Look up Physical Partition Details by Computer ID|Retrieves list of physical partitions associated with a computer.|
|Look up Physical Partitions Stream|Retrieves the list of physical partitions of the scanned computers.|
|Look up Processor Details by Computer ID|Retrieves the operating system details of a computer.|
|Look up Processor Details Stream|Retrieves the details of all active physical processors.|
|Look up Shared Disks Stream|Lists shared disks in BigFix Inventory.|
|Look up Storage Devices by Computer ID|Retrieves list of the physical partitions associated with a computer.|
|Look up Storage Devices Stream|Retrieves the list of storage devices of the scanned systems.|
|License Management|Look up License Metric Utilizations Stream|Retrieves utilization data for licenses in BigFix Inventory.|
|Software Management|Look up Cluster Information Stream|Lists clusters in the BigFix Inventory system.|
|Look up IBM Product Release by Product ID|Retrieves the list of releases associated with an IBM software product.|
|Look up IBM Product Release Instances by Release ID|Retrieves the list of instances associated with an IBM software product release.|
|Look up IBM Product Release Instances Stream|Retrieves the list of Instances associated with the specified software product release.|
|Look up IBM Product Releases Stream|Retrieves the list of releases associated with the specified software product.|
|Look up IBM Software Products Stream|Retrieves the list of IBM software product details installed in the infrastructure.|
|Look up License Usages Stream|Lists peak license usage over the last 90 days.|
|Look up Software Components Stream|Lists software components in BigFix Inventory.|
|Look up Software Inventories Stream|Lists installed software in the infrastructure scanned by BigFix Inventory.|
|Look up VM Managers|Lists VM managers in the BigFix Inventory system.|
|Set End of Support Date for Software Component|Configures the End of Support Date for software component.|

For information about setting up the spoke, see [Set up the BigFix Inventory spoke](../task/setup-bigfix.md#).

## Spoke modules

The BigFix Inventory spoke provides the BigFix Inventory Spoke application that has these modules:

<table id="table_rh2_vdb_gvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Software Inventories

</td><td>

Displays details of all software inventories.

</td></tr><tr><td colspan="2">

Remote Table

</td></tr><tr><td>

Computers

</td><td>

Displays details of all computers in the BigFix Inventory.When users navigates to this module, the system retrieves this data and displays it for a duration of 5 minutes. After this duration, the data is deleted.

</td></tr></tbody>
</table>## Spoke user role

The BigFix Inventory spoke the bigfix\_admin \(sn\_bigfix\_in\_spoke.bigfix\_admin\) role. Users with this role can access the BigFix Inventory Spoke application.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r-credentials.md).

