---
title: Create a template version
description: Create a new template version when you must update the questions, instructions, or structure of a published template without disrupting assessments that are already in progress. Existing assessments continue to use the version they were triggered from, and new assessments triggered after you publish the new version use the new template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/create-a-new-template-version.html
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Template versioning, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Create a template version

Create a new template version when you must update the questions, instructions, or structure of a published template without disrupting assessments that are already in progress. Existing assessments continue to use the version they were triggered from, and new assessments triggered after you publish the new version use the new template.

## Before you begin

Role required: sn\_smart\_asmt.template\_manager

The template must be in the **Published** or **Retired** state and must have at least one assessment triggered from it. You can't create a new version from a draft template or from a published template that has no assessments yet.

## About this task

Trigger points configured against the template don't require updates. For an overview of how versioning interacts with copy response, reporting, and post-assessment actions, see [Template versioning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/template-versioning.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Assessment Workspace**.

2.  Open the template that you want to update.

    The template builder displays a version bar at the top of the template, showing the current version number and the actions available for the current state.

3.  To create a new version, select **Options** icon \[Omitted image "ellipsis-vertical-outline-24.svg"\]&gt; **Create new version**.

    **Note:** You can also create a new version from an earlier version of the same template by opening that version from the version history and selecting **Create new version**.

4.  Review the confirmation message, then select **Create**.

    The system creates a new version in **Draft** state. The version history records the new version number, the user who created it, the timestamp, and the source version from which it was created. While the new version is in draft, the previously published version continues to be the source for newly triggered assessments.

5.  Edit the new version as needed.

    You can change any element that is editable on a draft template, including question text, question type, option sets, sections, and instructions. For details on populating a template, see [Add instructions and questions to an assessment template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-populate.md).

6.  Review the post-assessment actions that were carried over from the previous version.

    When you create a new version, all post-assessment actions from the previous version are copied to the new version and set to **Draft**. You can't configure or publish post-assessment actions while the template is in draft state. Make a note of any actions that depend on questions you modified so that you can update them after publishing the new version.

7.  When you have finished editing, publish the new version.

    On publish, the system moves the previously published version to the **Retired** state and uses the new version as the source for all subsequent assessments. Assessments that were already triggered from the previous version continue to use that version. For more information on this policy, see [Template versioning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/template-versioning.md).


## What to do next

After you publish the new version, open the carried-over post-assessment actions, update any actions that depend on questions you modified in the new version, and publish them. For information about configuring post-assessment actions, see [Configure post-assessment actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/configure-post-assessment-actions.md).

