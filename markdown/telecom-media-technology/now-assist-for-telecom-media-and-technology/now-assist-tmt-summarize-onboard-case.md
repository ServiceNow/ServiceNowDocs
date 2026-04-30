---
title: Summarize an account onboarding case using Now Assist for Telecommunications, Media and Technology \(TMT\)
description: Generate a summary from the fields that you selected on the account onboarding case record. Quickly understand the case context by using the account onboarding case summarization skill in the Now Assist for TMT application.
locale: en-US
release: zurich
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Use generative AI skills, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Summarize an account onboarding case using Now Assist for Telecommunications, Media and Technology \(TMT\)

Generate a summary from the fields that you selected on the account onboarding case record. Quickly understand the case context by using the account onboarding case summarization skill in the Now Assist for TMT application.

## Before you begin

Role required: sn\_acct\_lc.agent

## About this task

The account onboarding case summarization skill provides you with a concise summary including details about each stage in the account boarding lifecycle. With this skill, you can do the following tasks:

-   Generate an initial summary of an account onboarding case so that you can understand the onboarding case context.
-   Summarize all the work that has been done on an account onboarding case.

The account onboarding case summarization skill is available in CSM/FSM Configurable Workspace and in Core UI.

-   In CSM/FSM Configurable Workspace, you use the Account Onboarding Case summary by Now Assist component to generate a summary. This component appears above the Activities card.
-   In Core UI, you select the **Summarize** button on the account onboarding case record to generate a summary.

**Note:** The account onboarding case summarization skill must be active. If it isn’t active, summaries are generated using the out of the box case summarization skill.

The account onboarding case summarization skill checks the record to determine if there’s enough information available to create a summary:

-   When an agent opens the account onboarding case record.
-   When an agent refreshes the account onboarding case record page.

If there’s enough data, the Account Onboarding Case summary component displays the **Summarize** button. If there isn’t enough data, the component displays a message in place of the button.

**Note:** The account onboarding case summarization skill requires a minimum 50 words in the case record to generate the summary.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** &gt; **Lists** &gt; **Account Onboarding Case**.

2.  Open an account onboarding case.

3.  In the Account Onboarding Case summary by Now Assist component, select **Summarize**.

    The Account Onboarding Case summary by Now Assist component appears above the Activities card. The component is collapsed by default and expands to display the summary. For longer summaries that don't fit in the window, select **View more** and use the scroll bar to view the rest of the content.

    **Note:** Generating and displaying the summary may take several seconds.

4.  After you're finished summarizing an account onboarding case, manage the results.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d22257e169">

Option

</th><th align="left" id="d22257e172">

Procedure

</th></tr></thead><tbody><tr><td id="d22257e178">

**View more or less summary details**

</td><td>

-   To see more details summary details, select the View more icon \(![Expand card icon.](../image/icon-expand.png)\).
-   To see fewer summary details, select the View less icon \(![Collapse card icon.](../image/icon-collapse.png)\).


</td></tr><tr><td id="d22257e208">

**Provide feedback for the summary**

</td><td>

-   If you think that the summary was helpful, select the helpful icon \(![Helpful icon.](../image/icon-helpful.png)\).
-   If you think that the summary wasn’t helpful, select the not helpful icon \(![Not helpful icon.](../image/icon-not-helpful.png)\).
 This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d22257e241">

**Copy the summary**

</td><td>

Select the copy to clipboard icon \(![Copy to clipboard icon.](../image/icon-copy.png)\) to use the summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d22257e256">

**View the information about the summary**

</td><td>

To check some details about the summary, select the more info icon \(![More info icon.](../image/icon-more-info.png)\).

</td></tr></tbody>
</table>
**Parent Topic:**[Using Now Assist for Telecommunications, Media and Technology \(TMT\)](../concept/now-assist-spm-using.md)

