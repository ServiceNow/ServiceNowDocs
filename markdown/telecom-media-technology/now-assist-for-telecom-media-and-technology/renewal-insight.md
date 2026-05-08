---
title: Renewal insight engine skill
description: Analyzes the renewal likelihood and expansion potential of an engagement or contract and generates recommended actions.
locale: en-US
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Renewal insight engine skill

Analyzes the renewal likelihood and expansion potential of an engagement or contract and generates recommended actions.

## Before you begin

Role required: sn\_acct\_lc.customer\_success\_agent

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see Now Assist skills, agents, and agentic workflows on by default.

## About this task

The Renewal insight engine skill evaluates individual product metrics, health metrics, health score trends, usage trends, and value scores to generate renewal assessments. The skill provides a granular analysis by evaluating data at the product level rather than using aggregated scores. The skill is automatically triggered by the [Now Assist for Telecommunications, Media and Technology \(TMT\) Support renewals and expansion](../concept/now-assist-tmt-renewal-analyzer.md) workflow and runs in two modes:

-   Engagement mode: Analyzes all products and health metrics for the overall engagement and generates the renewal likelihood, expansion potential, and up to three recommended actions for the engagement.
-   Contract mode: Analyzes contract-specific products while also considering the overall engagement health and non-contract products, and generates the renewal likelihood, expansion potential, and up to three recommended actions for the contract.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Now Assist Skills**.

2.  Select **Activate** in the Renewal Insight Engine card.

3.  Select the user role that can use this skill and select **Save** to activate the skill.

    The Renewal Insight Engine skill is automatically triggered when the [Now Assist for Telecommunications, Media and Technology \(TMT\) Support renewals and expansion](../concept/now-assist-tmt-renewal-analyzer.md) agentic workflow runs. When the workflow is completed, the following output is generated:

    -   Renewal likelihood: The predicted renewal likelihood including an assessment such as Very High, High, Moderate Risk, At Risk, or Critical Risk, and the key factors that influenced the assessment.
    -   Expansion potential: The potential for account expansion including an assessment of Strong, Moderate, or Limited, the probability, and the target products identified for expansion.
    -   Recommended actions: Up to three recommended actions in the form of internal plays or customer plays, each specifying the action, play type, target product, priority, and reasoning. The renewal assessment report is automatically added to the work notes of the generated internal play records.
    ![Renewal analysis workflow-1](../image/renew-analysis-1.jpg)

    ![Renewal analysis workflow - 2](../image/renewal-analysis-2.jpg)


**Parent Topic:**[Using Now Assist for Telecommunications, Media and Technology \(TMT\)](../concept/now-assist-spm-using.md)

