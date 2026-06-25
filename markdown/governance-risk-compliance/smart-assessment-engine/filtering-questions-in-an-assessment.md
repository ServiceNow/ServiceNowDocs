---
title: Filtering questions in an assessment
description: Responders can narrow the question list in an assessment by selecting one or more filters from the filter dropdown. Filters can be combined to focus on questions that match every selected criterion.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/filtering-questions-in-an-assessment.html
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2026-06-04"
reading_time_minutes: 2
keywords: [filter, filtering, question filter, assessment]
breadcrumb: [Respond to assessments, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Filtering questions in an assessment

Responders can narrow the question list in an assessment by selecting one or more filters from the filter dropdown. Filters can be combined to focus on questions that match every selected criterion.

## Filter overview

The filter is labeled **All questions** with no filter is applied. When a responder opens the drop- down list, they see a list of filters that they can select individually or in combination. The drop- down list label updates to reflect what is active — for example, **AI assisted +1** when two filters are selected.

Selecting multiple filters narrows the list to questions that match every selected filter. For example, selecting both **Unanswered** and **Flagged** shows only questions that are unanswered and flagged.

For the step-by-step procedure, see [Filter questions in an assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/filter-questions-in-an-assessment.md).

## Available filters

The filter drop-down list includes the following options:

-   **Unanswered**

    Shows only questions that don't yet have a response. Use this filter to find every question that still needs an answer before submitting the assessment.

-   **AI assisted**

    Shows only questions that have AI-generated suggestions. A question is considered AI assisted after the Smart Assessment Response Assist skill produces a suggestion for it. This applies whether the suggestion was applied, modified, or discarded. For more information about AI-generated responses, see [Smart Assessment response assist skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/ai-generated-responses-for-smart-assessment.md).

-   **With comments**

    Shows only questions that have at least one comment or work note attached to them. Comments and work notes are added at the question level through the dynamic panel on each question card. For more information, see [Collaboration in assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/collaboration-in-assessments.md).

-   **Flagged**

    Shows only questions that are currently in the Flagged state. A flagged question is one that a reviewer or contributor has marked as needing attention. For more information about the flagging workflow, see [Collaboration in assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/collaboration-in-assessments.md).

-   **Resolved**

    Shows only questions that are in the Resolved state. A question is moved to the Resolved state when a previously raised flag on it has been addressed. For more information about flag states, see [Collaboration in assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/collaboration-in-assessments.md).


## Combining and clearing filters

Each filter in the drop- down list can be selected or deselected independently:

-   To apply a filter, open the drop- down list and select the filter. The question list updates immediately to match.
-   To combine filters, select more than one option in the drop- down list. The list narrows to questions that match every selected filter.
-   To remove a single filter, reopen the drop- down list and deselect that filter. The remaining selected filters stay active.
-   To remove all filters at once, use the **Clear** option in the drop- down list or change it back to **All questions**.

