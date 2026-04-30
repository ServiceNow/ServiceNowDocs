---
title: Operational Technology Version Control data model for Backup Management
description: In Operational Technology \(OT\) Backup Management, you can develop multiple scripts or programs to automate the data backup process of OT devices. The Version Control data model enables you to maintain a record of all the backup scripts or programs you develop for an OT entity.
locale: en-US
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Operational Technology Manager, Operational Technology]
---

# Operational Technology Version Control data model for Backup Management

In Operational Technology \(OT\) Backup Management, you can develop multiple scripts or programs to automate the data backup process of OT devices. The Version Control data model enables you to maintain a record of all the backup scripts or programs you develop for an OT entity.

The following class tables are interconnected and collectively form the Version Control data model for Operational Technology \(OT\) Backup Management data model.

Use the OT Automation Repo \(sn\_ot\_automation\_repo\) class as a repository to store all configuration changes you want to perform on an OT entity. The following attributes are available in the class:

|Attribute|Description|
|---------|-----------|
|Project Last Updated|Date and time of the most recent changes to the project.|
|Comments|Additional information provided by the OT engineer.|
|Is multiple edits enabled|Select **Yes** or **No** to enable multiple edits to the project.|
|Days since current state|Number of days that have passed since the project has been in the present status.|
|Latest version|Current version of the OT device the project is assigned to.|
|Project State|Status of the project.|

Use the OT Automation Repo Device M2M \(sn\_ot\_automation\_repo\_device\_m2m\) class as a reference to the OT Automation repository and the OT Entity table. The following attributes are available in the class:

|Attribute|Description|
|---------|-----------|
|Automation Repo|The repository where all project modifications and configurations are stored.|
|OT Entity|The OT Entity to which the project has been assigned.|

Use the OT AutomationCommit \(sn\_ot\_automation\_commit\) class as a reference to the changes you have committed to a project. The following attributes are available in the class:

|Attribute|Description|
|---------|-----------|
|Automation Version|The version of the script or the program committed for the OT entity.|

**Parent Topic:**[Operational Technology Manager reference](operational-technology-manager-reference.md)

**Related topics**  


[Operational Technology Backup Management data model](ot-backup-management-data-model.md)

