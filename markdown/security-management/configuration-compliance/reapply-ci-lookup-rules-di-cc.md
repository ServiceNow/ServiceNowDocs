---
title: Reapply CI lookup rules on selected discovered items for Configuration Compliance
description: Reapply configuration item \(CI\) lookup rules on selected discovered items from the discovered item list view select actions. The administrator might have to edit or update a lookup rule for multiple reasons. If the lookup rule changes, they can reapply them on the discovered items.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/configuration-compliance/reapply-ci-lookup-rules-di-cc.html
release: zurich
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2026-06-20"
reading_time_minutes: 1
breadcrumb: [Discovery Items, Data Import, Explore, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Reapply CI lookup rules on selected discovered items for Configuration Compliance

Reapply configuration item \(CI\) lookup rules on selected discovered items from the discovered item list view select actions. The administrator might have to edit or update a lookup rule for multiple reasons. If the lookup rule changes, they can reapply them on the discovered items.

## Before you begin

Roles required:

## About this task

If the CI changes after reapplying the CI lookup rules, the discovered items are updated with the new CI and test results. For more information, see [CI changes for discovered items for Configuration Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/configuration-compliance/reapply-discovered-items-ci-changes-cc.md).

## Procedure

1.  Navigate to **All** &gt; **Security operations** &gt; **CMDB** &gt; **Discovered Items**.

2.  Select the required discovered items and click **Action on selected rows**.

    \[Omitted image "reapply-action-di-cc.png"\] Alt text: Reapply CI lookup rules on DIs

3.  Select **Reapply CI lookup rules** from the list.

    The rules are reapplied on these discovered items.

    **Note:**

    Starting with Configuration Compliance v15.1.5, you can skip the reapplication of CI lookup rules on discovered items with the substate ‘CI Decommissioned’ by enabling the system property **sn\_sec\_cmn.skipItemsWithCIDecommissioned**.


