---
title: SCCM data import process and source tables
description: The Microsoft SCCM versions supported in the ServiceNow platform offer identical features and the same imported data.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Microsoft SCCM integration, ServiceNow provided integrations, Integration options, Integration with third-party applications and data sources, Integrations, Configure core features, Administer]
---

# SCCM data import process and source tables

The Microsoft SCCM versions supported in the ServiceNow® platform offer identical features and the same imported data.

## Data import process

1.  A schedule called **SCCM System &lt;version&gt; Import** determines when the SCCM tables are imported into the ServiceNow® instance. Imports can be executed immediately or scheduled to run at defined intervals.
2.  A MID Server retrieves the SCCM data and imports it into staging tables on the instance.
3.  Transforms run on the data in the staging tables and map the SCCM data to existing fields in the CMDB.

![SCCM data import process](../image/SCCMDiagram.png)

## SCCM data imported

This table shows the SCCM source tables, the corresponding import set staging tables in the ServiceNow® instance, and the target tables in the CMDB.

<table id="table_kjy_3r4_j1b"><thead><tr><th>

SCCM table

</th><th>

Staging table

</th><th>

CMDB table

</th></tr></thead><tbody><tr><td>

-   v\_GS\_Computer\_System
-   v\_GS\_Workstation\_Status
-   v\_GS\_System
-   v\_GS\_PC\_Bios
-   v\_GS\_Operating\_System
-   v\_GS\_Computer\_System\_Product
-   v\_GS\_System\_Enclosure
-   v\_GS\_Baseboard

</td><td>

SCCM &lt;version&gt; Computer Identity \[imp\_sccm&lt;version&gt;\_computer\_id\]

</td><td>

Computer \[cmdb\_ci\_computer\]

</td></tr><tr><td>

v\_GS\_Disk

</td><td>

SCCM &lt;version&gt; Disk \[imp\_sccm&lt;version&gt;\_disk\]

</td><td>

Disk \[cmdb\_ci\_disk\]

</td></tr><tr><td>

v\_GS\_Network\_Adapter\_Configuration

</td><td>

SCCM &lt;version&gt; Network \[imp\_sccm&lt;version&gt;\_network\]

</td><td>

Network Adapter \[cmdb\_ci\_network\_adapter\]

</td></tr><tr><td>

v\_GS\_Operating\_System

</td><td>

SCCM &lt;version&gt; Operating System \[imp\_sccm&lt;version&gt;\_os\]

</td><td>

Computer \[cmdb\_ci\_computer\]

</td></tr><tr><td>

v\_GS\_Processor

</td><td>

SCCM &lt;version&gt; Processor \[imp\_sccm&lt;version&gt;\_processor\]

</td><td>

Computer \[cmdb\_ci\_computer\]

</td></tr><tr><td>

-   v\_GS\_Add\_Remove\_Programs
-   v\_GS\_Add\_Remove\_Programs\_64

</td><td>

SCCM &lt;version&gt; Software \[imp\_sccm&lt;version&gt;\_software\]

</td><td>

-   Software \[cmdb\_ci\_spkg\]
-   Software Installation \[cmdb\_sam\_sw\_install\] \(when Software Asset Management is enabled\*\)

</td></tr></tbody>
</table>\*For more information about Software Asset Management and how to enable it, see [Request Software Asset Management](https://www.servicenow.com/docs/access?context=t_RequSoftwareAssetMgmt&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US).

## SCCM data sources

The ServiceNow® SCCM integration uses JDBC data sources to import software data from the SCCM database. Each data source contains the connection specifics for the SCCM database and names the MID Server the instance will use to import the data. The transforms that map the SCCM fields to the CMDB are defined in a related list in each data source record.

## Transform maps

Transform maps are accessed from the **Transforms** related list in each data source record. The source fields in SCCM and the target fields in the CMDB are listed in the **Field Maps** related list in each Table Transform Map record. The SCCM integration uses the transform map utility provided with the ServiceNow® platform. For instructions on editing or creating a transform map, see [Transform maps](https://www.servicenow.com/docs/access?context=c_CreatingNewTransformMaps&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

The SCCM integration provides two transform maps for incremental software imports. Only one transform map can be enabled \(**Active**\) at a time.

-   **Incremental Import**: Enabled by default. This map should be configured as **Active** when ServiceNow® Software Asset Management is not enabled on the instance.
-   **Incremental Import \(SAM enabled\)**: If the Software Asset Management plugin is activated, set this transform to **Active**

**Note:** To force a one-time full import of all software data from the SCCM database, clear the value in the**Last run datetime** field on the data source. This operation can take a long time to execute, so the most efficient method is to use an incremental transform after the first full import.

## Transforming the assigned user

The SCCM &lt;version&gt; Computer Identity transform script attempts to set the **Assigned to** field in the CMDB record by looking up the name of the user in the SCCM source table and comparing the value with the matching field in the ServiceNow sys\_user table. If a match is found, that user is assigned to the record. If no match is found, the **Assigned to** field is left blank. The matching field is controlled by the **glide.discovery.assigned\_user\_match\_field** system property, which is set to **user\_name** by default.

## Identifiers

The SCCM integration uses CI identification to update CIs created from data imported from SCCM with a resource ID. The Hardware Rule identifier returns the resource ID of a computer from SCCM and stores it in the Source \[sys\_object\_source\] table. When resource IDs are first imported, either from SCCM or Discovery, the \[sys\_object\_source\] table is populated with IDs for each CI it identifies. In subsequent imports, if an incoming ID matches that of an existing CI, IRE \(Identification and Reconciliation Engine\) updates the information for that CI in the CMDB. If the incoming resource ID does not match that of an existing CI, IRE creates a new CI and populates it with the resource ID.

For more information about CMDB Identification and Reconciliation and IRE, see [CMDB Identification and Reconciliation](https://www.servicenow.com/docs/access?context=c_CMDBIdentifyandReconcile&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

Upgrades from pre-Geneva versions still preserve the legacy identifiers, but you can switch to the new identifiers using a property: `glide.discovery.use_cmdb_identifiers`. If you upgraded from a pre-Geneva version, you must manually add this property and set it to `true` to use the new identifiers. If you upgraded from Geneva, this property is available in the System Properties \[sys\_properties\] table. To preserve functionality in custom legacy identifiers, convert them to the new CMDB identifier rules format before enabling this property. The system does not reconfigure your custom identifiers to the new framework automatically.

## Scripts

Data population scripts populate the related data in the CMDB for each target CI discovered by the Hardware Rule identifier.

## Software

The Microsoft SCCM integration reconciles the software package count in the records for a CI and removes a software instance from the Software Instance \[cmdb\_software\_instance\] table if the software package is uninstalled from the CI. For a full software import, the transform populates the Software \[cmdb\_ci\_spkg\] and Software Instance \[cmdb\_software\_instance\] tables. If the Software Asset Management plugin is enabled, the transform populates the Software Installation \[cmdb\_sam\_sw\_install\] table.

**Note:** The table data imported from SCCM must contain complete data for the CI. The instance assumes that the import represents all relationships that exist and adjusts the CMDB accordingly. Partial data received from SCCM tables can cause the deletion of active relationships.

**Parent Topic:**[Microsoft SCCM integration](../concept/c_MicrosoftSCCMIntegration.md)

