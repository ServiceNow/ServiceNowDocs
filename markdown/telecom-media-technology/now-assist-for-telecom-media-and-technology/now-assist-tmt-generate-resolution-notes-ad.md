---
title: Generate resolution notes for ADR case
description: Generate the resolution notes for an Alternative Dispute Resolution \(ADR\) case by using the resolution notes generation for ADR skill in the Now Assist for TMT application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-generate-resolution-notes-ad.html
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Generate resolution notes for ADR case

Generate the resolution notes for an Alternative Dispute Resolution \(ADR\) case by using the resolution notes generation for ADR skill in the Now Assist for TMT application.

## Before you begin

Role required: sn\_telco\_adr\_mgmt.manager

## About this task

The resolution notes generation for ADR skill enables you to generate resolution for the customer dispute in the ADR case record. You can propose this resolution to the customer and get the customer feedback.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** &gt; **Lists** &gt; **Alternative Dispute Resolution** &gt; **All**.

2.  Open the ADR case that you're working on.

3.  Select Resolution stage.

4.  In the Propose resolution plan activity, navigate to the **Resolution notes** field.

5.  Select the Now Assist icon \(\[Omitted image "icon-ai-sparkle.png"\] Alt text: Now Assist Icon.\).

    The Now Assist component appears and displays the resolution plan.

    **Note:** Generating and displaying the details may take several seconds.

6.  After you're finished summarizing the key findings, manage the results.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d25005e138">

Option

</th><th align="left" id="d25005e141">

Procedure

</th></tr></thead><tbody><tr><td id="d25005e147">

**Provide feedback for the summary**

</td><td>

-   If you think that the resolution plan was helpful, select the helpful icon \(\[Omitted image "icon-helpful.png"\] Alt text: Helpful icon.\).
-   If you think that the resolution plan wasn’t helpful, select the not helpful icon \(\[Omitted image "icon-not-helpful.png"\] Alt text: Not helpful icon.\).
 This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d25005e180">

**Copy the case summary**

</td><td>

Select the copy to clipboard icon \(\[Omitted image "icon-copy.png"\] Alt text: Copy to clipboard icon.\) to use the resolution plan for another purpose, such as pasting into an email.

</td></tr><tr><td id="d25005e195">

**View the information about the case summary**

</td><td>

To check some details about the resolution plan, select the more info icon \(\[Omitted image "icon-more-info.png"\] Alt text: More info icon.\).

</td></tr></tbody>
</table>7.  Select **Insert** to add the generated content to the **Resolution notes** field.


## What to do next

Complete the remaining steps to execute the ADR case record. To learn more, see [Create an Alternative Dispute Resolution case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/create-adr-case-record.md).

**Parent Topic:**[Using Now Assist for Telecommunications, Media and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-spm-using.md)

