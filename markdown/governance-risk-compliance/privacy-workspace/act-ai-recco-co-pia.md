---
title: Accept or dismiss AI-recommended control objectives
description: Generate AI-assisted recommendations while reviewing a privacy assessment to quickly identify relevant control objectives from the privacy library.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/privacy-workspace/act-ai-recco-co-pia.html
release: zurich
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-08-24"
reading_time_minutes: 3
keywords: [review, AI recommendations, privacy task, control objectives, risk statements, Privacy Management]
breadcrumb: [AI recommendations in privacy assessments, ServiceNow Otto for Privacy Management, Privacy Management, Governance, Risk, and Compliance]
---

# Accept or dismiss AI-recommended control objectives

Generate AI-assisted recommendations while reviewing a privacy assessment to quickly identify relevant control objectives from the privacy library.

## Before you begin

The assessment task must be in Review state.

Role required: sn\_privacy.analyst, sn\_prm\_gen\_ai.user

**Note:** Without the sn\_prm\_gen\_ai.user role, the privacy analyst reviewing the assessment can't generate AI recommendations.

## About this task

After a business user submits a privacy assessment, the assessment task moves to the Review state. As its assigned analyst, generate AI recommendations to quickly surface relevant control objectives and risk statements based on the assessment’s responses. The corresponding controls and risks for the accepted records are automatically scoped to the processing activity.

**Note:** Review all AI-generated recommendations for accuracy.

The Control Objective Recommender skill generates the control objective recommendations. For more information about the skill, see [AI reviewer assist for privacy assessment tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/ai-reccos-for-pia.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Privacy Workspace**.

2.  Select the Tasks icon \[Omitted image "icon-tprm-ws-tasks.png"\] Alt text:.

3.  In the My pending tasks tab, select **Privacy assessments**.

4.  Open the privacy assessment to be reviewed.

5.  On the Overview tab, select **Recommend**.

    The Recommendations tab organizes results into two tabs, Control objectives and Risk statements. If the request is still in progress, reload the page after some time. The request might take longer depending on the volume of data the skill processes. If no relevant data is available, the tab indicates that the request was completed and there are no recommendations currently available.

6.  To review the control objective recommendations, select the Control objectives tab.

7.  Select a control objective recommendation card to review.

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
</table>8.  View the control objective in the privacy library or refresh your recommendations.

    |Option|Description|
    |------|-----------|
    |**Select the details icon \[Omitted image "details-icon.jpg"\] Alt text:.**|View details of the record in the privacy library.|
    |**Select the refresh icon \[Omitted image "refresh-icon.jpg"\] Alt text:.**|Refresh the recommendations to reflect the latest data.|

9.  Accept or dismiss the recommendation.

    -   If the recommendation is relevant, select **Accept**, then select **Accept and add** to confirm.
    -   If the recommendation isn't relevant, select **Dismiss**, then select **Confirm**.
    Accepted control objectives are automatically added to the Applicable scope tab of the assessment task.

10. To change your decision on an accepted or dismissed recommendation, select the card, then select **Revert**.


## Result

All the records scoped to a processing activity based on assessment responses appear in the Applicable scope tab of the assessment task. These include the accepted AI recommendations, and records added manually and through smart assessment automation rules. Filter by AI-assisted in the Mode column to confirm if the accepted control objective recommendations appear in the list correctly. If you must add more records, you can manually add those to the tab.

**Note:** If a recommended record is already in Applicable scope from another mode such as automation, accepting the recommendation does not create a duplicate. The Mode column retains the value of the original source. If that record is later removed from Applicable scope and the reviewer then accepts the same recommendation, the record is added back with AI-assisted as its mode.

## What to do next

Review the risk statement recommendations. For steps, see [Accept or dismiss AI-recommended risk statements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/act-ai-recco-rs-pia.md). When done, mark the assessment as complete. For steps, see [Review a privacy assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/privacy-workspace/review-a-privacy-assessment.md). Closing an assessment task automatically adds the corresponding controls for the accepted recommendations to the processing activity record.

