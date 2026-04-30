---
title: Run Glide fix script to run the reparenting script
description: Run the Glide fix script to take advantage of the new enhancements in Supplier Lifecycle Operations.
locale: en-US
release: xanadu
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-02-24"
reading_time_minutes: 1
breadcrumb: [Post-upgrade tasks for Supplier Lifecycle Operations, Install Supplier Lifecycle Operations, Configuring Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Run Glide fix script to run the reparenting script

Run the Glide fix script to take advantage of the new enhancements in Supplier Lifecycle Operations.

## About this task

This fix script is required to reparent the Task table or Supplier Task table on instances with huge count of records \(in millions\). It’s advisable to run the fix script during a period of low interaction.

This is a mandatory one-time fix script to be run on instances upgrading directly to Xanadu from Vancouver or older versions.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  Search for the **glidefix\_script\_reparent\_sn\_slm\_task** script.

3.  Open the fix script record.

4.  Select **Run Fix Script**.

    For more information, please see [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB1647660](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1647660).


**Parent Topic:**[Post-upgrade tasks for Supplier Lifecycle Operations](../concept/post-upgrade-tasks-slo.md)

**Related topics**  


[Restructured Supplier Task table](../concept/supplier-task-table-restructure.md)

[Run fix script to migrate existing data from the deprecated Action type column after upgrade](fix-script-deprecated-column.md)

[Run fix script to use the Supplier Manager Workspace after upgrading to the Xanadu release](access-smw-after-upgrade.md)

[Enable deprecated case types after upgrade](enable-deprecated-case-types.md)

[Processing the skipped supplier catalog item records after upgrade](../concept/process-skipped-records-upgrade.md)

