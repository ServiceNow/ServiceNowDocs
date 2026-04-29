---
title: Activate or update Smart Assessment templates
description: Manage SAE templates for TPRM from the Unified Content Management page in the Vendor Management Workspace. You can view available templates, select template versions, activate or update templates for use in Third-party Risk Management assessments, and update templates when newer versions are released.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing TPRM SAE templates with Unified Content Management, Smart Assessment Engine assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Activate or update Smart Assessment templates

Manage SAE templates for TPRM from the Unified Content Management page in the Vendor Management Workspace. You can view available templates, select template versions, activate or update templates for use in Third-party Risk Management assessments, and update templates when newer versions are released.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager

You must have the Unified Content Management application installed and you must set the Smart Assessment Engine enabled \[sn\_vdr\_risk\_asmt.sae\_enabled\] property. After setting this property, SAE becomes the default assessment engine and replaces the legacy experience.

**Warning:** After this option is enabled, this selection can’t be reversed.

For more information, see [Configure TPRM properties](../../grc-vendor-risk-implementation/task/tprm-properties-configure.md), [Migrating from Classic Assessment Engine to Smart Assessment Engine](../concept/tprm-migrate-asmnt-sae.md), and [Managing TPRM SAE templates with Unified Content Management](../concept/tprm-integrating-ucm.md).

## About this task

Use Unified Content Management to control which TPRM SAE templates are available for use in new Third-party Risk Management assessments. Activating a template version makes it available when creating new assessments. Updating a template applies a newer released version for future assessments.

## Procedure

1.  Navigate to **Workspaces** &gt; **Vendor Management Workspace**, and on the **Risk** tab, select the Unified Content Management icon ![](../image/unified-content-mgmt-icon.png).

2.  View templates by state by selecting **Active** or **Inactive**.

    Inactive templates are not available for new assessments until a year is selected and activated.

3.  Select the year from the dropdown menu for the template you want to activate or update.

4.  Choose the action you want to perform.

    |Action|Description|
    |------|-----------|
    |**Activate a template version**|Make the selected year of the inactive template available for use by selecting **Activate**.|
    |**Update a template version**|Apply the selected year of the template as the active version by selecting **Update**.|

    1.  Review the disclaimer, then select **Agree**.

    2.  Review all sections of the template and, after confirming they meet your requirements, select **Submit**.


## Result

If you activated the template, the selected year is available for use when creating new TPRM assessments. If you updated the template, the selected year is applied as the active version used for future assessments.

## What to do next

Review related assessments and configuration to help ensure that the appropriate template versions are in use.

To modify template content, contact a team member with the TPR admin \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\] role. TPR admins can edit templates by navigating to **Workspaces** &gt; **Assessment Workspace**, selecting the template you want to edit, and then selecting **Edit**.

**Note:**

You can create an assessment only from a published assessment template. You can update a published template only if no active assessment is associated with it. You can also copy an existing template, including all questions, sections, instructions, and configurations. For more information, see [Copy an assessment template](../../assessment-engine/task/sae-asmnt-template-duplicate.md).

