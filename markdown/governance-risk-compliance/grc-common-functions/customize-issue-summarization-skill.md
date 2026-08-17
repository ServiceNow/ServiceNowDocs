---
title: Customize the issue summarization skill in ServiceNow Otto for Integrated Risk Management \(IRM\)
description: If you have the admin role, you can customize the issue summarization skill so that users can use the generative AI skills in Risk Workspace and in Core UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/customize-issue-summarization-skill.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [ServiceNow Otto, generative AI]
breadcrumb: [Configure, ServiceNow Otto, Common GRC features, Governance, Risk, and Compliance]
---

# Customize the issue summarization skill in ServiceNow Otto for Integrated Risk Management \(IRM\)

If you have the admin role, you can customize the issue summarization skill so that users can use the generative AI skills in Risk Workspace and in Core UI.

## Before you begin

Role required: admin

## About this task

From the AI Admin Hub console, you can select the input data in various states for the skill and then configure the prompt headers to include them in the summary.

## Procedure

1.  Navigate to **All** &gt; **Admin Center** &gt; **AI Admin Hub.**

2.  Select the **AI skills** tab.

3.  In the **Technology** workflow group, select **Risk &amp; Sustainability**.

4.  Copy the issue summarization skill for customization.

    1.  On the feature card that is associated with the skill that you would like to customize, select the Options \(\[Omitted image "option-icon.png"\] Alt text: Options icon.\) icon and then select **Make a copy**.

    2.  On the confirmation dialog, select **Make a copy**.

5.  In the General details step, fill in the fields.

    1.  Enter a name and description for the skill.
    2.  Select **Save and continue**.
6.  View the input data for each skill and the base input fields.

    Configure the base input table fields for the skill.

    Each skill relies on a base input table and input fields with descriptions to provide context for the Now LLM Service to generate a response.

    \[Omitted image "choose-input-data.png"\] Alt text: Choose input data screen.

    1.  Select **Save and continue**.

    2.  Select **Back** to go the previous step.

7.  Define how the skill is available to your users.

    1.  Configure the skill to be always available to users, or select conditions that must be met before the skill is available.

        Selecting **Customize skill availability** displays a condition builder to filter the data further.

    2.  Select **Save and continue**.

    3.  Select **Back** to go the previous step.

8.  In the Select display step, configure where to display the issue summarization skill.

    **In-product desktop**: When selected, the Now Assist skills are displayed on the forms and workspaces.

    1.  Select the roles for whom you want the skill to be displayed.

    2.  Select **Save and continue**.

    3.  Select **Back** to go the previous step.

9.  In the Review and activate step, review all the details before activating the skill.

10. Select **Activate**.

11. Select **Back** to go the previous step.


## Result

You can select **Summarize** in an issue to generate the issue summary.

