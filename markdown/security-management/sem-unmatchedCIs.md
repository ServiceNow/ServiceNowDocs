---
title: Managing unmatched configuration items \(CIs\)
description: When assets are imported, they are automatically matched against existing CIs in your Configuration Management Database \(CMDB\). Assets that do not find a match are listed as 'Unmatched CIs' under Discovered Items.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Associating finding with a configuration item using lookup rules, Automating prioritization and triaging, Security Exposure Management workflow, Explore, Unified Security Exposure Management, Security Operations]
---

# Managing unmatched configuration items \(CIs\)

When assets are imported, they are automatically matched against existing CIs in your Configuration Management Database \(CMDB\). Assets that do not find a match are listed as 'Unmatched CIs' under Discovered Items.

## Locating unmatched CIs

You can view these unmatched configuration items in the **Security Operations** &gt; **CMDB** &gt; **Discovered Items** module. By default, this list is filtered to show only "unmatched" items. To see all discovered items from an import, simply remove this filter.

## Taking action on Unmatched CIs

-   **Review Lookup rules:** If you believe an unmatched CI should belong to an existing class within the CMDB, it's recommended to review your lookup rules. This can help ensure proper matching in the future. See [Create lookup rule](sem-configure-lookup-rules.md#) for more information.
-   **Consider reclassification:** If a CI doesn't fit an existing class, you may need to reclassify it to ensure accurate CMDB data. See [reclassifying the configuration item](../../vulnerability-response/task/view-discovered-items.md) for more information.

**Note:** If the Identification and Reconciliation Engine \(IRE\) is active, the reclassify option for discovered items is not supported.

**Parent Topic:**[Associating finding with a configuration item using lookup rules](sem-associate-finding-configuration-item-using-lookup-rules.md)

**Related topics**  


[View and reclassify unmatched configuration items](../../vulnerability-response/task/view-discovered-items.md)

[Reconcile unmatched discovered items](../../vulnerability-response/task/reapply-reconcile-unmatched-discovered-items.md)

[Steps to help prevent duplicate or orphaned records after running Vulnerability Response CI lookup rules](../../security-operations-common/concept/ci-identifier-rules-impl-test.md)

[De-duplicating existing configuration items](../../vulnerability-response/concept/reapply-deduplication.md)

