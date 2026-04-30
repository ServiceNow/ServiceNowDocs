---
title: Summarize a case by using Now Assist for Financial Services Operations \(FSO\)
description: Generate a summary from the defined fields on the case record and quickly understand the case context by using the case summarization skill in the Now Assist for Financial Services Operations \(FSO\) application.
locale: en-US
release: xanadu
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
keywords: [generative AI for financial services operations generate summary, generative AI for FSO generate summary]
breadcrumb: [Using Now Assist for Financial Services Operations \(FSO\), Now Assist for Financial Services Operations \(FSO\), Financial Services Operations \(FSO\)]
---

# Summarize a case by using Now Assist for Financial Services Operations \(FSO\)

Generate a summary from the defined fields on the case record and quickly understand the case context by using the case summarization skill in the Now Assist for Financial Services Operations \(FSO\) application.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent, sn\_bom\_credit\_card.dispute\_manager, sn\_bom\_credit\_card.dispute\_viewer, sn\_bom\_credit\_card.contributor, sn\_bom.b2c\_agent, sn\_bom.b2b\_agent, sn\_bom.adjuster, sn\_bom.fnol\_representative

**Note:** These roles are the default list of roles that are defined for this task. Administrators can modify the list of roles in the Now Assist Admin console.

## About this task

The case summarization skill provides you with a concise summary of a banking card dispute or insurance claims case. With this skill, you can do the following tasks:

-   Generate an initial summary of a case so that you can understand the case context.
-   Summarize the actions taken and any resolutions for a case.

The case summarization skill is available in Financial Services Workspace and in Core UI.

-   In Financial Services Workspace, use the Case summary by Now Assist component to generate a summary. The component appears in the following areas:
    -   Insurance: Next to the claim details panel in the claim summary page, claim workspace, and claim details page
    -   Card dispute: Between the activities and case information panel
-   In Core UI, select the **Summarize** button on the case record to generate a summary.

The case summarization skill checks the case record to determine if enough information is available to create a summary:

-   When an agent opens the case record.
-   When an agent refreshes the case record page.

If there’s enough data, the Case summary component displays the **Summarize** button. If there isn’t enough data, the component displays a message in place of the button.

## Procedure

1.  Navigate to **Workspaces** &gt; **Financial Services Workspace** and open a claim or card dispute.

2.  In the Case Summary by Now Assist component, select **Summarize**.

    ![Selecting Summarize generates a case summary for the dispute or claims case.](../image/now-assist-fso-summarize-dispute.png)

    The Case Summary by Now Assist component appears next to the claim details panel or case information panel. The component is collapsed by default and expands to display the summary. For longer summaries that don't fit the window, select **View more** and use the scroll bar to view the rest of the content.

    **Note:** Generating and displaying the summary may take several seconds.

3.  When you're finished summarizing a case, you can perform additional actions.

<table id="choicetable_ybr_pjr_mbc"><thead><tr><th align="left" id="d29701e194">

Option

</th><th align="left" id="d29701e197">

Procedure

</th></tr></thead><tbody><tr><td id="d29701e203">

**Save the summary information by adding it to the case work notes**

</td><td>

1.  Select **Share to worknotes**.
2.  In the Share Case summary as Work notes dialog box, edit the summary.
3.  Select **Save to Work notes**.


</td></tr><tr><td id="d29701e230">

**Expand or collapse the summary**

</td><td>

Select the expand card icon \(![Expand card icon.](../../customer-service-management/image/icon-expand.png)\) or the collapse card icon \(![Collapse card icon.](../../customer-service-management/image/icon-collapse.png)\) to see more details or fewer summary details.

</td></tr><tr><td id="d29701e251">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select the helpful icon \(![Helpful icon.](../../customer-service-management/image/icon-helpful.png)\). If you think that the summary wasn’t helpful, select the not helpful icon \(![Not helpful icon.](../../customer-service-management/image/icon-not-helpful.png)\).This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d29701e274">

**Copy the case summary**

</td><td>

Select the copy to clipboard icon \(![Copy to clipboard icon.](../../customer-service-management/image/icon-copy.png)\) to use the case summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d29701e290">

**Refresh the case summary**

</td><td>

Select the refresh icon \(![Refresh icon.](../image/icon-refresh.png)\) to reload the case summary with any new information that was added to the case.

</td></tr><tr><td id="d29701e305">

**View the information about the case summary**

</td><td>

If you want to check some details about the summary, select the more info icon \(![More info icon.](../../customer-service-management/image/icon-more-info.png)\).

</td></tr></tbody>
</table>
**Parent Topic:**[Using Now Assist for Financial Services Operations \(FSO\)](../concept/using-now-assist-for-financial-services-operations-fso.md)

