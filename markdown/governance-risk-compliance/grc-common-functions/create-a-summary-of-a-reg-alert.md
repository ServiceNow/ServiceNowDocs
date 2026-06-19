---
title: Generate a regulatory alert summary
description: Generate a summary of a new regulatory alert for a quick analysis of the alert using the regulatory alert summarization skill. Summarized alerts help compliance officers, regulatory managers, and legal teams quickly understand the impact of new regulations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/grc-common-functions/create-a-summary-of-a-reg-alert.html
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Now Assist, generative AI]
breadcrumb: [Use generative AI skills, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Generate a regulatory alert summary

Generate a summary of a new regulatory alert for a quick analysis of the alert using the regulatory alert summarization skill. Summarized alerts help compliance officers, regulatory managers, and legal teams quickly understand the impact of new regulations.

## Before you begin

Role required: sn\_grc\_reg\_change.user and sn\_grc\_comp\_genai.reg\_change\_ai\_user

For more information on related roles and regulatory alerts, see [Types of alerts, user roles, and states of regulatory alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/regulatory-change-management-service-portal/user_roles_and_actions.md).

## About this task

Install the Now Assist for IRM application to generate regulatory alert summaries. For more information, see [Now Assist for Integrated Risk Management \(IRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-common-functions/now-assist-for-irm.md).

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see .

The summary for a regulatory alert is generated based on the prompts set during the configuration of the summarization skill. For example, if you select important dates, regulatory authority, summary of changes, penalties, and fines as key details to capture, the summary includes that information. After the summary is generated, you can directly use the summary and save it in the activity stream of the regulatory alert.

Starting with version 19.0.x, users who have the Now Assist for IRM application installed can use the regulatory alert summarization, recommend alert impacted citations, and regulatory alert impacted control objectives skills.

**Important:** Be sure to check AI-generated summaries for accuracy. If no information is available, the generated summary displays “**No specific information available for penalty or fines and so on"**.

By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see . \(Note that global domain is not the same as global scope. For more information, see .\)

## Procedure

1.  Navigate to one of the following locations:

    -   **Workspaces** &gt; **Compliance Workspace**, select the list icon \[Omitted image "ws-list-icon.png"\] Alt text: and then navigate to **Regulatory alerts**.
    -   **Workspaces** &gt; **Compliance Workspace** select the Regulatory Change Management dashboard icon \[Omitted image "reg-change-icon.png"\] Alt text: and then in the Activity overview, Tracking, or Trends section, select any segment or value in an Alerts related widget to open the list of regulatory alerts with that state.
2.  Select a regulatory alert in any state except Closed or Cancelled.

3.  On the Overview tab, select **Summarize**.

    The summary is displayed.

4.  Review the summary and complete any of the following options.

<table id="choicetable_szp_rjg_d2c"><thead><tr><th align="left" id="d153925e211">

Option

</th><th align="left" id="d153925e214">

Description

</th></tr></thead><tbody><tr><td id="d153925e220">

**Share to additional comments**

</td><td>

Select the **Share to additional comments** button to launch the Summarized result in an editor window. You can modify or review the summary and make any necessary corrections to improve its accuracy and completeness.

</td></tr><tr><td id="d153925e235">

**View more**

</td><td>

Select this link to expand the summary.

</td></tr><tr><td id="d153925e244">

**View less**

</td><td>

Select this link to collapse the summary.

</td></tr><tr><td id="d153925e253">

**Provide feedback**

</td><td>

Select the helpful icon \[Omitted image "a3961a217c6c42794d87b70ca50a5c4e51637db4.png"\] Alt text: for positive feedback. Select the not helpful icon \[Omitted image "a8538f6374f4f5e87b48dc63f04908d721aa1789.png"\] Alt text: if the summary wasn't helpful.

 **Note:** Feedback improves the generative AI model and can help to improve future versions of this skill.

</td></tr><tr><td id="d153925e279">

**Copy the summary**

</td><td>

Select the copy icon \[Omitted image "0e923b11ae593b3c5240d2fab57b32bca386c59d.png"\] Alt text: to copy the summary to the clipboard.

</td></tr><tr><td id="d153925e296">

**Regenerate the summary**

</td><td>

If you think that data might have changed after you viewed the summary, select the refresh icon \[Omitted image "refresh-icon.jpg"\] Alt text: to regenerate the summary information.

</td></tr></tbody>
</table>
