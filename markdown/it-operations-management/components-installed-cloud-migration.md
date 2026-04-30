---
title: Components installed with Cloud Migration Assessment
description: Several types of components are installed with the activation of the Cloud Migration Assessment plugin, including tables, user roles, properties, and scheduled jobs.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Cloud Migration Assessment reference, Cloud Migration Assessment, ITOM Cloud Accelerate, IT Operations Management]
---

# Components installed with Cloud Migration Assessment

Several types of components are installed with the activation of the Cloud Migration Assessment plugin, including tables, user roles, properties, and scheduled jobs.

## Roles installed

|Role title \[name\]|Description|Contains roles|
|-------------------|-----------|--------------|
|sn\_cloud\_migration.admin|Configures advanced parameters to customize the default behavior of Cloud Migration Assessment.|cloud\_migration\_operator|
|sn\_cloud\_migration.operator|Reviews the information on the discovered IT resources, assigns these resources to assessment tasks, and tracks the migration progress.|itil, canvas\_user|

## Scheduled jobs installed

|Scheduled job|Description|
|-------------|-----------|
|Cloud Migration - Populate Resources|Runs daily. Populates the Migration Resource \[sn\_cloud\_migration\_resource\] table with information about servers and virtual machines.|
|Cloud Migration - Update Application Counters|Runs on demand. Updates the Application Count of each resource by the number of applications running on each resource.|
|Cloud Migration Assessment Licensing Usage Count|Runs daily. Counts all resources in the Cloud Migration Assessment application that are assigned to a task. ServiceNow® ITOM SU Licensing application uses this information for counting licensable CIs.|

## Tables installed

|Table|Description|
|-----|-----------|
|Migration VM Metric \[sn\_cloud\_migration\_vm\_metrics\]|Contains the information about virtual machines and their metrics necessary for assessing IT infrastructure.|
|Software Requirement for Migration \[sn\_cloud\_migration\_software\_requirement\]|Contains the list of applications which run on servers that are assigned to assessment tasks.|
|Cloud Migration Assessment Task \[sn\_cloud\_migration\_task\]|Contains the information about a migration task for resources designated for migration to the cloud.|
|Base Migration Assessment Task \[sn\_cloud\_migration\_task\_base\]|Serves as the base table for different migration tasks that extend this table.|
|Assigned Resource for Migration \[sn\_cloud\_migration\_task\_resource\_m2m\]|Contains the information on the assignments of resources to tasks.|
|Migration Resource \[sn\_cloud\_migration\_resource\]|Contains the information about virtual machines, servers, and servers and virtual machines discovered together with the servers.|
|Migration Wave \[sn\_cloud\_migration\_wave\]|Gathers the assessment tasks and migration waves.|
|Cloud Migration Assessment Governance Licensing \[itom\_lu\_cloud\_migration\_assessment\_ci\]|Contains licensable CIs for Cloud Migration Assessment.|

## Properties installed

<table id="table_mvw_tfb_pt"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_cloud\_migration.os.exclusion\_list

</td><td>

A comma-separated deny list of operating systems. Servers with the operating systems listed here are excluded from the migration process.-   **Type**: String
-   **Default value**: ESX, Windows XP, Windows 7 Enterprise, Windows 7 Ultimate, Windows 10 Enterprise 2016 LTSB.
-   **Location**: **Cloud Migration** &gt; **Administration** &gt; **Properties**.

</td></tr><tr><td>

sn\_cloud\_migration.vm\_state.inclusion\_list

</td><td>

A comma-separated allow list of VM instance status for Cloud Migration Assessment. Only servers with the install status listed here can participate in the migration process-   **Type**: String
-   **Other possible values**: on, off, paused, scheduled, starting, stopping, retired, terminated, error, cancelled, pausing, terminating.
-   **Default value**: on
-   **Location**: **Cloud Migration** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

sn\_cloud\_migration.server\_status.inclusion\_list

</td><td>

A comma-separated allow list of server status for Cloud Migration Assessment. Only servers with the install status listed here can participate in the migration process.-   **Type**: string
-   **Default value**: 1
-   **Other possible values**: Installed=1, On Order=2, In Maintenance=3, Pending Install=4, Pending Repair=5, In Stock=6, Retired=7, Stolen=8, Absent=100.
-   **Location**: **Cloud Migration** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

sn\_cloud\_migration.categories.inclusion\_list

</td><td>

A comma-separated allow list of categories for Cloud Migration Assessment. Only resources assigned to categories that are listed here can participate in the migration process.-   **Type**: string
-   **Default value**: Physical,VMware, HyperV, IBM HMC,OpenStack, Solaris,Nutanix, Amazon AWS,Microsoft Azure,Google Cloud,IBM Cloud
-   **Location**: **Cloud Migration** &gt; **Administration** &gt; **Properties**

</td></tr></tbody>
</table>In addition to the listed components, Cloud Migration Assessment comes with the following VMware probe: VMWare - vCenter VM Performance. For more information, see [vCenter probes and probe parameters](../../discovery/reference/vcenter-probes.md#).

**Parent Topic:**[Cloud Migration Assessment reference](cloud-migration-reference.md)

