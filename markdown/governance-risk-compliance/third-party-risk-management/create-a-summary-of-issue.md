---
title: Generate a summary of a TPRM issue
description: Generate a summary of a TPRM issue to support efficient triaging, remediation, and reporting using the TPRM issue summarization skill. Summarized issues help risk assessors and analysts quickly review issue content and take informed action.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/third-party-risk-management/create-a-summary-of-issue.html
release: zurich
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [ServiceNow Otto, Agentic AI, generative AI, Gen AI]
breadcrumb: [Assess third-party risk, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Generate a summary of a TPRM issue

Generate a summary of a TPRM issue to support efficient triaging, remediation, and reporting using the TPRM issue summarization skill. Summarized issues help risk assessors and analysts quickly review issue content and take informed action.

## Before you begin

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

Role required: sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer

## About this task

The summary for a TPRM issue is generated based on all the information captured in the issue record. After the summary is generated, you can save it to the activity stream or share it in the **Work Notes** field for visibility.

**Important:** Be sure to check AI-generated summaries for accuracy.

## Procedure

1.  Navigate to one of the following locations:

    -   **Workspaces** &gt; **Vendor Management Workspace**, select the list icon \[Omitted image "ws-list-icon.png"\] Alt text: and then navigate to **Issues**.
    -   **Workspaces** &gt; **Vendor Management Workspace**, select the tasks icon \[Omitted image "icon-tprm-ws-tasks.png"\] Alt text: and then navigate to the **My pending tasks** tab and select **Issues**.
2.  Select an issue in any state.

3.  On the **Overview** tab, select **Summarize**.

    The summary is displayed.

    **Note:** The Summarize button appears only if the summarization skill is enabled.

4.  Review the summary and complete any of the following options.

<table><thead><tr><th align="left" id="d384545e186">

Option

</th><th align="left" id="d384545e189">

Description

</th></tr></thead><tbody><tr><td id="d384545e195">

**Share to work notes**

</td><td>

Select the **Share to work notes** button to launch the summarized result in an editor window. You can modify or review the summary and make any necessary corrections to improve its accuracy and completeness.

</td></tr><tr><td id="d384545e210">

**View more**

</td><td>

Select this link to expand the summary.

</td></tr><tr><td id="d384545e219">

**View less**

</td><td>

Select this link to collapse the summary.

</td></tr><tr><td id="d384545e228">

**Provide feedback**

</td><td>

Select the helpful icon \[Omitted image "icon-helpful.png"\] Alt text: for positive feedback. Select the not helpful icon \[Omitted image "icon-not-helpful.png"\] Alt text: if the summary wasn't helpful.

 **Note:** Feedback improves the generative AI model and can help to improve future versions of this skill.

</td></tr><tr><td id="d384545e254">

**Copy the summary**

</td><td>

Select the copy icon \[Omitted image "icon-copy.png"\] Alt text: to copy the summary to the clipboard.

</td></tr><tr><td id="d384545e271">

**Regenerate the summary**

</td><td>

If you think that data might have changed after you viewed the summary, select the refresh icon \[Omitted image "refresh-icon.jpg"\] Alt text: to regenerate the summary information.

</td></tr></tbody>
</table>
