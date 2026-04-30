---
title: Create a TPRM SAE questionnaire or document request template
description: Create a TPRM SAE questionnaire or document request template that supports SAE for risk identification. After integrating SAE, new users must create SAE templates, and existing users can create additional templates after migrating their existing ones.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Smart Assessment Engine assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Create a TPRM SAE questionnaire or document request template

Create a TPRM SAE questionnaire or document request template that supports SAE for risk identification. After integrating SAE, new users must create SAE templates, and existing users can create additional templates after migrating their existing ones.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_admin

You must set the Smart Assessment Engine enabled \[sn\_vdr\_risk\_asmt.sae\_enabled\] property. After setting this property, SAE becomes the default assessment engine and replaces the legacy experience.

**Warning:** After this option is enabled, this selection can’t be reversed.

For more information, see [Configure TPRM properties](../../grc-vendor-risk-implementation/task/tprm-properties-configure.md) and [Migrating from Classic Assessment Engine to Smart Assessment Engine](../concept/tprm-migrate-asmnt-sae.md).

## About this task

To add Third-party Risk Management \(TPRM\) specific information such as third-party risk areas, the include previous responses option, and enable scoring option to your questionnaire template, you must create a template using the Vendor Management Workspace. After saving the questionnaire, the questionnaire template opens in the Assessment Workspace where you can make edits using the Smart Assessment template designer.

**Important:** You must publish your questionnaire template after completing all of your customizations and review for it to be available for use in the Vendor Management Workspace. TPR admins can edit the questionnaire and republish it with changes. However, editing templates that have already been sent out is not recommended, as this can disrupt scoring for questionnaires completed using the previous version.

## Procedure

1.  Navigate to **Workspaces** &gt; **Vendor Management Workspace**, select the list icon ![](../../grc-workspace-vrm/image/ws-list-icon.png) and then navigate to **Assessment setup** &gt; **Questionnaire templates**.

2.  Complete one of the following options to create a new template or copy an existing template and customize.

<table id="choicetable_ctx_vmr_g2c"><thead><tr><th align="left" id="d90298e169">

Option

</th><th align="left" id="d90298e172">

Description

</th></tr></thead><tbody><tr><td id="d90298e178">

**Create a new template**

</td><td>

1.  Select **New**.
2.  On the **Create New TPRM questionnaire template form**, fill in the fields.

For more information about the field descriptions, see [Create New TPRM SAE questionnaire template form](../reference/create-sae-q-template-form.md).

3.  Select Save.
 **Note:** For Issue-generation rules to work as expected when applied to an SAE assessment template, at least one question with Enable preferred response must be set to true.

</td></tr><tr><td id="d90298e232">

**Copy and customize an existing template**

</td><td>

Select the copy icon ![](../../assessment-engine/image/copy-icon.png) and make any necessary updates.

</td></tr></tbody>
</table>
## What to do next

-   If you chose to create a new template the system generates an empty template. Navigate to each corresponding tab to define the overall instructions, questions, optional guidance for responding to a question, sections that group the related questions, and scoring. For more information, see [Add instructions and questions to an assessment template](../../assessment-engine/task/sae-asmnt-template-populate.md), [Add reference information to an assessment template](../../assessment-engine/task/sae-asmnt-add-reference.md), [Configure scoring for an assessment](../../assessment-engine/task/configure-scoring-for-assessments.md), and [Normalization in assessment](../../assessment-engine/concept/normalization-in-assessment.md).
-   If you chose to copy an existing template, the system generates a template including all questions, sections, instructions, and configurations of the existing template. You can now customize it as necessary.

**Note:** Not all question types are supported. Percentage, ranking, image scale, and custom metric aren’t supported. For the percentage and image scale question types, customers can use the Number type and Radio button type, respectively. Ranking and custom metric question types aren't supported. You must either convert these question types to supported formats before migration or create questions in the template designer after migration.

**Related topics**  


[Using the template designer](../../assessment-engine/concept/sae-template-designer.md)

