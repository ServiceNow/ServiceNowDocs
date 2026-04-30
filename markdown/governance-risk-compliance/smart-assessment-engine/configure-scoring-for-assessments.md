---
title: Configure scoring for an assessment
description: Set up scoring for your assessment responses to calculate meaningful scores at the assessment, section, or subsection level.
locale: en-US
release: yokohama
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Scoring assessments, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Configure scoring for an assessment

Set up scoring for your assessment responses to calculate meaningful scores at the assessment, section, or subsection level.

## Before you begin

-   Confirm that the smart assessment scoring plugin \[com.sn\_smart\_scoring\] is installed.
-   Role required: sn\_smart\_asmt.template\_manager or sn\_smart\_asmt.assessment\_admin

## About this task

Configure scoring for assessment 

-   Scoring can be configured at the assessment, section, subsection, and question levels. Configuring scoring at each level is optional, enable it at one or more levels based on your needs. Scoring levels are dependent on each other. For example, assessment scoring depends on section scores, which depend on subsection and question scores.
-   Scoring can only be configured on a draft template. Once the template is published, you can no longer configure scoring for it.
-   If questions are skipped and not answered, they’re excluded from the score calculation.

## Procedure

1.  Navigate to **Workspaces** &gt; **Assessment Workspace** to access the assessment workspace landing page.

2.  Create an assessment or open an existing assessment template, which is in a draft state to configure scoring.

3.  Select the **Scoring** tab.

4.  Under **Scoring settings**, select the **Enable scoring for this template** option.

    -   The **Enable scoring for this template** option enables you to apply scoring at the assessment, section, subsection, and question levels.
    -   Once scoring is enabled, you can enable normalization and configure its default settings. For more information, refer to [Configure normalization in assessment](configure-normalization-in-assessment.md)
5.  To activate scoring at assessment level, select the **Assessment score** option.

    1.  On the **Assessment scoring** form, fill in the fields.

        For a description of the field values, see [Assessment scoring form](../reference/scoring-forms.md#section_xfs_1bk_k3c).

    2.  Select **Save**.

6.  To configure scoring at the question level, select the **Questions** tab.

    1.  Turn on the toggle for the question for which you want to configure scoring.

    2.  On the **Question scoring** form, fill in the fields.

        For a description of the field values, see [Question scoring form](../reference/scoring-forms.md#section_tpx_3bk_k3c).

        **Note:** Scoring logic varies by question type.

        -   For multi-select, you can assign scores to options, apply functions, and set question weights.
        -   For radio options, you can assign scores to choices and set question weights.
        -   For number-type questions, the assessor's numeric response is directly used as the score.
    3.  Select **Save**.

7.  To configure scoring at the **Subsection** level, turn on the toggle switch on the subsection for which you want to configure scoring.

    1.  On the **Subsection scoring** form, fill in the fields.

        For a description of the field values, see [Assessment scoring form](../reference/scoring-forms.md#section_xfs_1bk_k3c)

        **Note:** The subsection scores are calculated by grouping question scores based on the defined criteria.

    2.  Select **Save**.

8.  To configure scoring at the **Section** level, turn on the toggle switch on the section for which you want to configure scoring.

    ![Scoring section.](../image/scoring-section.jpg)

    1.  On the **Section scoring** form, fill in the fields.

        For a description of the field values, see [Section scoring form](../reference/scoring-forms.md#section_xbl_4bk_k3c)

    2.  Select **Save**.


## Result

The scoring is now configured at all required levels.

