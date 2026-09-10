---
title: AI reviewer assist for risk assessments
description: AI Risk and Compliance analysts reviewing assessments can review AI-assisted recommendations and assign relevant control objectives and risk statements from the compliance library. Accepted recommendations are scoped automatically to the AI Asset.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/ai-based-reviewer-assistant-for-assessments.html
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-08-26"
reading_time_minutes: 4
breadcrumb: [Exploring Now Assist in AI Risk and Compliance, Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# AI reviewer assist for risk assessments

AI Risk and Compliance analysts reviewing assessments can review AI-assisted recommendations and assign relevant control objectives and risk statements from the compliance library. Accepted recommendations are scoped automatically to the AI Asset.

## Overview of AI recommendations in risk assessments

Control objectives and risk statements can be mapped to assessment responses through automation rules configured directly in smart assessment templates. However, these rules are tied to specific templates and control objectives shipped with the product. This translates to manual effort for organizations using custom templates, custom questionnaires, or their own authority documents as the configuration have to be mapped manually.

AI-assisted recommendations spare this effort. When an assessment task moves to the Review state, a reviewer can trigger the recommendation skills to analyze the completed assessment responses and the associated processing activity. The skills identify relevant control objectives and risk statements from the compliance library that the reviewer can either accept or dismiss.

When a reviewer accepts a recommendation, the control objective or risk statement is added to the **Applicable scope** tab on the assessment task. After the reviewer closes the assessment task, the corresponding controls and risks for the items in **Applicable scope** are automatically scoped to the AI Asset.

## Key benefits

AI-assisted recommendations provide the following benefits:

-   Reduces manual effort by automatically identifying relevant control objectives and risk statements from the compliance library based on assessment responses.
-   Supports assessments built on smart assessment templates, including custom templates and questionnaires, without requiring preconfigured automation rules.
-   Provides an AI suggestion guide for each recommendation that explains why the item was recommended, citing the specific assessment response or record detail that triggered it.

## How recommendations are generated

The following skills discover the relevant risk-controls for further governance evaluation:

-   **Control Objective Recommender**

    Surfaces matching control objectives from the compliance policy statement library \(sn\_compliance\_policy\_statement\).

-   **Risk Statement Recommender**

    Surfaces matching risk statements from the risk definition library \(sn\_risk\_definition\).


Each skill retrieves candidate records from an existing compliance library using retrieval-augmented generation \(RAG\), then uses a language model to reason over the retrieved candidates and finalize a de-duplicated list.

**Note:** A control objective or risk statement that's already in scope through manual addition or automation rules, isn't recommended.

The RAG approach matches assessment content against the compliance library. Here's how the skills generate recommendations.

1.  Context is gathered from the following sources:

    -   Processing activity details, such as name and description.
    -   Completed smart assessment responses, including information objects, data subject types and hierarchy.
    -   AI Asset, AI Asset Task, and AI Assessment Response.
    **Note:** Excluded from the context are attachments, commentary notes, and AI Asset relationships

2.  Based on context, short retrieval texts are generated that represent distinct risk obligations.
3.  Each retrieval text is used to query the compliance library for semantically similar control objectives or risk statements.
4.  The retrieved candidates are evaluated, and the most relevant items are selected and displayed in the **Recommendations** tab of a risk assessment task.

## Role requirements to generate recommendations

<table id="table_tc3_443_jkc"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1.  sn\_airc\_gen\_ai.airc\_ai\_agent\_user
2.  sn\_airc\_gen\_ai.airc\_ai\_user

</td><td>

Enables risk and compliance analysts to generate AI recommendations and view them in the **Recommendations** tab.

</td></tr><tr><td>

sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst

</td><td>

Enables risk and compliance analysts to access the assigned risk assessment task from the [AI Risk and Compliance workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/ai-risk-and-compliance-workspace.md), and accept, dismiss, or revert AI recommendations on the assessment.

</td></tr></tbody>
</table>## Recommendations tab in the Assessment Task record

On the Overview tab of a Assessment Task in the Review state, a banner prompts the reviewer to generate recommendations. Selecting **Recommend** opens the Recommendations tab, which lists the recommended records on separate Control objectives and Risk Statements tabs. For details about what each recommendation card displays

If there’s no relevant data available, the recommendations page indicates that the request was completed and there are no recommendations currently available. If the request is in progress, try reloading the page after some time.

Each recommendation card in the New state displays the option to accept and dismiss it. After a reviewer accepts or dismisses a recommendation, the card displays the state as Accepted or Dismissed and offers a **Revert** option to reset the state. Accepted recommendations automatically reflect in the Applicable scope tab on the assessment task record.

For details about what each recommendation card displays, see.

## Applicable scope tab in a risk assessment task

The Applicable scope tab lists all the records that apply to the processing activity. Items in this tab originate from three sources, identified by the Mode column.

|Mode|Description|
|----|-----------|
|**Automation**|Items added by smart assessment automation rules configured in the assessment template.|
|**AI-assisted**|Items accepted from the **Recommendations** tab.|
|**Manual**|Items added manually by the privacy analyst during review.|

Reviewers can add and remove items from Applicable scope regardless of how they originated, including items from automation rules or accepted AI recommendations.

