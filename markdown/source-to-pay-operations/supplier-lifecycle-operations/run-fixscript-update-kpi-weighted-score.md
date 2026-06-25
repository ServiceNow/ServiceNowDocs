---
title: Run fix script to update the KPI weighted score field in the KPI score table
description: Run this fix script to update the KPI weighted score field values \(from integer to decimal type\) in the KPI score table \(sn\_kpi\_score\) after the March 2026 Australia release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/run-fixscript-update-kpi-weighted-score.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Post-upgrade tasks, Install Supplier Case Management, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Run fix script to update the KPI weighted score field in the KPI score table

Run this fix script to update the KPI weighted score field values \(from integer to decimal type\) in the KPI score table \(sn\_kpi\_score\) after the March 2026 Australia release.

## Before you begin

Role required: admin

After the upgrade, the old field **Weighted score** is replaced by **KPI weighted score** field in the KPI score \(sn\_kpi\_score\) table.

With the updated decimal type **KPI weighted score** field, all performance scores are calculated in decimal up to three decimal places.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  Search for the **Backfill KPI Weighted Score** script.

3.  Open the fix script record.

    **Note:** In the **Script** field, the batch size variable is set to 10000. If there are more than 10000 KPI records, you can do one of the following:

    -   Run the fix script repeatedly until all active records are checked and copied.
    -   In the **Script** field, set the batch size variable to a number equal to the number of KPI records in your instance and select **Update**.
4.  Select **Run Fix Script**.


**Parent Topic:**[Post-upgrade tasks for Supplier Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/post-upgrade-tasks-slo.md)

**Related topics**  


[Run fix script to update the Aggregation method field in the KPI table]()

[Run fix script to update the KPI Instruction field in the Supplier Task table]()

[Run fix scripts to enable Automated KPI collection]()

[Run fix script to migrate existing data from the deprecated Action type column after upgrade]()

[Run fix script to use the Supplier Manager Workspace after upgrading to the Australia release]()

[Enable deprecated case types after upgrade]()

[Processing the skipped supplier catalog item records after upgrade]()

