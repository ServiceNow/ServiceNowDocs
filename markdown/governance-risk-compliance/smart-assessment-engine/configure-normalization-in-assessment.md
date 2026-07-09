---
title: Configure normalization in assessment
description: In Smart Assessment Engine, set up normalization to adjust assessment response scores to a common scale at the assessment, section, or subsection level.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/configure-normalization-in-assessment.html
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Normalization in assessment, Scoring assessments, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Configure normalization in assessment

In Smart Assessment Engine, set up normalization to adjust assessment response scores to a common scale at the assessment, section, or subsection level.

## Before you begin

-   Confirm that the smart assessment scoring plugin \[com.sn\_smart\_scoring\] is installed.
-   Role required: sn\_smart\_asmt.template\_manager and sn\_smart\_asmt.assessment\_admin

## About this task

-   To configure normalization, first set up scoring. For more information, see [Configure scoring for an assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/configure-scoring-for-assessments.md).
-   Normalization is supported for questions with number, drop-down, radio button, and check box types.

## Procedure

1.  Navigate to **Workspaces** &gt; **Assessment Workspace** to access the assessment workspace landing page.

2.  Create or open a draft assessment template in which you want to configure normalization.

    |Option|Description|
    |------|-----------|
    |**New template**|Select **New template** on the Assessment Workspace landing page and fill in the template details. The new template opens in **Draft** state.|
    |**Existing template**|Select an existing template from the Assessment Workspace landing page. The template must be in the **Draft** state to edit scoring or normalization settings.|

3.  Select the **Scoring** tab.

4.  Select the **Enable normalization for this template** option.

    -   To enable normalization on a template, normalization and its defaults must be enabled in the purpose assigned to that template. For more information, see [Create an assessment template category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-category-create.md).
    -   The **Enable normalization for this template** option enables you to apply normalization rules at the section, subsection, and question levels.
5.  To define default normalization values to be applied at section, subsection, and question levels automatically, select **Define default normalization to apply at different levels automatically** option and on the form, fill in the fields.

    **Note:** The following input fields are specific to the default Linear normalization strategy. The fields may differ when using alternative normalization strategies.

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

6.  If the **Assessment score** option is selected, to use aggregate score at the assessment level, select **Use normalized score for aggregation**.

    1.  To edit the normalization values for the assessment score, select edit \[Omitted image "edit-normalization.png"\] Alt text: icon and update normalization values.

    2.  To delete the normalization values for the assessment score, select delete \[Omitted image "delete-normalization.png"\] Alt text: icon and select **Remove normalization**.

7.  Select **Save**.

8.  Select the **Questions** tab.

9.  To customize normalization values, select the specific section, subsection, or question you want to update.

    1.  To edit the normalization values for the assessment score, select edit \[Omitted image "edit-normalization.png"\] Alt text: icon and update normalization values.

    2.  To delete the normalization values for the assessment score, select delete \[Omitted image "delete-normalization.png"\] Alt text: icon and select **Remove normalization**.

    Default normalization is automatically applied at multiple levels sections, subsections, and individual questions.

10. Select **Save**.


## Result

Normalization is configured for the assessment template and applied at the specified levels.

