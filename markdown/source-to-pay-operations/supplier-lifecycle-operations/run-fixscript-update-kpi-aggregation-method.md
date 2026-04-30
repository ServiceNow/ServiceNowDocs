---
title: Run fix script to update the Aggregation method field in the KPI table
description: Run this fix script to update the new fields added in the KPI table \(sn\_kpi\_kpi\) after the May 2025 Yokohama release.
locale: en-US
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Post-upgrade tasks for Supplier Case Management, Install Supplier Lifecycle Operations, Configuring Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Run fix script to update the Aggregation method field in the KPI table

Run this fix script to update the new fields added in the KPI table \(sn\_kpi\_kpi\) after the May 2025 Yokohama release.

## Before you begin

Role required: admin

After the upgrade, the new fields **Aggregation method**, **Collection level**, and **Current threshold value** are added in the KPI table \(sn\_kpi\_kpi\).

It is mandatory to run the script to be able to use new features for the existing KPI records. Without the aggregation method and current threshold values, the calculated KPI behavior and KPI performance calculations might get impacted.

**Note:**

For new KPI templates and KPIs, there’s no impact even if the script is not run.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  Search for the **KPI - May 2025 data upgrade script** script.

3.  Open the fix script record.

    **Note:** In the **Script** field, the batch size variable is set to 9500. If there are more than 9500 KPI records, you can do one of the following:

    -   Run the fix script repeatedly until all active records are checked and copied.
    -   In the **Script** field, set the LIMIT variable to a number equal to the number of KPI records in your instance and select **Update**.
4.  Select **Run Fix Script**.


**Parent Topic:**[Post-upgrade tasks for Supplier Case Management](../concept/post-upgrade-tasks-slo.md)

**Related topics**  


[Run fix script to update the KPI weighted score field in the KPI score table](run-fixscript-update-kpi-weighted-score.md)

[Run fix script to update the KPI Instruction field in the Supplier Task table](run-fixscript-update-kpi-instruction.md)

[Run fix scripts to enable Automated KPI collection](run-fixscript-automated-kpis.md)

[Run fix script to migrate existing data from the deprecated Action type column after upgrade](fix-script-deprecated-column.md)

[Run fix script to use the Supplier Manager Workspace after upgrading to the Yokohama release](access-smw-after-upgrade.md)

[Enable deprecated case types after upgrade](enable-deprecated-case-types.md)

[Processing the skipped supplier catalog item records after upgrade](../concept/process-skipped-records-upgrade.md)

