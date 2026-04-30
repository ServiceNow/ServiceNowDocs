---
title: Restructured Supplier Task table
description: The Supplier Task table architecture has been restructured in the Washington DC release.
locale: en-US
release: xanadu
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Post-upgrade tasks for Supplier Lifecycle Operations, Install Supplier Lifecycle Operations, Configuring Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Restructured Supplier Task table

The Supplier Task table architecture has been restructured in the Washington DC release.

In releases before the Washington DC release, the Supplier Task \[sn\_slm\_task\] table extended the Task \[task\] table.

Starting with the Washington DC release, the Supplier Task \[sn\_slm\_task\] table extends the Service Task \[sn\_spend\_sdc\_service\_task\] table.

![Supplier Task table structure](../image/supplier-task-structure.png "Supplier Task table structure")

After you upgrade to the Xanadu release, verify that your existing supplier task data has been migrated correctly. If you notice that your active Supplier Task table did not migrate properly, use the [Now Support Portal](https://support.servicenow.com/now) to raise a new case with the Technical Support team.

Also, after you upgrade to the Washington DC release, the fix script `glidefix_script_reparent_sn_slm_task.xml` runs to reparent the Supplier Task table on instances with huge count of records \(in millions\). Therefore, it’s advisable to run the upgrade during a period of low interaction.

**Note:** This is a mandatory one-time fix script run on instances upgrading directly to Washington DC from Vancouver or older versions.

**Parent Topic:**[Post-upgrade tasks for Supplier Lifecycle Operations](post-upgrade-tasks-slo.md)

**Related topics**  


[Run Glide fix script to run the reparenting script](../task/run-glide-fix-script-for-reparenting-script.md)

[Run fix script to migrate existing data from the deprecated Action type column after upgrade](../task/fix-script-deprecated-column.md)

[Run fix script to use the Supplier Manager Workspace after upgrading to the Xanadu release](../task/access-smw-after-upgrade.md)

[Enable deprecated case types after upgrade](../task/enable-deprecated-case-types.md)

[Processing the skipped supplier catalog item records after upgrade](process-skipped-records-upgrade.md)

