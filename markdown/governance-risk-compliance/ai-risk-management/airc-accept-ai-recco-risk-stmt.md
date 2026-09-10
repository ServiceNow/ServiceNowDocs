---
title: Accept or dismiss AI-recommended risk statements
description: Generate AI-assisted recommendations to quickly identify and associate relevant risk statements with an AI Assessment from the AI risk and compliance library.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/airc-accept-ai-recco-risk-stmt.html
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2026-08-30"
reading_time_minutes: 3
breadcrumb: [Use, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Accept or dismiss AI-recommended risk statements

Generate AI-assisted recommendations to quickly identify and associate relevant risk statements with an AI Assessment from the AI risk and compliance library.

## Before you begin

The assessment task must be in Review state.

Role required: sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst, sn\_airc\_gen\_ai.airc\_ai\_user

**Note:** Without the sn\_airc\_gen\_ai.airc\_ai\_user role, the risk and compliance analyst reviewing the assessment can't generate AI recommendations.

## About this task

After a business user submits an AI Assessment, the assessment task moves to the Review state. As the assigned analyst on the assessment task, generate AI recommendations to quickly surface relevant control objectives and risk statements based on the assessment responses. Accepting a recommendation automatically scopes that record to the AI Asset, and maps corresponding risks and controls to it.

**Note:** Review all AI-generated recommendations for accuracy.

The Risk Statement Recommender skill generates the risk statement recommendations. Each risk statement recommendation displays related control objectives that serve as mitigating controls for the identified risks.

For more information about the skill, see [AI reviewer assist for risk assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/ai-based-reviewer-assistant-for-assessments.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Risk and Compliance Workspace**.

2.  Select the Tasks icon \[Omitted image "icon-tprm-ws-tasks.png"\] Alt text:.

3.  In the My pending tasks tab, select **Risk assessments**.

4.  Open the privacy assessment to be reviewed.

5.  On the Overview tab, select **Recommend**.

    The Recommendations tab opens. It organizes the AI recommendations into two tabs, Control objectives and Risk statements. If there’s no relevant data available, the recommendations page indicates that the request was completed and there are no recommendations currently available.

6.  To review the risk statement recommendations, select the Risk statements tab.

    **Note:** A risk statement that is already in scope through manual addition or automation rules, isn't recommended.

7.  Select a risk statement recommendation card to review.

    Each card displays:

<table id="id_b2w_dgj_jkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the risk statement.

</td></tr><tr><td>

Category

</td><td>

Business or technical domain for the risk statement.

</td></tr><tr><td>

Classification

</td><td>

Risk classification based on use and purpose

</td></tr><tr><td>

AI suggestion guide

</td><td>

Reason for recommending the risk statement. It references the specific assessment responses and record context that contributed to the recommendation.**Note:** Review AI-generated content for accuracy.

</td></tr><tr><td>

Description

</td><td>

Description and summary of the risk statement.

</td></tr><tr><td>

Review and accept mitigating controls

</td><td>

Related control objectives that mitigate the risk.**Note:** Only the control objectives that are also recommended for the same assessment appear here. For example, a risk statement might have five mitigating control objectives mapped to it in the library. If only one of those was recommended for this assessment, only that control objective is listed.

</td></tr></tbody>
</table>8.  View the risk statement in the privacy library or refresh your recommendations.

    |Option|Description|
    |------|-----------|
    |**Select the details icon \[Omitted image "details-icon.jpg"\] Alt text:.**|View details of the record in the privacy library.|
    |**Select the refresh icon \[Omitted image "refresh-icon.jpg"\] Alt text:.**|Refresh the recommendations to reflect the latest data.|

9.  To scope related control objectives along with the recommended risk statement, select each record from the Control objective sub-tab within Review and accept mitigating controls.

    The State column shows Accepted for a control objective that is already in Applicable scope, and New for those that haven't been acted on yet.

10. Accept or dismiss the recommendation.

    -   If the recommendation is relevant, select **Accept**, then select **Accept and add** to confirm.
    -   If the recommendation isn't relevant, select **Dismiss**, then select **Confirm**.
    An accepted risk statement, and any related control objectives you selected with it, are automatically added to the Applicable scope tab of the assessment task. A dismissed risk statement results in any related control objectives you selected to be dismissed with it.

11. To change your decision on an accepted or dismissed recommendation, select the card, then select **Revert**.


## Result

All accepted AI recommendations are scoped to the asset and appear in the Applicable scope tab of the assessment task. The applicable scope also includes other control objectives and risk statements added manually and through smart assessment automation rules. Filter by AI-assisted in the Mode column to confirm if the accepted control objective recommendations appear in the list correctly. If you must add more records, you can manually add those to the tab.

## What to do next

Review the control objective recommendations. For steps, see [Accept or dismiss AI-recommended control objectives](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/airc-accept-ai-recco-co.md). When done, mark the assessment as complete.

**Parent Topic:**[Using AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/using-ai-risk-and-compliance.md)

