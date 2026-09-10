---
title: AI reviewer assist for privacy assessment tasks
description: Privacy analysts reviewing an assessment can use AI-assisted recommendations to identify relevant control objectives and risk statements from the library. Accepted recommendations are automatically scoped to the processing activity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/ai-reccos-for-pia.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2026-08-24"
reading_time_minutes: 5
keywords: [recommendations, control objectives, risk statements]
breadcrumb: [ServiceNow Otto for Privacy Management, Privacy Management, Governance, Risk, and Compliance]
---

# AI reviewer assist for privacy assessment tasks

Privacy analysts reviewing an assessment can use AI-assisted recommendations to identify relevant control objectives and risk statements from the library. Accepted recommendations are automatically scoped to the processing activity.

## Overview of AI recommendations in privacy assessment tasks

Previously, control objectives and risk statements were mapped to assessment responses through automation rules in smart assessment templates. These rules were tied to the specific templates shipped with the product. Organizations that used custom templates or custom questionnaires had to manually configure these mappings.

AI-assisted recommendations address this limitation. When an assessment task moves to the Review state, the reviewer can select the **Recommend** button on the Overview tab to trigger the AI recommendation skills. These skills analyze the completed assessment responses and the associated processing activity. The skills then identify relevant control objectives and risk statements from the library that the reviewer can either accept or dismiss.

When a reviewer accepts a recommendation, the control objective or risk statement is added to the Applicable scope tab on the assessment task. After the reviewer closes the assessment task, the corresponding controls and risks for the records in applicable scope are automatically scoped to the processing activity.

## Key benefits

AI-assisted recommendations provide the following benefits:

-   Reduces manual effort by automatically identifying relevant control objectives and risk statements from the library based on assessment responses.
-   Supports assessments built on smart assessment templates, including custom templates and questionnaires, without requiring preconfigured automation rules.
-   Provides an AI suggestion guide for each recommendation that explains why the record was recommended, citing the specific assessment response or record detail that triggered it.
-   Surfaces related control objectives that serve as mitigating controls for the recommended risk statements.

## How recommendations are generated

Two skills recommend control objectives and risk statements based on assessment responses:

-   **Control Objective Recommender**

    Surfaces matching control objectives from the compliance policy statement library.

-   **Risk Statement Recommender**

    Surfaces matching risk statements from the risk definition library.


Each skill retrieves candidate records from an existing library using retrieval-augmented generation \(RAG\), then uses a language model to reason over the retrieved candidates and finalize a de-duplicated list.

The RAG approach matches assessment content against the library. Here's how the skills generate recommendations.

1.  Context is gathered from these sources:
    -   Processing activity details, such as name and description.
    -   Completed smart assessment responses, including information objects, data subject types and hierarchy.
2.  Based on this context, short retrieval texts are generated that represent distinct privacy obligations.
3.  Each retrieval text is used to query the library for semantically similar control objectives or risk statements.
4.  The retrieved candidates are evaluated, and the most relevant records are selected and displayed in the Recommendations tab of a privacy assessment task.

## Role requirements to generate recommendations

|Role|Description|
|----|-----------|
|sn\_prm\_gen\_ai.user|Enables privacy analysts to generate AI recommendations, view them in the Recommendations tab, and accept, dismiss, or revert recommendations on the assessment.|
|sn\_privacy.analyst|Enables privacy analysts to access assigned privacy assessment tasks from the Privacy Workspace and add or remove records from the Applicable scope tab.|

## Recommendations tab in a privacy assessment task

On the Overview tab of a privacy assessment in Review state, the reviewer selects the **Recommend** button to generate AI recommendations. The Recommendations tab opens and displays the results on separate Control objectives and Risk Statements sub-tabs.

The following image shows the Recommendations tab on a privacy assessment task.

\[Omitted image "ai-prm-recco-tab.png"\] Alt text: Recommendations tab of a privacy assessment task in the Review state hosts all the AI-recommended control objectives and risk statements.

**Note:** If there’s no relevant data available, the recommendations page indicates that the request was completed and there are no recommendations currently available. If the request is in progress, try reloading the page after some time.

Each recommendation card in the New state displays the option to accept and dismiss it. After a reviewer accepts or dismisses a recommendation, the card displays the state as Accepted or Dismissed and offers a **Revert** option to reset the state. Accepted recommendations automatically reflect in the Applicable scope tab on the assessment task record.

For details about the recommendation cards, see [AI-recommended control objectives](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/act-ai-recco-co-pia.md) and [AI-recommended risk statements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/act-ai-recco-rs-pia.md).

## Applicable scope tab in a privacy assessment task

The Applicable scope tab lists all the records that apply to the processing activity. Records in this tab originate from three sources, identified by the Mode column.

|Mode|Description|
|----|-----------|
|**Automated**|Records added by smart assessment automation rules configured in the assessment template.|
|**AI-assisted**|Records accepted from the Recommendations tab.|
|**Manual**|Records added manually by the privacy analyst during review.|

Reviewers can manually add and remove records from Applicable scope regardless of how they originated, including accepted AI recommendations and records added through automation rules.

**Note:** If a recommended record is already in applicable scope from another mode such as automation, accepting the recommendation does not create a duplicate. The Mode column retains the value of the original source. If that record is later removed from the Applicable scope tab and the reviewer then accepts the same recommendation, the record is added back with AI-assisted as its mode.

The summary cards for control objectives and risk statements in the Overview tab display the following counts:

-   **In scope**

    Total number of records in the Applicable scope tab, including accepted AI recommendations, records added by smart assessment automation rules, and records added manually by the reviewer. Selecting this count opens a list of all the records that are scoped to the processing activity.

-   **Recommended**

    Total number of control objectives or risk statements recommended by the AI skills. Selecting this count opens the Recommendations tab.

-   **Accepted recommendations**

    Number of AI-recommended records that the reviewer accepted. Selecting this count opens a filtered list of accepted recommendations.

-   **Auto-scoped by rule**

    Number of records added to applicable scope by smart assessment automation rules. Selecting this count opens a filtered list of records scoped by automation rules.


