---
title: Accept or dismiss AI-recommended control objectives
description: Generate AI-assisted recommendations to quickly identify and associate relevant control objectives with an AI Assessment from the AI risk and compliance library.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/airc-accept-ai-recco-co.html
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2026-08-30"
reading_time_minutes: 3
breadcrumb: [Use, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Accept or dismiss AI-recommended control objectives

Generate AI-assisted recommendations to quickly identify and associate relevant control objectives with an AI Assessment from the AI risk and compliance library.

## Before you begin

The assessment task must be in Review state.

Role required: sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst, sn\_airc\_gen\_ai.airc\_ai\_user

**Note:** Without the sn\_airc\_gen\_ai.airc\_ai\_user role, the risk and compliance analyst reviewing the assessment can't generate AI recommendations.

## About this task

After a business user submits an AI Assessment, the assessment task moves to the Review state. As the assigned analyst on the assessment task, generate AI recommendations to quickly surface relevant control objectives and risk statements based on the assessment responses. Accepting a recommendation automatically scopes that record to the AI Asset, and maps corresponding risks and controls to it.

**Note:** Review all AI-generated recommendations for accuracy.

The Control Objective Recommender skill generates the control objective recommendations. For more information about the skill, see [AI reviewer assist for risk assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/ai-based-reviewer-assistant-for-assessments.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Risk and Compliance Workspace**.

2.  Select the List icon \[Omitted image "icon-list.png"\].

3.  Open the AI asset.

4.  Select **AI assessments**.

5.  Open the AI assessment to be reviewed.

6.  On the Overview tab, select **Recommend**.

    The Recommendations tab opens. It organizes the AI recommendations into two tabs, Control objectives and Risk statements. If there’s no relevant data available, the recommendations page indicates that the request was completed and there are no recommendations currently available.

7.  To review the control objective recommendations, select the Control objectives tab.

    **Note:** A control objective that is already in scope through manual addition or automation rules, isn't recommended.

8.  Select a control objective recommendation card to review.

    Each card displays:

<table id="table_f34_r23_jkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the control objective.

</td></tr><tr><td>

Category

</td><td>

Business or technical domain of the control objective.

</td></tr><tr><td>

Classification

</td><td>

Functional intent of the control objective, such as Preventive or Corrective.

</td></tr><tr><td>

AI suggestion guide

</td><td>

Reason for recommending the control objective. It references the specific assessment responses and record context that contributed to the recommendation.**Note:** Review AI-generated content for accuracy.

</td></tr><tr><td>

Description

</td><td>

Description and summary of the control objective.

</td></tr><tr><td>

Supplemental guidance

</td><td>

Additional guidance related to the control objective and how to address it.

</td></tr><tr><td>

Mapped citations

</td><td>

Citations mapped to the control objective. Citations are informational and don't affect the applicable scope.

</td></tr></tbody>
</table>9.  View the control objective in the privacy library or refresh your recommendations.

    |Option|Description|
    |------|-----------|
    |**Select the details icon \[Omitted image "details-icon.jpg"\] Alt text:.**|View details of the record in the privacy library.|
    |**Select the refresh icon \[Omitted image "refresh-icon.jpg"\] Alt text:.**|Refresh the recommendations to reflect the latest data.|

10. Accept or dismiss the recommendation.

    -   If the recommendation is relevant, select **Accept**, then select **Accept and add** to confirm.
    -   If the recommendation isn't relevant, select **Dismiss**, then select **Confirm**.
    Accepted control objectives are automatically added to the Applicable scope tab of the assessment task.

11. To change your decision on an accepted or dismissed recommendation, select the card, then select **Revert**.


## Result

All accepted AI recommendations are scoped to the asset and appear in the Applicable scope tab of the assessment task. The applicable scope also includes other control objectives and risk statements added manually and through smart assessment automation rules. Filter by AI-assisted in the Mode column to confirm if the accepted control objective recommendations appear in the list correctly. If you must add more records, you can manually add those to the tab.

## What to do next

Review the risk statement recommendations. For steps, see [Accept or dismiss AI-recommended risk statements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/airc-accept-ai-recco-risk-stmt.md). When done, mark the assessment as complete.

**Parent Topic:**[Using AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/using-ai-risk-and-compliance.md)

