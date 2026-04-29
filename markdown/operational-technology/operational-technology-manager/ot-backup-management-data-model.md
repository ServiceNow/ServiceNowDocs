---
title: Operational Technology Backup Management data model
description: The Operational Technology \(OT\) Backup Management provides visibility and actionable insights on the backup of the OT devices. The class tables described below are interconnected and collectively form the Backup Management data model.
locale: en-US
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Operational Technology Manager, Operational Technology]
---

# Operational Technology Backup Management data model

The Operational Technology \(OT\) Backup Management provides visibility and actionable insights on the backup of the OT devices. The class tables described below are interconnected and collectively form the Backup Management data model.

Use the Backup Storage Information \[cmdb\_backup\_storage\_information\] class to create backup records that identify the device in internal or external backup services. The Backup Storage Information table includes the following attributes:

|Attributes|Description|
|----------|-----------|
|Backup Configuration Status|Indicates whether the CI has been configured in the backup service or appliance with relevant policies.|
|Discovery Source|Discovery source of the backup record.|
|Backup Service|Reference to the Common Service Data Model Technical Service hosting external and internal backup system, services, or appliances|
|Managed By|Name or ID of the user whi is responsible for managing the backup.|
|Latest Successful Execution|Date and time of the most recent data backup that was successfully executed for a device.|
|Latest Execution Attempt|Date and time of the most recent data backup that was attempted for a device.|
|Next Execution Attempt|Date and time when the next data backup is going to be attempted for a device.|
|Latest Execution Log|Detailed log entries for all device data backup that were executed.|
|Backup Source ID|Backup service record for a device, which identifies the device in external or internal backup services. Backup source id can include host\_id, vcenter\_id, instance\_id, db\_id.|
|Job Definition ID|Identification number assigned to a data backup job.|
|Recovery Point Objective|Amount of time that can elapse between backups and the amount of data lost.|
|Execution Mode|Indicates whether the backup is configured to run automatically on a periodic basis, or if it’s manually executed on an as-needed basis.|
|Backup Source|Details of the backed-up CI. This table holds the backup status details for the referenced CI.|
|Job Definition Name|Name assigned to a data backup job.|
|Managed By Group|Name of the user group responsible for managing the backup.|
|Domain|ID of the domain to which the instance belongs.|

Use the Backup Job Execution History \[cmdb\_backup\_job\_execution\_history\] class to create a history of records for all backup executions. The Backup Job Execution History table includes the following attributes:

|Attributes|Description|
|----------|-----------|
|Backup Job Information|Details of the backup job you created.|
|Backup End Time|The time when the backup job ended.|
|Completion Status|The current completion status of the backup job.|
|Mark for Archival|Select to archive backup job execution history after 90 days.|

Use the OT Backup Job Execution History \[ot\_backup\_history\_and\_comparision\_log\] class to compare the history of records for all backup executions. The Backup Log table includes the following attributes:

|Attribute|Description|
|---------|-----------|
|Current Version|The current version of the OT device.|
|Current Version vs Backup|Comparison between the current version of the OT device and the version information available in the backup record.|
|Current Version vs Backup Error|Comparison between the current version of the OT device and the version information available in the backup record that experienced an error during backup job execution.|
|Current Version vs Backup Warning|Comparison between the current version of the OT device and the version information available in the backup record that experienced a warning during backup job execution.|
|Previous Version vs Backup|Comparison between the previous recorded version of the OT device and the version information available in the backup record.|
|Previous Version vs Backup Error|Comparison between the previous recorded version of the OT device and the version information available in the backup record that experienced an error during backup job execution.|
|Previous Version vs Backup Warning|Comparison between the previous recorded version of the OT device and the version information available in the backup record that experienced a warning during backup job execution.|

**Parent Topic:**[Operational Technology Manager reference](operational-technology-manager-reference.md)

**Related topics**  


[Operational Technology \(OT\) extension classes](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

