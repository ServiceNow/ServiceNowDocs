---
title: Run fix scripts to enable Automated KPI collection
description: Run the fix scripts to enable the Automated KPIs feature that automatically calculates KPI data from database tables instead of manually entering values.
locale: en-US
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Post-upgrade tasks for Supplier Case Management, Install Supplier Lifecycle Operations, Configuring Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Run fix scripts to enable Automated KPI collection

Run the fix scripts to enable the Automated KPIs feature that automatically calculates KPI data from database tables instead of manually entering values.

## Before you begin

Role required: admin

**Note:** This feature is available from the Yokohama December 2025 release onwards.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  Search for **KPI - Dec 25 records script**.

3.  Open the fix script record.

4.  Select **Run Fix Script**.

5.  Repeat steps 2-4 to run the **KPI - Dec 25 data records script**.


## Result

After running the fix script, a new field **Data collection type** is added in the KPI Template \[sn\_kpi\_template\] table.

**Parent Topic:**[Post-upgrade tasks for Supplier Case Management](../concept/post-upgrade-tasks-slo.md)

**Related topics**  


[Run fix script to update the KPI weighted score field in the KPI score table](run-fixscript-update-kpi-weighted-score.md)

[Run fix script to update the Aggregation method field in the KPI table](run-fixscript-update-kpi-aggregation-method.md)

[Run fix script to update the KPI Instruction field in the Supplier Task table](run-fixscript-update-kpi-instruction.md)

[Run fix script to migrate existing data from the deprecated Action type column after upgrade](fix-script-deprecated-column.md)

[Run fix script to use the Supplier Manager Workspace after upgrading to the Yokohama release](access-smw-after-upgrade.md)

[Enable deprecated case types after upgrade](enable-deprecated-case-types.md)

[Processing the skipped supplier catalog item records after upgrade](../concept/process-skipped-records-upgrade.md)

[Run fix script to update the Aggregation method field in the KPI table](run-fixscript-update-kpi-aggregation-method.md)

[Run fix script to update the KPI Instruction field in the Supplier Task table](run-fixscript-update-kpi-instruction.md)

