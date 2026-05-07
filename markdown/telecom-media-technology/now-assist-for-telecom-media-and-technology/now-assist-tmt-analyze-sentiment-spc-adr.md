---
title: Analyze the sentiment of a service problem case using Now Assist for TMT
description: Generates the requester's sentiment and the reasoning behind it on the complaint cases in the Now Assist for TMT application. Make informed decisions on complaint cases based on sentiment to link the cases on the Alternative Dispute Resolution \(ADR\) case record.
locale: en-US
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use generative AI skills, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Analyze the sentiment of a service problem case using Now Assist for TMT

Generates the requester's sentiment and the reasoning behind it on the complaint cases in the Now Assist for TMT application. Make informed decisions on complaint cases based on sentiment to link the cases on the Alternative Dispute Resolution \(ADR\) case record.

## Before you begin

Role required: sn\_telco\_adr\_mgmt.manager

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** &gt; **Lists** &gt; **Alternative Dispute Resolution** &gt; **All**.

2.  Open the ADR case that you are working on.

3.  Select Investigate stage.

4.  On the Lookup record history activity, under the Relevant record section, navigate to the complaint cases.

5.  Select the information icon \(![More info icon.](../image/icon-more-info.png)\).

    The Customer sentiment component appears and provides an explanation for why that sentiment was given.

    The Customer Sentiment component shows the assigned sentiment and explains why that sentiment was given.

    **Note:** Generating and displaying the summary may take several seconds.

6.  After you're finished analyzing the sentiment, manage the results.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d30554e133">

Option

</th><th align="left" id="d30554e136">

Procedure

</th></tr></thead><tbody><tr><td id="d30554e142">

**Provide feedback for the summary**

</td><td>

-   If you think that the sentiment information was helpful, select the helpful icon \(![Helpful icon.](../image/icon-helpful.png)\).
-   If you think that the sentiment information wasn’t helpful, select the not helpful icon \(![Not helpful icon.](../image/icon-not-helpful.png)\).
 This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated sentiment information and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr></tbody>
</table>
## What to do next

Complete the remaining steps to execute the ADR case record. To learn more, see [Create an Alternative Dispute Resolution case](create-adr-case-record.md).

**Parent Topic:**[Using Now Assist for Telecommunications, Media and Technology \(TMT\)](../concept/now-assist-spm-using.md)

