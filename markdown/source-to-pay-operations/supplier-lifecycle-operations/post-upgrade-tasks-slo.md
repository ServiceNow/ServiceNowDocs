---
title: Post-upgrade tasks for Supplier Case Management
description: After you upgrade to Washington DC, you must review all the post-upgrade tasks and complete them as needed.
locale: en-US
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Install Supplier Lifecycle Operations, Configuring Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Post-upgrade tasks for Supplier Case Management

After you upgrade to Washington DC, you must review all the post-upgrade tasks and complete them as needed.

**Important:** The Supplier Lifecycle Operations plugin \(com.snc.sn\_supplier\_mgmt\) is renamed to Supplier Case Management in the Yokohama December 2025 \(v 5.2.0\) release.

-   **[Run fix script to update the KPI weighted score field in the KPI score table](../task/run-fixscript-update-kpi-weighted-score.md)**  
Run this fix script to update the KPI weighted score field values \(from integer to decimal type\) in the KPI score table \(sn\_kpi\_score\) after the March 2026 Yokohama release.
-   **[Run fix script to update the Aggregation method field in the KPI table](../task/run-fixscript-update-kpi-aggregation-method.md)**  
Run this fix script to update the new fields added in the KPI table \(sn\_kpi\_kpi\) after the May 2025 Yokohama release.
-   **[Run fix script to update the KPI Instruction field in the Supplier Task table](../task/run-fixscript-update-kpi-instruction.md)**  
Run this fix script to update the new field **KPI Instruction** added in the Supplier Task \(sn\_slm\_task\) table in the Yokohama release.
-   **[Run fix scripts to enable Automated KPI collection](../task/run-fixscript-automated-kpis.md)**  
Run the fix scripts to enable the Automated KPIs feature that automatically calculates KPI data from database tables instead of manually entering values.
-   **[Run fix script to migrate existing data from the deprecated Action type column after upgrade](../task/fix-script-deprecated-column.md)**  
In the May Store 2024 release, the **Action type** column in the Supplier Task \(sn\_slm\_task\) table has been deprecated.
-   **[Run fix script to use the Supplier Manager Workspace after upgrading to the Yokohama release](../task/access-smw-after-upgrade.md)**  
After upgrading to the Yokohama release, you can see only the Source-to-Pay Workspace on the **All** navigation tab. You don't have to do anything if you choose to continue to use the Source-to-Pay Workspace.
-   **[Enable deprecated case types after upgrade](../task/enable-deprecated-case-types.md)**  
After you upgrade to Yokohama, you can enable deprecated case types if you have the admin role.
-   **[Processing the skipped supplier catalog item records after upgrade](process-skipped-records-upgrade.md)**  
After you upgrade to Yokohama, the latest supplier catalog items may get skipped and therefore may not be available after the upgrade.

**Parent Topic:**[Install Supplier Lifecycle Operations](../task/install-supp-mgmt.md)

