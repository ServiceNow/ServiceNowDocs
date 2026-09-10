---
title: Accept or dismiss AI-recommended risk statements
description: Generate AI-assisted recommendations while reviewing a privacy assessment to quickly identify relevant risk statements from the privacy library.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/privacy-workspace/act-ai-recco-rs-pia.html
release: zurich
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-08-24"
reading_time_minutes: 5
keywords: [review, AI recommendations, privacy task, control objectives, risk statements, Privacy Management]
breadcrumb: [AI recommendations in privacy assessments, ServiceNow Otto for Privacy Management, Privacy Management, Governance, Risk, and Compliance]
---

# Accept or dismiss AI-recommended risk statements

Generate AI-assisted recommendations while reviewing a privacy assessment to quickly identify relevant risk statements from the privacy library.

## Before you begin

The assessment task must be in Review state.

Role required: sn\_privacy.analyst, sn\_prm\_gen\_ai.user

**Note:** Without the sn\_prm\_gen\_ai.user role, the privacy analyst reviewing the assessment can't generate AI recommendations.

## About this task

After a business user submits a privacy assessment, the assessment task moves to the Review state. As the assigned analyst on the assessment task, generate AI recommendations to quickly surface relevant control objectives and risk statements based on the assessment responses. Accepting a recommendation automatically scopes that record to the processing activity, and maps corresponding risks and controls to it.

**Note:** Review all AI-generated recommendations for accuracy.

The Risk Statement Recommender skill generates the risk statement recommendations. Each recommended risk statement includes related control objectives that help mitigate the identified risks. You can select these control objectives to scope them to the processing activity along with the risk statement.

For more information about the skill, see [AI reviewer assist for privacy assessment tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/ai-reccos-for-pia.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Privacy Workspace**.

2.  Select the Tasks icon \[Omitted image "icon-tprm-ws-tasks.png"\] Alt text:.

3.  In the My pending tasks tab, select **Privacy assessments**.

4.  Open the privacy assessment to be reviewed.

5.  On the Overview tab, select **Recommend**.

    The Recommendations tab organizes results into two tabs, Control objectives and Risk statements. If the request is still in progress, reload the page after some time. The request might take longer depending on the volume of data the skill processes. If no relevant data is available, the tab indicates that the request was completed and there are no recommendations currently available.

6.  To review the risk statement recommendations, select the Risk statements tab.

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

Functional intent of the risk statement.

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

Control objectives that are mapped to this risk statement in the privacy library and are also recommended for the current assessment. The records that are mapped in the library but not recommended for this assessment don't appear here.For example, a risk statement might have five mitigating control objectives mapped to it in the library. If only one of those was recommended for this assessment, only that control objective is listed for selection.

</td></tr></tbody>
</table>8.  View the risk statement in the privacy library or refresh your recommendations.

    |Option|Description|
    |------|-----------|
    |**Select the details icon \[Omitted image "details-icon.jpg"\] Alt text:.**|View details of the record in the privacy library.|
    |**Select the refresh icon \[Omitted image "refresh-icon.jpg"\] Alt text:.**|Refresh the recommendations to reflect the latest data.|

9.  To scope related control objectives with the recommended risk statement, select records in New state from the Control objective sub-tab of **Review and accept mitigating controls**.

    When you accept the risk statement, any selected control objectives are accepted with it. This control-to-risk mapping carries over to the processing activity record after the assessment is closed.

    **Note:** The State column shows Accepted for a control objective that is already in Applicable scope, and New for those that haven't been acted on yet.

    \[Omitted image "ai-recco-co-in-rs-pia.png"\] Alt text: Review and accept mitigating controls section in a risk statement recommendation card for a privacy assessment

10. Accept or dismiss the recommendation.

    -   If the recommendation is relevant, select **Accept**, then select **Accept and add** to confirm.
    -   If the recommendation isn't relevant, select **Dismiss**, then select **Confirm**.
    An accepted risk statement, and any control objectives you selected with it, are automatically added to the Applicable scope tab of the assessment task. A dismissed risk statement results in any related control objectives you selected to be dismissed with it.

11. To change your decision on an accepted or dismissed recommendation, select the card, then select **Revert**.


## Result

Records scoped to a processing activity based on assessment responses appear in the Applicable scope tab of the assessment task. These include accepted AI recommendations, records added manually and through smart assessment automation rules. Filter by AI-assisted in the Mode column to verify that the accepted risk statement recommendations appear in the list correctly. Any control objective you selected with the accepted risk statement also appears in this tab. If you must add more records, you can manually add those to the tab.

**Note:** If a recommended record is already in Applicable scope from another mode such as automation, accepting the recommendation does not create a duplicate. The Mode column retains the value of the original source. If that record is later removed from Applicable scope and the reviewer then accepts the same recommendation, the record is added back with AI-assisted as its mode.

## What to do next

Review the control objective recommendations. For steps, see [Accept or dismiss AI-recommended control objectives](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/act-ai-recco-co-pia.md). When done, mark the assessment as complete. For steps, see [Review a privacy assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/review-a-privacy-assessment.md). Closing the assessment task scopes the accepted recommendations to the processing activity:

-   The corresponding risk for the accepted risk statement is added to the Risks tab of the processing activity.
-   The corresponding controls from the accepted control objectives are added to the Controls tab of the processing activity.
-   The same controls are also mapped to the corresponding risk record in the processing activity, carrying over the control-to-risk mapping from the assessment task.

