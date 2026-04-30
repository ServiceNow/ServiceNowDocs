---
title: Run fix script to use the Supplier Manager Workspace after upgrading to the Australia release
description: After upgrading to the Australia release, you can see only the Source-to-Pay Workspace on the All navigation tab. You don't have to do anything if you choose to continue to use the Source-to-Pay Workspace.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Post-upgrade tasks, Install Supplier Case Management, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Run fix script to use the Supplier Manager Workspace after upgrading to the Australia release

After upgrading to the Australia release, you can see only the Source-to-Pay Workspace on the **All** navigation tab. You don't have to do anything if you choose to continue to use the Source-to-Pay Workspace.

## Before you begin

Role required: admin

## About this task

**Important:** To use the Supplier Manager Workspace without any issues, ensure that you are on the latest version of the Vancouver release \(2.4.4\) before upgrading to Washington DC or later releases. For more information, see the KB article [KB1651502](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1651502).

After upgrading to the Australia release, you can see both the Source-to-Pay Workspace and Supplier Manager Workspace on the **Workspaces** tab. If you want to use the Supplier Manager Workspace instead of the default Source-to-Pay Workspace, run the **fixscript\_migrate\_workspace\_to\_smw.xml** fix script.

At any time, you can revert to using the Source-to-Pay Workspace by running the **fixscript\_migrate\_workspace\_to\_s2p.xml** fix script.

You can download the fix script XML files from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do).![Download fix script from Supporting Links and Docs section.](../image/smw-script-store.jpg)

## Procedure

1.  Download the fix script XML file from the Supporting Links and Docs section.

2.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

3.  Right-click the Name column and choose **Import XML**.

4.  Select **Choose file** and then select the fix script XML file that you downloaded.

5.  Select **Upload**.

6.  Search for and select the fix script record to open it.

7.  Select **Run Fix Script**.


**Parent Topic:**[Post-upgrade tasks for Supplier Case Management](../concept/post-upgrade-tasks-slo.md)

**Related topics**  


[Run fix script to update the KPI weighted score field in the KPI score table](run-fixscript-update-kpi-weighted-score.md)

[Run fix script to update the Aggregation method field in the KPI table](run-fixscript-update-kpi-aggregation-method.md)

[Run fix script to update the KPI Instruction field in the Supplier Task table](run-fixscript-update-kpi-instruction.md)

[Run fix scripts to enable Automated KPI collection](run-fixscript-automated-kpis.md)

[Run fix script to migrate existing data from the deprecated Action type column after upgrade](fix-script-deprecated-column.md)

[Enable deprecated case types after upgrade](enable-deprecated-case-types.md)

[Processing the skipped supplier catalog item records after upgrade](../concept/process-skipped-records-upgrade.md)

[Run fix script to migrate existing data from the deprecated Action type column after upgrade](fix-script-deprecated-column.md)

[Run fix script to update the KPI Instruction field in the Supplier Task table](run-fixscript-update-kpi-instruction.md)

[Restructured Supplier Task table](../concept/supplier-task-table-restructure.md)

