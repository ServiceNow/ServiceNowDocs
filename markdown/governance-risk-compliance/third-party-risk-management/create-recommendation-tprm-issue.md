---
title: Generate issue recommendations for TPRM
description: Use generative AI to identify and recommend potential Third-party Risk Management issues based on assessment responses. The TPRM issue recommendation skill presents recommended issues with rationalized summaries for reviewer confirmation.
locale: en-US
release: zurich
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, generative AI]
breadcrumb: [Use generative AI skills, Now Assist, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Generate issue recommendations for TPRM

Use generative AI to identify and recommend potential Third-party Risk Management issues based on assessment responses. The TPRM issue recommendation skill presents recommended issues with rationalized summaries for reviewer confirmation.

## Before you begin

The assessment you are using to generate issue recommendations must use the Smart Assessment Engine. Starting with version 21.0.x of the Third-party Risk Management application, you can enable the Smart Assessment Engine \(SAE\) by setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property. After setting this property, SAE becomes the default assessment engine and replaces the legacy experience. The transition isn’t reversible.

**Warning:**

Set this property in your non-production instances and conduct thorough testing before changing your production instances. Failure to do so may result in unexpected issues.

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

Role required: sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer

## About this task

The third party or engagement must have completed prior assessments, and reviewers must have previously created issues from those assessments. The recommendation skill uses these historical issues and their associated questions and responses as reference data. TPR Assessors generate issue recommendations. TP Reviewers can review, accept, or dismiss the generated recommendations.

For more information on activating the recommendation for TPRM issues skill, refer to [Activate TPRM issue recommendation skill](tprm-recommend-an-issue.md).

**Note:** If you want generated issues to be created using historical data for individual third parties or engagements, a team member with the administrator role needs to navigate to **All** &gt; **System Properties** &gt; **All** select `sn_tprm_genai.same_vendor_required` and set the property to true.

By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the Now Assist Admin console](https://www.servicenow.com/docs/access?context=domain-separation-in-the-now-assist-admin-console&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://www.servicenow.com/docs/access?context=next-experience-pickers&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).\)

**Important:** Be sure to check AI-generated recommendations for accuracy.

## Procedure

1.  Navigate to **Workspaces** &gt; **Vendor Management Workspace**, select the list icon ![](../../grc-workspace-vrm/image/ws-list-icon.png) and then navigate to **Questionnaire requests** &gt; **All**.

2.  Select an **Assessment instance** in the Responses received, Generating responses, or Completed state that you want to generate recommendations for.

    The completed assessment opens and you can review all sections, questions, responses, and details. You can return the questionnaire to the third party or engagement if there are any discrepancies by selecting **Return questionnaire to third party**.

3.  Generate recommendations by selecting **Generate predicted issues**.

4.  To view the status of the recommendations, refresh the Predicted issues pane.

    Issue recommendation requests are asynchronous enabling you to complete other tasks while the request is processed. You can select the refresh icon ![](../../grc-risk/image/refresh-icon.jpg) to view the latest.

    On the Predicted issues pane, a message indicates the status of your recommendations request.

    -   No predicted issues available: If there’s no relevant historical data, the Predicted issues pane indicates that issue generation is complete and no issues are available.
    -   Generating predicted issues: If the request is in progress, try refreshing after some time.

## What to do next

Create issues based on generated issue recommendations or dismiss the issue recommendations. For more information, see [Create or dismiss issues using recommendations](manage-recommendation-issue.md).

-   **[Create or dismiss issues using recommendations](manage-recommendation-issue.md)**  
Accept recommendations to create issues based on historical assessment data, or dismiss recommendations that aren’t relevant. Accepting or dismissing issue recommendations helps reviewers efficiently act on AI‑predicted findings while retaining control over which issues are created.

**Parent Topic:**[Using Now Assist for Third-party Risk Management \(TPRM\) skills](../concept/using-now-assist-for-tprm.md)

