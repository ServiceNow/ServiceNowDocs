---
title: Entity lifecycle management
description: Review entity changes and their impact on associated risks and controls before the changes take effect.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/entity-change-management.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-09-02"
reading_time_minutes: 1
breadcrumb: [Common GRC features, Governance, Risk, and Compliance]
---

# Entity lifecycle management

Review entity changes and their impact on associated risks and controls before the changes take effect.

Entity filters identify the source records used to generate entities. When an entity filter condition or a source record changes, the resulting entities can be new, updated, or retired. Entity lifecycle management enables administrators to review configured types of changes before they take effect.

Administrators can select **Enable impact approvals** and define conditions that determine which change types require review. Supported change types are **New**, **Update**, and **Retire**. Changes that don't meet the configured approval conditions take effect without an entity approval.

When a change meets the configured approval conditions, the system creates a change task. The proposed changes remain pending until the change task is reviewed and accepted.

A change task can be created when an entity filter condition changes, or when a source record change affects the records that meet an entity filter condition.

Open change tasks appear on the **Needs review** tab of the **Impact approvals** page. Each change task summarizes the impacted entities and their associated risks and controls. Reviewers can evaluate the proposed changes and fetch the latest impact information before making a decision.

A reviewer can accept the proposed changes or edit the entity filter condition and preview the revised impact. Saving the edited filter also accepts the changes. After a change task is accepted, the proposed changes take effect and the completed task appears on the **History** tab.

-   **[Configure entity approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/configure-entity-approvals.md)**  
Specify which types of entity changes require review before they take effect.
-   **[Review and accept entity changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/review-and-accept-entity-changes.md)**  
Review the impact of proposed entity changes and accept the changes when the impact is expected.
-   **[Edit an entity filter from a change task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/edit-an-entity-filter-from-a-change-task.md)**  
Modify an entity filter condition and preview the revised impact before saving the filter and accepting the entity changes.

**Parent Topic:**[Common Governance, Risk, and Compliance features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/common-grc-features.md)

