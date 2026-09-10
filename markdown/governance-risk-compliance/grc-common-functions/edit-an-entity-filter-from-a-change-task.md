---
title: Edit an entity filter from a change task
description: Modify an entity filter condition and preview the revised impact before saving the filter and accepting the entity changes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/grc-common-functions/edit-an-entity-filter-from-a-change-task.html
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-09-02"
reading_time_minutes: 1
breadcrumb: [Entity lifecycle management, Common GRC features, Governance, Risk, and Compliance]
---

# Edit an entity filter from a change task

Modify an entity filter condition and preview the revised impact before saving the filter and accepting the entity changes.

## Before you begin

-   A change task must be available on the **Needs review** tab. See [Review and accept entity changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-common-functions/review-and-accept-entity-changes.md).
-   Role required: sn\_grc\_change\_mgmt.implementer

## About this task

If the impact shown in a change task is not expected, modify the associated entity filter condition and preview the resulting entity changes.

## Procedure

1.  From the change task, select **Edit filter**.

2.  Modify the **Filter condition**.

    The matching-record count updates based on the filter condition.

3.  Select **Preview changes**.

4.  Review the **Summary of changes** and the impacted records.

5.  Decide how to proceed.

    -   To modify the filter condition again, select **Back**.
    -   To save the filter and accept the resulting entity changes, select **Save filter and accept changes**.
6.  In the confirmation dialog, select **Confirm**.

    **Warning:**

    This action can't be undone. The changes are applied to the entity and all downstream records.


## Result

If you select **Save filter and accept changes**, the system saves the modified filter condition and applies the resulting entity changes and their downstream impacts. The change task then moves to the **Closed** state. The completed change task appears on the **History** tab.

**Parent Topic:**[Entity lifecycle management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-common-functions/entity-change-management.md)

