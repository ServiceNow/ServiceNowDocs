---
title: Run fix scripts to enable Automated KPI collection
description: Run the fix scripts to enable the Automated KPIs feature that automatically calculates KPI data from database tables instead of manually entering values.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/run-fixscript-automated-kpis.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Post-upgrade tasks, Install Supplier Case Management, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Run fix scripts to enable Automated KPI collection

Run the fix scripts to enable the Automated KPIs feature that automatically calculates KPI data from database tables instead of manually entering values.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  Search for **KPI - Dec 25 records script**.

3.  Open the fix script record.

4.  Select **Run Fix Script**.

5.  Repeat steps 2-4 to run the **KPI - Dec 25 data records script**.


## Result

After running the fix script, a new field **Data collection type** is added in the KPI Template \[sn\_kpi\_template\] table.

**Parent Topic:**[Post-upgrade tasks for Supplier Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/post-upgrade-tasks-slo.md)

**Related topics**  


[Run fix script to update the KPI weighted score field in the KPI score table]()

[Run fix script to update the Aggregation method field in the KPI table]()

[Run fix script to update the KPI Instruction field in the Supplier Task table]()

[Run fix script to migrate existing data from the deprecated Action type column after upgrade]()

[Run fix script to use the Supplier Manager Workspace after upgrading to the Australia release]()

[Enable deprecated case types after upgrade]()

[Processing the skipped supplier catalog item records after upgrade]()

[Run fix script to update the Aggregation method field in the KPI table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/run-fixscript-update-kpi-aggregation-method.md)

[Run fix script to update the KPI Instruction field in the Supplier Task table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/run-fixscript-update-kpi-instruction.md)

