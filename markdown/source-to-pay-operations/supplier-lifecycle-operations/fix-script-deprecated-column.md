---
title: Run fix script to migrate existing data from the deprecated Action type column after upgrade
description: In the May Store 2024 release, the Action type column in the Supplier Task \(sn\_slm\_task\) table has been deprecated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/fix-script-deprecated-column.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Post-upgrade tasks, Install Supplier Case Management, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Run fix script to migrate existing data from the deprecated Action type column after upgrade

In the May Store 2024 release, the **Action type** column in the Supplier Task \(sn\_slm\_task\) table has been deprecated.

## Before you begin

Role required: admin

## About this task

In the May Store 2024 release, the Supplier Task \(sn\_slm\_task\) table uses the **Action type for task** column from its parent Service Task \[sn\_spend\_sdc\_service\_task\] table. After you upgrade to the May Store 2024 release, ensure that you run the fix script to migrate existing data from the deprecated **Action type** column to the newly added **Action type for task** column in the Supplier Task table.

**Important:** Before you run the fix script, ensure that you restructure the Supplier Task table to extend the Service Task table.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  Search for the **SLO - upgrade scripts for may 2024** script.

3.  Open the fix script record.

4.  In the **Script** field, set the batch size variable to a number equal to the number of supplier task records in your instance.

    For example, if your instance has 10000 supplier task records, set the batch size variable as follows:

    `var batchSize = 10000;`

5.  Select **Update**.

6.  Select **Run Fix Script**.


**Parent Topic:**[Post-upgrade tasks for Supplier Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/post-upgrade-tasks-slo.md)

**Related topics**  


[Run fix script to update the KPI weighted score field in the KPI score table]()

[Run fix script to update the Aggregation method field in the KPI table]()

[Run fix script to update the KPI Instruction field in the Supplier Task table]()

[Run fix scripts to enable Automated KPI collection]()

[Run fix script to use the Supplier Manager Workspace after upgrading to the Australia release]()

[Enable deprecated case types after upgrade]()

[Processing the skipped supplier catalog item records after upgrade]()

[Run fix script to update the KPI Instruction field in the Supplier Task table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/run-fixscript-update-kpi-instruction.md)

[Run fix script to use the Supplier Manager Workspace after upgrading to the Australia release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/access-smw-after-upgrade.md)

[Restructured Supplier Task table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/supplier-task-table-restructure.md)

