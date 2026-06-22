---
title: Generate summary for remote hands case record
description: Remote Hands Request Summarization is a capability that generates a contextual summary of a Remote Hands case by combining current case data with insights from similar historical cases, using information submitted by the DCIM user through the CSM portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/now-assist-for-telecom-media-and-technology/generate-summary-for-remote-hands-case-record.html
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2026-06-22"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Generate summary for remote hands case record

Remote Hands Request Summarization is a capability that generates a contextual summary of a Remote Hands case by combining current case data with insights from similar historical cases, using information submitted by the DCIM user through the CSM portal.

## Before you begin

Role required: Remote hands agent \(sn\_remote\_hands\_agent\)

## About this task

Remote Hands Request Summarization is an Now Assist capability that provides a contextual overview of a Remote Hands case by combining current case data with insights from similar historical cases. Users with the Remote Hands Agent role can generate a summarized view of a Remote Hands case by selecting the **Summarize** option from either the Remote Hands Case table or the CSM/FSM Configurable Workspace. The information displayed in the summary is populated from the data entered by the DCIM user in the Remote Hands case record through the Customer Service Management \(CSM\) portal.

The Case Overview section displays key metadata retrieved from the Remote Hands Case table, including Case Category, Priority, Channel, and State. The Case Details section displays the Short Description and Description fields from the Remote Hands case record, providing detailed context about the current request. The Related Case Summary section is generated based on similar cases from the related cases present in the remote hands case record. Within this section, the Case Reference lists up to five similar cases identified by the system, the Case Issue displays the Short Description of each related case, and the Case Resolution displays the Resolution Notes recorded in the related cases.

This skill available in CSM/FSM Configurable Workspace and in Core UI

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** &gt; **Lists** &gt; **Remote Hands Cases**.

2.  Select a case record to open and review the case details.

3.  Select **Summarize** to view the case summary.

    The summary includes the overview of the case, case details, and related case summary. Switch to the Related Cases tab to view the related cases.

4.  After you're finished summarizing a Remote Hands case, manage the results.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d25256e92">

Option

</th><th align="left" id="d25256e95">

Procedure

</th></tr></thead><tbody><tr><td id="d25256e101">

**View more or less summary details**

</td><td>

-   To see more details summary details, select the View more icon \(\[Omitted image "icon-expand.png"\] Alt text: Expand card icon.\).
-   To see fewer summary details, select the View less icon \(\[Omitted image "icon-collapse.png"\] Alt text: Collapse card icon.\).


</td></tr><tr><td id="d25256e131">

**Provide feedback for the summary**

</td><td>

-   If you think that the Remote Hands case summary was helpful, select the helpful icon \(\[Omitted image "icon-helpful.png"\] Alt text: Helpful icon.\).
-   If you think that the summary wasn’t helpful, select the not helpful icon \(\[Omitted image "icon-not-helpful.png"\] Alt text: Not helpful icon.\).
 This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d25256e164">

**Copy the case summary**

</td><td>

Select the copy to clipboard icon \(\[Omitted image "icon-copy.png"\] Alt text: Copy to clipboard icon.\) to use the Remote Hands case summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d25256e179">

**View the information about the case summary**

</td><td>

To check some details about the summary, select the more info icon \(\[Omitted image "icon-more-info.png"\] Alt text: More info icon.\).

</td></tr></tbody>
</table>
**Parent Topic:**[Using Now Assist for Telecommunications, Media and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-spm-using.md)

