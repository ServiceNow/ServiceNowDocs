---
title: Review and accept entity changes
description: Review the impact of proposed entity changes and accept the changes when the impact is expected.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/review-and-accept-entity-changes.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-02"
reading_time_minutes: 1
breadcrumb: [Entity lifecycle management, Common GRC features, Governance, Risk, and Compliance]
---

# Review and accept entity changes

Review the impact of proposed entity changes and accept the changes when the impact is expected.

## Before you begin

-   Entity approvals must be configured for the applicable change type. See [Configure entity approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/configure-entity-approvals.md).
-   Role required: sn\_grc\_change\_mgmt.implementer

## About this task

When an entity filter or source record change meets the configured approval condition, the system creates a change task. Open change tasks appear on the **Needs review** tab of the **Impact approvals** page. The change task shows impacted entities and their associated risks and controls.

## Procedure

1.  Navigate to **All** &gt; **Entity management** &gt; **Impact approvals**.

2.  On the **Needs review** tab, open the change task that you want to review.

3.  Review the **Summary of changes**.

    The summary shows the number of impacted entities, risks, and controls.

4.  Review the impacted entities and their downstream impacts.

    1.  View an entity's associated risks and controls by selecting the entity.

    2.  View the records associated with a downstream impact by selecting a value in the **Downstream impacts** column.

    3.  Refine the displayed records using the available filter and sort options.

    4.  Export the impact information by selecting **Export to Excel**.

5.  If the impact information does not reflect the latest entity filter or source record changes, select **Fetch latest changes**.

    The system recalculates the impact and updates the summary, impacted records, and last-refreshed information.

6.  Select **Accept changes**.

7.  In the **Accept changes** dialog, select **Confirm**.

    **Warning:**

    This action can't be undone. The changes are applied to the entity and all downstream records.


## Result

The system applies the accepted changes and moves the change task to the **Closed** state. The completed change task appears on the **History** tab, where you can review the summary and impacted records.

**Parent Topic:**[Entity lifecycle management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/entity-change-management.md)

