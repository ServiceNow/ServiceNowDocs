---
title: Create or dismiss issues using recommendations
description: Accept recommendations to create issues based on historical assessment data, or dismiss recommendations that aren’t relevant. Accepting or dismissing issue recommendations helps reviewers efficiently act on AI‑predicted findings while retaining control over which issues are created.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, generative AI]
breadcrumb: [Generate TPRM issue recommendations, Use generative AI skills, Now Assist, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Create or dismiss issues using recommendations

Accept recommendations to create issues based on historical assessment data, or dismiss recommendations that aren’t relevant. Accepting or dismissing issue recommendations helps reviewers efficiently act on AI‑predicted findings while retaining control over which issues are created.

## Before you begin

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

Role required: sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer

**Important:** Be sure to check AI-generated recommendations for accuracy.

## Procedure

1.  Navigate to **Workspaces** &gt; **Vendor Management Workspace**, select the list icon ![](../../grc-cam-workspace/image/ws-list-icon.png) and then navigate to **Questionnaire requests** &gt; **All**.

2.  Select an **Assessment instance** in the Responses received, Generating responses, or Completed state that you want to view generated issues for.

3.  Review the generated issues in the Predicted issues pane.

    If recommendations are available, you can scroll through the generated issue recommendation cards and review a summary for each issue.

    **Note:** The recommended issues are based on historical data.

4.  View more details for the generated issues by completing one of the following.

    -   Select the individual issue recommendation card to view more details about that issue.
    -   Select **View all** to review all recommended issues and their additional details.
    |Field|Description|
    |-----|-----------|
    |Number|Auto-generated number to recommended issue.|
    |Name|Name of the issue.|
    |Description|Description and summary of the issue.|
    |Smart assessment question instance|Assessment question associated with the recommended issue.|
    |Types|Source of the historic data. By default, it is from the previous assessments.|
    |Priority|Priority of the historical issue.|
    |Historical issues|Historical issue that was used as data to generate the recommended issue.|

5.  Create issues based on these recommendations or dismiss the recommendations.

<table id="choicetable_mqj_mcr_23c"><thead><tr><th align="left" id="d42742e243">

Option

</th><th align="left" id="d42742e246">

Description

</th></tr></thead><tbody><tr><td id="d42742e252">

**Create issues or dismiss issues from the Predicted issues pane**

</td><td>

1.  Navigate to the recommendation card you want.
2.  Select **Create issue** or **Dismiss**.


</td></tr><tr><td id="d42742e276">

**Create issues or dismiss issues from the Predicted issues list**

</td><td>

1.  Select the checkbox of the issue you want.
2.  Select **Create issue** or **Delete.**


</td></tr></tbody>
</table>    If you accept the recommendation by creating an issue, an issue record is created. If you dismiss the recommendation, it’s marked as dismissed and removed from the Predicted issues list for that assessment.


## What to do next

If you accepted any recommendations, confirm the creation of your issues by navigating to the Issues tab for that assessment.

**Note:** Dismissed issues and created issues reappear if when you select **Generate predicted issues** again.

**Parent Topic:**[Generate issue recommendations for TPRM](create-recommendation-tprm-issue.md)

