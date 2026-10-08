---
title: Generate summary for remote hands case record
description: Remote Hands Request Summarization generates a contextual summary of a Remote Hands case. It combines current case data with insights from similar historical cases using information submitted through the CSM portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-network-inventory/telecommunications-network-inventory/summerizing-remote-hands-case.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-10-08"
reading_time_minutes: 2
breadcrumb: [Use, Telecommunications Network Inventory]
---

# Generate summary for remote hands case record

Remote Hands Request Summarization generates a contextual summary of a Remote Hands case. It combines current case data with insights from similar historical cases using information submitted through the CSM portal.

## Before you begin

Role required: Remote hands agent \(sn\_remote\_hands\_agent\)

## About this task

Remote Hands Request Summarization is an ServiceNow Otto capability that provides a contextual overview of a Remote Hands case. It combines current case data with insights from similar historical cases. Users with the Remote Hands Agent role can generate a summarized view of a Remote Hands case by selecting the **Summarize** option. This option is available from either the Remote Hands Case table or the CSM/FSM Configurable Workspace. The information displayed in the summary is populated from the data entered by the DCIM user in the Remote Hands case record. This data is submitted through the Customer Service Management \(CSM\) portal.

The Case Overview section displays key metadata retrieved from the Remote Hands Case table, including Case Category, Priority, Channel, and State. The Case Details section displays the Short Description and Description fields from the Remote Hands case record, providing detailed context about the current request. The Related Case Summary section is generated based on similar cases from the related cases present in the remote hands case record. Within this section, the Case Reference lists up to five similar cases identified by the system. The Case Issue displays the Short Description of each related case. The Case Resolution displays the Resolution Notes recorded in the related cases.

This skill available in CSM/FSM Configurable Workspace and in Core UI

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** &gt; **Lists** &gt; **Remote Hands Cases**.

2.  Select a case record to open and review the case details.

3.  Select **Summarize** to view the case summary.

    The summary includes the overview of the case, case details, and related case summary. Switch to the Related Cases tab to view the related cases.

4.  After you're finished summarizing a Remote Hands case, manage the results.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d76136e92">

Option

</th><th align="left" id="d76136e95">

Procedure

</th></tr></thead><tbody><tr><td id="d76136e101">

**View more or less summary details**

</td><td>

-   To see more details summary details, select the View more icon \(\).
-   To see fewer summary details, select the View less icon.


</td></tr><tr><td id="d76136e119">

**Provide feedback for the summary**

</td><td>

-   If you think that the Remote Hands case summary was helpful, select the helpful icon \).
-   If you think that the summary wasn’t helpful, select the not helpful icon.
 This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d76136e142">

**Copy the case summary**

</td><td>

Select the copy to clipboard icon to use the Remote Hands case summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d76136e151">

**View the information about the case summary**

</td><td>

To check some details about the summary, select the more info icon.

</td></tr></tbody>
</table>
**Parent Topic:**[Using Telecommunications Network Inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-network-inventory/telecommunications-network-inventory/using-telecom-network-inventory.md)

