---
title: Validate imported staging records
description: Validate the imported staging records from your import task to find missing, duplicate, and invalid data.
locale: en-US
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using the Service Graph Connector for Microsoft Excel through import tasks, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Validate imported staging records

Validate the imported staging records from your import task to find missing, duplicate, and invalid data.

## Before you begin

Role required: ot\_excel\_import\_user

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace**.

2.  Select the **List** \(![List icon](../../../common/image/icon-list.png)\) icon.

3.  Under the OT Excel SGC - Import Task module, select one of the available lists.

4.  Select the Import Task record that you want to validate.

5.  Ensure you're the assigned to the import task so you can see the **Validate** UI action.

    **Note:** If you aren't in the **Assigned to** field of the import task, click the **Assign to me** UI action before proceeding with the next step.

6.  Click the **Validate** UI action.

    Once the validation process is complete, the **State** field of the Import Task record changes to **Validation complete**. The **Validation state** of the staging records created can update to one of the following values.

    -   Valid
    -   Invalid
    -   Partially invalid
    If invalid, the **Validation comments** field contains the cause or causes of the invalid state.

    If an imported staging record matches an existing configuration item \(CI\) in the CMDB, you can preview the existing OT records. For more information, see [Preview existing OT records in the CMDB](preview-existing-asset-records.md).


## What to do next

For valid records, you can directly trigger the Configuration Management Database \(CMDB\) import. For more information, see [Trigger a CMDB import for valid staging records](trigger-cmdb-import.md).

To resolve invalid or partially invalid records, you can optionally create remediation tasks. For more information, see [Create a remediation task for invalid staging records](create-remediation-task-for-validation-errors.md).

-   **[Managing Validations](../concept/managing-validations.md)**  
Validation enables you to review and manage the imported data in the staging table.
-   **[Preview existing OT records in the CMDB](preview-existing-asset-records.md)**  
Preview existing Operational Technology \(OT\) device records in the Configuration Management Database \(CMDB\) before you import any new records from the staging table. By previewing existing records, you can avoid reconciling or merging unrelated records.

**Parent Topic:**[Using the Service Graph Connector for Microsoft Excel through import tasks](../concept/use-excel-sgc-through-import-tasks.md)

