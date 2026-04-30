---
title: Processing the skipped supplier catalog item records after upgrade
description: After you upgrade to Xanadu, the latest supplier catalog items may get skipped and therefore may not be available after the upgrade.
locale: en-US
release: xanadu
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Post-upgrade tasks for Supplier Lifecycle Operations, Install Supplier Lifecycle Operations, Configuring Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Processing the skipped supplier catalog item records after upgrade

After you upgrade to Xanadu, the latest supplier catalog items may get skipped and therefore may not be available after the upgrade.

For example, when onboarding a new supplier, the supplier onboarding flow includes a supplier task that creates a new record for supplier location and payment information using catalog items. Because the latest catalog items may not be available after the upgrade, the onboarding flow may get affected.

If you notice that the supplier catalog item records have been skipped during the upgrade, you must review the list of skipped records, evaluate how you want to resolve the conflict for these records, and take appropriate action. For more information about processing the skipped records, see [Process the skipped records list](https://www.servicenow.com/docs/access?context=upgrademon-process-skip-list&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

**Parent Topic:**[Post-upgrade tasks for Supplier Lifecycle Operations](post-upgrade-tasks-slo.md)

**Related topics**  


[Restructured Supplier Task table](supplier-task-table-restructure.md)

[Run Glide fix script to run the reparenting script](../task/run-glide-fix-script-for-reparenting-script.md)

[Run fix script to migrate existing data from the deprecated Action type column after upgrade](../task/fix-script-deprecated-column.md)

[Run fix script to use the Supplier Manager Workspace after upgrading to the Xanadu release](../task/access-smw-after-upgrade.md)

[Enable deprecated case types after upgrade](../task/enable-deprecated-case-types.md)

