---
title: Create condition templates for condition attributes
description: Create a condition template and associate the template to condition attributes for enterprise models and assets.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-03-28"
reading_time_minutes: 2
breadcrumb: [Create and manage enterprise assets, Managing enterprise assets and models, Enterprise Asset Management, IT Asset Management]
---

# Create condition templates for condition attributes

Create a condition template and associate the template to condition attributes for enterprise models and assets.

## Before you begin

Role required: Asset technician \(sn\_smart\_asmt.actor\) and Asset manager \(sn\_smart\_asmt.template\_manager\)

## About this task

Create condition templates before defining condition attributes on enterprise models and assets.

## Procedure

1.  From the Enterprise Asset Workspace, navigate to either of the views:

    -   Admin center
    -   Enterprise asset estate
    -   Enterprise model management
2.  Depending on the view you are in, do one of the following:

    -   Admin center: Select **New** in the Asset condition templates page.
    -   Enterprise asset estate or Enterprise model management: Select the **All enterprise** tab or the tab for a specific model or asset category, such as Construction. Open an enterprise model or asset, select the Condition attributes related list, select **New**, and then select **Create condition template**.
3.  In the **Create new condition template** dialog box, enter a name for the template.

4.  Select **Create**.

    The fields in the **General** tab are automatically populated.

    The template opens in the Assessment Workspace that belongs to the Governance, Risk, and Compliance application.

    The fields in the **General** tab are automatically populated.

5.  Select the **Scoring** tab to add scores to the overall template.

    Scoring helps to evaluate the condition of assets and indicates whether the condition evaluation passed or failed. Scoring can be also added for each section in the **Questions** tab and also for each question.

6.  Select **Enable scoring**

    You must enable scoring to make results available for the condition attributes. For more details on scoring, see [Create Smart Assessment templates for BIA](https://www.servicenow.com/docs/access?context=conf-impact-asmt-template&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US).

7.  After entering the details in the **Scoring** tab, select **Save**.

8.  Select the **Questions** tab to create sections and questions.

    You can create sections and questions in this tab and enable scoring for any specific section and for individual questions. For more details on creating questions, sections, and scoring, see [Create Smart Assessment templates for BIA](https://www.servicenow.com/docs/access?context=conf-impact-asmt-template&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US).

    **Note:** To use the template in the Mobile Agent® application for Enterprise Asset Management, do not configure any of the following settings in the **Questions** tab:

    -   Option to **Add instructions** to the template.
    -   Option to **Add additional content** to a question, including question descriptions and guidance.
    -   Attribute to **Make conditionally visible**, which makes a question visible only when specified response-based conditions are met.
9.  After entering all the details in the **Questions** tab, select **Save**.

10. Select **Publish**

    The questions and scores are published. Publishing finalizes the template and makes the template ready to be used for evaluation.

    If you don’t publish the template, the template won’t be available in the condition template picker when creating condition attributes.


**Parent Topic:**[Create and manage enterprise assets](../concept/create-manage-enterprise-assets.md)

