---
title: Generate a risk assessment summary
description: Generate a risk assessment summary that is based on your inherent risks, residual risks, target risks, and control effectiveness data by using the Now Assist for IRM application. Your approvers get the key insights to understand the context quickly, and you reduce the time involved in creating summaries manually.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use generative AI skills, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Generate a risk assessment summary

Generate a risk assessment summary that is based on your inherent risks, residual risks, target risks, and control effectiveness data by using the Now Assist for IRM application. Your approvers get the key insights to understand the context quickly, and you reduce the time involved in creating summaries manually.

## Before you begin

Install the Now Assist for IRM application to generate a risk assessment summary. For more information, see [Now Assist for Integrated Risk Management \(IRM\)](../../grc-common/concept/now-assist-for-irm.md).

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

Role required: The sn\_grc\_sharegenai.risk\_asmt\_user role must be assigned manually to the assessor \(sn\_risk\_advanced.ara\_assessor\) and approver \(sn\_risk\_advanced.ara\_approver\) roles to generate the risk assessment summary.

## About this task

Assessor can generate the risk assessment summary and save the summary in the **Risk assessment summary field** only when they are submitting the assessment. After submission, both assessors and approvers can generate the summary and share it in the work notes. You can also summarize the assessment for object based assessments.

**Note:** This feature is available only on the Risk Workspace.

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Workspace** &gt; **My tasks**.

2.  Open the risk assessment that you want to create the risk assessment summary for.

3.  Generate a risk assessment summary from the risk assessment landing page by selecting **Summarize**.

    ![Generate risk assessment summary button on the risk assessment landing page.](../../grc-workspace-risk/image/risk-assessment-summary-landing-page-genai.png)

4.  Generate a risk assessment summary while submitting the assessment by selecting the generate summary ![Summarize button on the risk assessment landing page.](../../grc-workspace-risk/image/risk-assessment-summarization-icon.png) icon.

    ![Generate risk assessment summary button on the submit an assessment dialog box.](../../grc-workspace-risk/image/risk-assessment-summary-submit-assessment-genai.png)

    A summary is generated; you can edit it and save it for reference and reporting purposes. After submission of the risk assessment, the **Assessment summary** field becomes read only.


