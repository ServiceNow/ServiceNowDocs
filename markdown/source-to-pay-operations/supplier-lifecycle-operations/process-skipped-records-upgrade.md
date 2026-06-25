---
title: Processing the skipped supplier catalog item records after upgrade
description: After you upgrade to Australia, the latest supplier catalog items may get skipped and therefore may not be available after the upgrade.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/process-skipped-records-upgrade.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Post-upgrade tasks, Install Supplier Case Management, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Processing the skipped supplier catalog item records after upgrade

After you upgrade to Australia, the latest supplier catalog items may get skipped and therefore may not be available after the upgrade.

For example, when onboarding a new supplier, the supplier onboarding flow includes a supplier task that creates a new record for supplier location and payment information using catalog items. Because the latest catalog items may not be available after the upgrade, the onboarding flow may get affected.

If you notice that the supplier catalog item records have been skipped during the upgrade, you must review the list of skipped records, evaluate how you want to resolve the conflict for these records, and take appropriate action.

**Parent Topic:**[Post-upgrade tasks for Supplier Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/post-upgrade-tasks-slo.md)

**Related topics**  


[Run fix script to update the KPI weighted score field in the KPI score table]()

[Run fix script to update the Aggregation method field in the KPI table]()

[Run fix script to update the KPI Instruction field in the Supplier Task table]()

[Run fix scripts to enable Automated KPI collection]()

[Run fix script to migrate existing data from the deprecated Action type column after upgrade]()

[Run fix script to use the Supplier Manager Workspace after upgrading to the Australia release]()

[Enable deprecated case types after upgrade]()

[Enable deprecated case types after upgrade](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/enable-deprecated-case-types.md)

[Restructured Supplier Task table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/supplier-task-table-restructure.md)

