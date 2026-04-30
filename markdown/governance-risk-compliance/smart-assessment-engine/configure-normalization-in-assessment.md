---
title: Configure normalization in assessment
description: Set up normalization for your assessment responses to adjust individual scores to a common scale at the assessment, section, or subsection level.
locale: en-US
release: zurich
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Normalization in assessment, Scoring assessments, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Configure normalization in assessment

Set up normalization for your assessment responses to adjust individual scores to a common scale at the assessment, section, or subsection level.

## Before you begin

-   Confirm that the smart assessment scoring plugin \[com.sn\_smart\_scoring\] is installed.
-   Role required: sn\_smart\_asmt.template\_manager and sn\_smart\_asmt.assessment\_admin

## About this task

-   To configure normalization, first set up scoring. For more information, refer to [Configure scoring for an assessment](configure-scoring-for-assessments.md).
-   Normalization is supported for questions with number, drop-down, radio button, and check box types.

## Procedure

1.  Navigate to **Workspaces** &gt; **Assessment Workspace** to access the assessment workspace landing page.

2.  Create an assessment or open an existing assessment template, which is in a draft state to configure normalization.

3.  Select the **Scoring** tab.

4.  Select the **Enable normalization for this template** option.

    -   To enable normalization on a template, normalization and its defaults must be enabled in the purpose assigned to that template. For more information, refer to [Create an assessment template category](sae-asmnt-template-category-create.md).
    -   The **Enable normalization for this template** option enables you to apply normalization rules at the section, subsection, and question levels.
5.  To define default normalization values to be applied at section, subsection, and question levels automatically, select **Define default normalization to apply at different levels automatically** option and on the form, fill in the fields.

    **Note:** The input fields shown below are specific to the default Linear normalization strategy. The fields may differ when using alternative normalization strategies.

    |Field|Description|
    |-----|-----------|
    |Normalization Strategy|The default normalization strategy to be used.|
    |Minimum|The minimum value of the current scale.|
    |Maximum|The maximum value of the current scale.|
    |New scale minimum|The minimum value of the target scale.|
    |New scale maximum|The maximum value of the target scale.|
    |Scale definition|Specifies the scoring direction: 'high' for higher scores being better or 'low' for lower scores being better.|
    |Relative scaling|When enabled the normalized score is calculated relative to the maximum value.|
    |Choose where to apply these defaults|
    |Assessment level|Default normalization values are applied for assessment level scores.|
    |All sections|Default normalization values are applied for all section level scores.|
    |All subsections|Default normalization values are applied for all subsection level scores.|
    |All questions|Default normalization values are applied for all question level scores.|

6.  If the **Assessment score** option is selected, to use aggregate score at the assessment level, you can select **Use normalized score for aggregation**.

    1.  To edit the normalization values for the assessment score, select edit ![](../image/edit-normalization.png) icon and update normalization values.

    2.  To delete the normalization values for the assessment score, select delete ![](../image/delete-normalization.png) icon and select **Remove normalization**.

7.  Select **Save**.

8.  Select the **Questions** tab.

9.  To customize normalization values, select the specific section, subsection, or question you wish to update.

    1.  To edit the normalization values for the assessment score, select edit ![](../image/edit-normalization.png) icon and update normalization values.

    2.  To delete the normalization values for the assessment score, select delete ![](../image/delete-normalization.png) icon and select **Remove normalization**.

    Default normalization is automatically applied at multiple levels sections, subsections, and individual questions.

10. Select **Save**.


