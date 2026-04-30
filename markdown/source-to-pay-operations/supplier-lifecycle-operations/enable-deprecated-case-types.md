---
title: Enable deprecated case types after upgrade
description: After you upgrade to Xanadu, you can enable deprecated case types if you have the admin role.
locale: en-US
release: xanadu
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Post-upgrade tasks for Supplier Lifecycle Operations, Install Supplier Lifecycle Operations, Configuring Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Enable deprecated case types after upgrade

After you upgrade to Xanadu, you can enable deprecated case types if you have the admin role.

## Before you begin

Role required: admin

## About this task

In the xanadu release, the **Conduct a risk assessment** and **Conduct a tiering risk assessment** case types have been deprecated. However, you can perform this task to enable and use these case types after upgrade.

## Procedure

1.  Select **All**.

2.  In the navigation filter, enter **sn\_slm\_case\_list.do**.

    The Supplier Cases page opens listing all the supplier cases.

3.  Select **New**.

4.  Right-click the **Case type** field label and select **Configure Choices**.

    The Configuring Case type Choices page opens.

5.  In the Available list, double-click the **Conduct a risk assessment \(Deprecated\)** and **Conduct a tiering risk assessment \(Deprecated\)** case types to move them to the Selected list.

6.  Select **Save**.

    The deprecated case types now appear in the **Case type** field on the Create New Supplier Case form.


**Parent Topic:**[Post-upgrade tasks for Supplier Lifecycle Operations](../concept/post-upgrade-tasks-slo.md)

**Related topics**  


[Restructured Supplier Task table](../concept/supplier-task-table-restructure.md)

[Run Glide fix script to run the reparenting script](run-glide-fix-script-for-reparenting-script.md)

[Run fix script to migrate existing data from the deprecated Action type column after upgrade](fix-script-deprecated-column.md)

[Run fix script to use the Supplier Manager Workspace after upgrading to the Xanadu release](access-smw-after-upgrade.md)

[Processing the skipped supplier catalog item records after upgrade](../concept/process-skipped-records-upgrade.md)

