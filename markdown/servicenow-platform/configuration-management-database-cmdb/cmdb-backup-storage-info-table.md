---
title: Backing up CMDB data
description: The cmdb\_backup\_storage\_information table \(part of the \[app-cmdb-content\] ServiceNow Store application\) holds generic backup storage information for a CI as a platform related item. The table includes a CI as a reference attribute and stores information for hardware, cloud, containers, and other CI types.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Backing up CMDB data

The cmdb\_backup\_storage\_information table \(part of the \[app-cmdb-content\] ServiceNow Store application\) holds generic backup storage information for a CI as a platform related item. The table includes a CI as a reference attribute and stores information for hardware, cloud, containers, and other CI types.

## Backup Store Information \[cmdb\_backup\_storage\_information\] table

The table captures backup policy, last successful backup, last backup attempt, execution mode, backup source, backup source ID, and backup service.

To mitigate the risk of uncontrolled growth of the table, a cascade-delete rule applies to the Backup Source \(CI\) reference field. When a CI is deleted, the corresponding rows in the table are deleted.

![Diagram of the references that the cmdb_backup_storage_information table makes to the technical service and backup source tables.](../image/cmdb-backup-storage-info-table.png)

## Tables related to backup operations

<table id="table_nmr_dmw_gdc"><thead><tr><th>

Table

</th><th>

Contents

</th></tr></thead><tbody><tr><td>

Backup Store Information \[cmdb\_backup\_storage\_information\]

</td><td>

Informational object that stores CI backup/snapshot information.

</td></tr><tr><td>

cmdb\_related\_entry

</td><td>

To populate the cmdb\_backup\_storage\_information with an IRE payload, you define a CMDB-related rule in cmdb\_related\_entry. For the related rule, use the Backup Source ID criteria attributes and Backup Source as a reference field. Example:```
//. Sample IRE payload  var payload = 
{ 
 "items": [ 
   { 
     "className": "cmdb_ci_hardware", 
      "sys_object_source_info": { 
       "source_name": "ServiceNow", 
       "source_native_key": "some key" 
     }, 
     "values": { 
       "name": "I am a good cat" 
     }, 
     "lookup": [], 
     "related": [ 
       { 
         "className": " cmdb_backup_storage_information", 
         "values": { 
           "backup_policy": "true", 
           "last_backup": "2023-02-02", 
           “backup_id”:”sede-09191-fet” 
         } 
       } 
     ] 
   } 
 ] } 
var jsonUntil = new JSON(); var input = jsonUntil.encode(payload); 
var output = SNC.IdentificationEngineScriptableApi.createOrUpdateCI('ServiceNow', input); gs.print(output); 

```

</td></tr><tr><td>

sys\_security\_acl

</td><td>

Reports and user access.

</td></tr><tr><td>

sys\_ui\_related

</td><td>

Multisource configuration, default forms.

</td></tr></tbody>
</table>## Columns in cmdb\_backup\_storage\_information

<table id="table_x5z_fnb_hdc"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Backup Configuration Status

 \[backup\_config\_status\]

</td><td>

String \(choice\)

 -   Backup Disabled \[False, default\]: CI has not been configured for regular backup.
-   Backup Enabled \[True\]: CI has policies and configurations defined in the backup system, service, or appliance for regular backups
-   Unknown
-   Not Applicable
-   Planned
-   Not Planned

</td></tr><tr><td>

Last Successful Backup \[last\_successful\_backup\]

</td><td>

glide\_date\_time

 Date and time of last successful backup. Platform-specific value that can be either the start or end of the backup attempt as reported by the platform API. If ambiguous, use the start time of the backup attempt.

</td></tr><tr><td>

Last Backup Attempt \[last\_backup\_attempt\]

</td><td>

glide\_date\_time

 Date and time of the last successful or failed backup attempt. Platform-specific value that can be either the start or the end of the backup attempt as reported by the platform API. If ambiguous, use the start time of the backup attempt.

 For a successful backup, both last\_backup and last\_backup\_attempt will have the same value.

</td></tr><tr><td>

Execution Mode \[backup\_execution\_mode\]

</td><td>

String \(choice\)

 -   Manual: Run as needed.
-   Automatic: Run periodically.
-   Unknown

</td></tr><tr><td>

sys\_domain and sys\_domain\_path

</td><td>

glide columns

 Values copied from cmdb\_ci.

</td></tr><tr><td>

managed\_by and managed\_by\_group

</td><td>

Values copied from cmdb\_ci.

</td></tr><tr><td>

Backup Source \[backup\_source\_ configuration\_item\]

</td><td>

reference \(ci\)

 Backup status details for the referenced CI being backed up.

</td></tr><tr><td>

Backup Source ID \[backup\_source\_id\]

</td><td>

String \(1024\)

 Backup Service source identifier for the CI. Identifies the CI in external/internal backup service such as host\_id, vcenter\_id, instance\_id, and db\_id.

</td></tr><tr><td>

Backup Service \[backup\_service\_ configuration\_item\]

</td><td>

reference \(ci\)

 Reference to the CSDM technical service that hosts the external or internal backup system, service, or appliance.

</td></tr><tr><td>

Recovery Point Objective \[recovery\_point\_objective\]

</td><td>

Duration

 Time that can elapse between backups and the acceptable amount of data loss.

</td></tr></tbody>
</table>