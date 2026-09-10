---
title: Create condition templates for condition attributes
description: Create a condition template and associate the template to condition attributes for enterprise models and assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/create-condition-template-eam.html
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Asset conditions, Create and manage enterprise assets, Managing enterprise models and assets, Enterprise Asset Management, Asset Management]
---

# Create condition templates for condition attributes

Create a condition template and associate the template to condition attributes for enterprise models and assets.

## Before you begin

Role required: Asset technician \(sn\_smart\_asmt.actor\) and Asset manager \(sn\_smart\_asmt.template\_manager\).

## About this task

Create condition templates before defining condition attributes on enterprise models and assets.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace**.

2.  From the Enterprise Asset Workspace, navigate to one of the following views:

    -   Admin center view
    -   Enterprise asset estate view
    -   Enterprise model management view
3.  Depending on the view you are in, perform the following steps:

    -   Admin center view: In the navigation panel of the Admin center view, navigate to **Asset condition configuration** &gt; **Asset condition templates** and then select **New**.
    -   Enterprise asset estate or Enterprise model management view: Select the **All enterprise** tab or the tab for a specific model or asset category, such as Construction. Open an enterprise model or asset, select the **Condition attributes** tab, select **New**, and then select **Create assessment template**.
4.  In the Create new assessment template dialog box, enter a name for the template.

5.  Select **Create**.

    The fields in the **General** tab are automatically populated.

    The template opens in the Assessment Workspace that belongs to the Governance, Risk, and Compliance application.

    The fields in the **General** tab are automatically populated.

6.  Select the **Scoring** tab to add scores to the overall template.

    Scoring helps to evaluate the condition of assets and indicates whether the condition evaluation passed or failed. Scoring can be also added for each section in the **Questions** tab and also for each question.

7.  Select **Enable scoring**

    You must enable scoring to make results available for the condition attributes. For more details on scoring, see [Create Smart Assessment templates for BIA](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/conf-impact-asmt-template.md).

8.  After entering the details in the **Scoring** tab, select **Save**.

9.  Select the **Questions** tab to create sections and questions.

    You can create sections and questions in this tab and enable scoring for any specific section and for individual questions. For more details on creating questions, sections, and scoring, see [Create Smart Assessment templates for BIA](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/conf-impact-asmt-template.md).

10. After entering all the details in the **Questions** tab, select **Save**.

11. Select **Publish**

    The questions and scores are published. Publishing finalizes the template and makes the template ready to be used for evaluation.

    If you don’t publish the template, the template won’t be available in the condition template picker when creating condition attributes.


**Parent Topic:**[Asset conditions in Enterprise Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/asset-conditions-eam.md)

**Related topics**  


[Define condition attributes on enterprise models and assets]()

