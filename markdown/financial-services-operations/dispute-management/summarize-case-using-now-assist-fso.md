---
title: Summarize a dispute or claims case with case summarization
description: Generate a summary from the defined fields on the case record and quickly understand the case context by using the case summarization skill in the ServiceNow Otto for Financial Services Operations \(FSO\) application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/summarize-case-using-now-assist-fso.html
release: brazil
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 3
keywords: [generative AI for financial services operations generate summary, generative AI for FSO generate summary]
breadcrumb: [Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Summarize a dispute or claims case with case summarization

Generate a summary from the defined fields on the case record and quickly understand the case context by using the case summarization skill in the ServiceNow Otto for Financial Services Operations \(FSO\) application.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent, sn\_bom\_credit\_card.dispute\_manager, sn\_bom\_credit\_card.dispute\_viewer, sn\_bom\_credit\_card.contributor, sn\_bom.b2c\_agent, sn\_bom.b2b\_agent, sn\_bom.adjuster, sn\_bom.fnol\_representative

**Note:** These roles are the default list of roles that are defined for this task. Administrators can modify the list of roles in the AI Admin Hub console.

## About this task

The case summarization skill provides you with a concise summary of a banking card dispute or insurance claims case. With this skill, you can do the following tasks:

-   Generate an initial summary of a case so that you can understand the case context.
-   Summarize the actions taken and any resolutions for a case.

The case summarization skill is available in Financial Services Workspace and in Core UI.

-   In Financial Services Workspace, use the Case summary by Now Assist component to generate a summary. The component appears in the following areas:
    -   Insurance: Next to the claim details panel.
        -   Claims processor: On the Claim Summary tab
        -   Claims adjuster: On the Claim Workspace and Claim Summary tabs
    -   Card dispute: Next to the case information panel.
-   In Core UI, select the **Summarize** button on the case record to generate a summary.

The case summarization skill checks the case record to determine if enough information is available to create a summary:

-   When an agent opens the case record.
-   When an agent refreshes the case record page.

If there’s enough data, the Case summary component displays the **Summarize** button. If there isn’t enough data, the component displays a message in place of the button.

**Note:** The generated summary is intended for informational purposes only. Review AI-generated summaries for accuracy and appropriateness before you rely on them.

## Procedure

1.  Navigate to **Workspaces** &gt; **Financial Services Workspace** and open a claim or card dispute.

2.  In the Case Summary component, select **Summarize**.

    \[Omitted image "now-assist-fso-summarize-dispute.png"\] Alt text: Selecting Summarize generates a case summary for the dispute or claims case.

    Before you generate a summary, the component displays **AI can summarize this claim case** or **AI can summarize your dispute** next to the **Summarize** button.

    When the summary is generated, the Case Summary component expands to display the summary. For longer summaries that don't fit the window, select **Show more** and use the scroll bar to view the rest of the content.

    **Note:** Generating and displaying the summary may take several seconds.

    \[Omitted image "now-assist-fso-dispute-summary.png"\] Alt text: The format of a generated summary for a dispute case.

3.  When you're finished summarizing a case, you can perform additional actions.

<table id="choicetable_ybr_pjr_mbc"><thead><tr><th align="left" id="d35268e299">

Option

</th><th align="left" id="d35268e302">

Procedure

</th></tr></thead><tbody><tr><td id="d35268e308">

**Save the summary information by adding it to the case work notes**

</td><td>

1.  Select **Share**.
2.  In the Share to work notes dialog box, review the summary for accuracy and edit if required.
3.  Select **Save to work notes**. Alternatively, select **Cancel** to close the dialog box without saving.


</td></tr><tr><td id="d35268e361">

**Expand or collapse the summary**

</td><td>

Select the expand card icon \(\[Omitted image "icon-expand.png"\] Alt text: Expand card icon.\) or the collapse card icon \(\[Omitted image "icon-collapse.png"\] Alt text: Collapse card icon.\) to see more details or fewer summary details.

</td></tr><tr><td id="d35268e382">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select the helpful icon \(\[Omitted image "icon-helpful.png"\] Alt text: Helpful icon.\). If you think that the summary wasn’t helpful, select the not helpful icon \(\[Omitted image "icon-not-helpful.png"\] Alt text: Not helpful icon.\).This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d35268e405">

**Copy the case summary**

</td><td>

Select the copy to clipboard icon \(\[Omitted image "icon-copy.png"\] Alt text: Copy to clipboard icon.\) to use the case summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d35268e421">

**Refresh the case summary**

</td><td>

Select the refresh icon \(\[Omitted image "icon-refresh.png"\] Alt text: Refresh icon.\) to reload the case summary with any new information that was added to the case.

</td></tr></tbody>
</table>
**Parent Topic:**[Managing Disputes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/dispute-management/managing-disputes.md)

