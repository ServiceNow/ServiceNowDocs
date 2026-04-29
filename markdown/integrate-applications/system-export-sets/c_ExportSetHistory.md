---
title: Export set history
description: An export set history record is automatically created whenever an export set runs, either scheduled or manually started by a user. Export set history records allow you to monitor and troubleshoot the progress of export sets.
locale: en-US
release: australia
product: System Export Sets
classification: system-export-sets
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Export sets, Exports, Workflow Data Fabric]
---

# Export set history

An export set history record is automatically created whenever an export set runs, either scheduled or manually started by a user. Export set history records allow you to monitor and troubleshoot the progress of export sets.

Fields on the Export History form display the current status of the export set. The **Export Log** related list shows a detailed list of changes to the export set status.

|Field|Description|
|-----|-----------|
|Export set|The export set that was run.|
|Started|The date and time the export started.|
|Completed|The date and time the export completed.|
|Export time|The amount of time it took to export the data, excluding the time it took to transfer the data to the target.|
|Run time|The amount of time it took to export the data, including the time it took to transfer the data to the target.|
|State|The current state of the export.|
|Delta export|The export used delta export functionality if this check box is selected.|
|ECC queue|The ECC Queue record associated with this export set run. This field is visible only to users with the admin role.|
|MID Server Attachment|A MID Server attachment record containing a copy of the exported file. The exported file is attached to this record in addition to being saved on the MID Server.|

The **State** field may have the following values.

|State|Description|
|-----|-----------|
|Exporting|The export set is creating a file with the data to export.|
|MID Server Processing|The export set successfully created a file with the data to export. The file is being processed by the MID Server.|
|Completed|The export set successfully ran and sent the exported file to the target.|
|Completed with errors|The export set ran, but encountered one or more errors.|
|Cancel requested|A user requested that the export set be cancelled.|
|Cancelled|The export set was cancelled.|

## Parallel export history

Export history records include two fields for parallel exports:

-   **Parallel Export Set**: References the parent parallel export set record
-   **Parallel Export Set Job:** References the specific chunk/job record

For standard exports, these fields remain empty. For parallel exports, multiple export history records are created \(one per chunk\), and all records share the same Parallel Export Set reference. Each export history record contains one exported file attachment.

To identify the export type:

-   Standard export: **Parallel Export Set** field is empty
-   Parallel export: **Parallel Export Set** field is populated

