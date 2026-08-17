---
title: Revert a product adoption roadmap to a previous version
description: Restore a product adoption roadmap to the state captured in a previous published version.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/account-lifecycle-revert-par-roadmap.html
release: australia
topic_type: task
last_updated: "2026-07-26"
reading_time_minutes: 1
breadcrumb: [View a product adoption roadmap, Product adoption, Customer success, Use, Customer Success Management]
---

# Revert a product adoption roadmap to a previous version

Restore a product adoption roadmap to the state captured in a previous published version.

## Before you begin

-   The roadmap must have at least one previous published version.
-   Role required: sn\_acct\_lc.customer\_success\_agent

## About this task

Reverting a roadmap restores the lanes and items from the selected version record. The roadmap header state remains unchanged. A work note is automatically added to the version record, documenting the **Revert** action and the version label that was restored.

## Procedure

1.  Open the product adoption roadmap record you want to revert.

2.  Scroll to the **Versions** related list and open the version record you want to revert to.

3.  Select **Revert to this version**.

    **Note:** A confirmation dialog is displayed before the revert is applied.

4.  Select **OK**.

    The roadmap lanes and items are replaced with the values from the selected version. The version label in the roadmap header and the version history is updated to reflect the restored version.


## Result

The roadmap reflects the lane and item configuration from the selected version. The roadmap state \(Draft or Published\) is not changed when you revert a version.

**Parent Topic:**[View a product adoption roadmap](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-view-par-roadmap.md)

**Related topics**  


[Product adoption roadmap versioning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-par-versioning.md)

[View a product adoption roadmap](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-view-par-roadmap.md)

[Product adoption roadmap](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-par-roadmap.md)

