---
title: Template versioning
description: Template versioning enables organizations to maintain multiple versions of assessment templates over time. The ongoing assessments continue to exist even if a their related version is retired or superseded by new versions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/template-versioning.html
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Template versioning

Template versioning enables organizations to maintain multiple versions of assessment templates over time. The ongoing assessments continue to exist even if a their related version is retired or superseded by new versions.

## Template versioning overview

As organizational requirements evolve, assessment templates must be updated to reflect new conformance standards, improved question sets, or refined evaluation criteria. Template Versioning provides a structured approach to managing these changes while maintaining control over assessments that are already in progress.

When a template manager publishes a new version of an existing template, the system automatically retires the previous version. This promotes a clear version lineage and prevents confusion about which template version should be used for new assessments. Template versioning introduces lifecycle management for assessment templates.

Before template versioning, updating a published template required copying it, modifying the copy, and updating every trigger move to use the new copy. This approach broke continuity. Copy responses from previous assessments did not carry over, because the new template was technically a different template. Reporting was also impacted, and the historical evolution of the template was not preserved. Template versioning solves these problems by treating each version as part of the same template lineage. Trigger points, copy responses, and reporting continue to work without reconfiguration.

From the template builder, the current version is shown in a version bar at the top of the template. The version bar displays the version number, lets you open the full version history.

## Template version lifecycle

A template version moves through the following states:

-   **Draft**

    The version is open for editing. You can modify question text, question type, option sets, sections, instructions, and the rest of the template structure. Assessments can't be triggered from a draft version. Post-assessment actions can't be configured or published while a version is in draft state. You can also delete a draft version using the **Delete template** action. This action is available only while the version is in the draft state; published and retired versions can't be deleted.

-   **Published**

    The version is active and is used as the source for all new assessments triggered from this template. Direct editing of the published template is restricted; to change a published template, either use Quick edit for minor corrections \(see [Quick edit for published templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/quick-edit-for-published-templates.md)\) or create version.

-   **Retired**

    The version is no longer used as the source for new assessments. When a new version is published, the previously published version is retired automatically. Assessments that were already triggered from the retired version continue to use the version they started with.


You can create version from a published or retired version that already has at least one assessment triggered from it. You can't create version from a draft version and from a published template that has no assessments yet. If a template is published but has no assessments, you can edit the published template directly until the first assessment is triggered.

## What happens when a version is published

When you publish a new version of a template, the system applies the following behavior automatically:

-   The previously published version is moved to the Retired state.
-   Assessments that have already been triggered from the previous version continue to use the version they were triggered from. They aren't migrated to the new version.
-   New assessments triggered after the publish use the newly published version.
-   Trigger points configured against the template continue to work without any change.

## Impact on copy response and reporting

Copy response and reporting both rely on matching a question across template versions. A structural comparison determines whether two questions represent the same logical question.

-   If a question's type and label are unchanged in the new version, the question is treated as the same question across versions. Responses copied from a previous assessment are placed against this question in the new assessment, and reports continue to aggregate responses across versions.
-   If a question's type or label has changed in the new version, the question is treated as a different question. Responses for the modified question aren't copied across versions, and the question is reported as a separate question across the lifetime of the template.

For example, consider a template with five questions where only question 3 is structurally modified. Questions 1, 2, 4, and 5 receive copied responses and are reported as the same question. Question 3 is treated as a new question starting from the new version.

## Impact on post-assessment actions

Post-assessment actions from the previously published version are carried forward, but remain in draft state until you re-publish them.

-   When you create version, all post-assessment actions from the previous version are copied to the new version and set to **Draft**.
-   While the new template version is in draft state, you can't configure or publish post-assessment actions. Post-assessment actions can only be configured on a published template.
-   After you publish the new template version, review the carried-over post-assessment actions, update any actions that depend on questions you modified, and publish them.

This protects against publishing actions that reference questions you may have changed in the new version. For more information about post-assessment actions, see [Configure post-assessment actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/configure-post-assessment-actions.md).

## Benefits of template versioning

Template versioning in Smart Assessment Engine provides the following benefits:

-   Organizations can evolve assessment templates to meet changing requirements without disrupting ongoing assessment programs.
-   Completed assessments remain unchanged, maintaining a permanent record of which template version was used for each assessment.
-   The system maintains complete version lineage, supporting conformance auditing and historical analysis.
-   Reduces manual tracking of which assessments must be restarted or updated after template changes.
-   Automated policy execution eliminates the need for administrators to manually review and update assessments after template changes.
-   Trigger points continue to work after publishing a new version, eliminating the must manually update flows, scripts, or related lists that reference the template.
-   Copy response from previous assessments continues to work for questions that have not been structurally changed across versions.
-   Reports continue to aggregate responses across versions for unchanged questions, preserving longitudinal reporting.
-   Supports templates maintained in multiple languages, so internationalized templates can be versioned without losing translated content.

**Related topics**  


[KB3013746](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3013746)

