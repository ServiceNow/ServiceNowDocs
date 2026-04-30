---
title: Run fix script to update the KPI Instruction field in the Supplier Task table
description: Run this fix script to update the new field KPI Instruction added in the Supplier Task \(sn\_slm\_task\) table in the Zurich release.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Post-upgrade tasks, Install Supplier Case Management, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Run fix script to update the KPI Instruction field in the Supplier Task table

Run this fix script to update the new field **KPI Instruction** added in the Supplier Task \(sn\_slm\_task\) table in the Zurich release.

## Before you begin

Role required: admin

After the upgrade, a new field **KPI Instruction** is added in the Supplier Task \(sn\_slm\_task\) table.

The new field **KPI Instruction** added in the Supplier Task \(sn\_slm\_task\) table is derived from the KPI table \(sn\_kpi\_kpi\) **Instructions** field. Run this fix script to transfer data from the dot-walked **kpi\_data.kpi.instructions** field to the **KPI Instruction** field in the Supplier Task table.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  Search for the **SLO - Feb 25 data script** script.

3.  Open the fix script record.

    **Note:** In the **Script** field, the batch size variable is set to 1000. If there are more than 1000 supplier task records, you can do one of the following:

    -   Run the fix script repeatedly until all active records are checked and copied.
    -   In the **Script** field, set the batch size variable to a number equal to the number of supplier task records in your instance and select **Update**.
4.  Select **Run Fix Script**.

    The script updates the **KPI Instruction** field value for the records where all the following conditions are met:

    -   The supplier task is active
    -   The supplier task is created to collect KPI data
    -   The **KPI Instruction** field is empty

**Parent Topic:**[Post-upgrade tasks for Supplier Case Management](../concept/post-upgrade-tasks-slo.md)

**Related topics**  


[Run fix script to update the KPI weighted score field in the KPI score table](run-fixscript-update-kpi-weighted-score.md)

[Run fix script to update the Aggregation method field in the KPI table](run-fixscript-update-kpi-aggregation-method.md)

[Run fix scripts to enable Automated KPI collection](run-fixscript-automated-kpis.md)

[Run fix script to migrate existing data from the deprecated Action type column after upgrade](fix-script-deprecated-column.md)

[Run fix script to use the Supplier Manager Workspace after upgrading to the Zurich release](access-smw-after-upgrade.md)

[Enable deprecated case types after upgrade](enable-deprecated-case-types.md)

[Processing the skipped supplier catalog item records after upgrade](../concept/process-skipped-records-upgrade.md)

[Run fix script to migrate existing data from the deprecated Action type column after upgrade](fix-script-deprecated-column.md)

[Run fix script to use the Supplier Manager Workspace after upgrading to the Zurich release](access-smw-after-upgrade.md)

[Restructured Supplier Task table](../concept/supplier-task-table-restructure.md)

