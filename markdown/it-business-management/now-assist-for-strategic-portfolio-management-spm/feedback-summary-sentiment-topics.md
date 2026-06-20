---
title: Summarize the feedback by using Now Assist for Strategic Portfolio Management \(SPM\)
description: Generate a summary from the name and description of the feedback records so that you can analyze a large volume of feedback quickly without reading each feedback record manually. You can do this task by using the multi feedback summarization skill in the Now Assist for Strategic Portfolio Management \(SPM\) application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/now-assist-for-strategic-portfolio-management-spm/feedback-summary-sentiment-topics.html
release: zurich
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [Feedback summarization, Multi summarization skill, Summarize feedback]
breadcrumb: [Using Now Assist for Strategic Portfolio Management \(SPM\), Now Assist for Strategic Portfolio Management \(SPM\), Strategic Portfolio Management]
---

# Summarize the feedback by using Now Assist for Strategic Portfolio Management \(SPM\)

Generate a summary from the name and description of the feedback records so that you can analyze a large volume of feedback quickly without reading each feedback record manually. You can do this task by using the multi feedback summarization skill in the Now Assist for Strategic Portfolio Management \(SPM\) application.

Multi feedback summarization video.

## Before you begin

**Important:** This Now Assist skill is now turned on by default. The skill will be automatically available to appropriate role users for the application. This change simply activates the skill and does not touch the roles that are needed to use the skill. The new default behavior works as follows:

-   **New customers**

    When you install a Now Assist product, designated skills will turn on automatically.

-   **Existing customers who are upgrading**

    Any previously unconfigured skill will turn on automatically \(the skill was never turned on, then off again\).

    There is no change to Now Assist skills that are currently enabled and customized.

    Previously configured skills that were turned on, then off, will remain inactive.


If you have users with custom roles that need access to this skill, you must update ACLs for those roles and also add those custom roles to the In product role.

Role required: pf\_user

## About this task

With the feedback or multi feedback summarization skill, you can get enough details about the feedback that you received on your product so that you can improve the product features, usability, and performance.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** and select **Feedback**.

2.  From the Feedback page, select any feedback filter card.

3.  From the feedback list, select one or multiple feedback records.

    View a loader for the side panel while the summary content loads for a more engaging loading experience.

    If you want to generate a summary for one feedback record, you can either generate it from the list level or at the record level. At the record level, the feedback summary is displayed in the Now Assist component. The component is collapsed by default and expands to display the summary.

4.  Select **Summarize**.

    View an animation for the Now assist icon when you hover over it.

    You can generate a summary of a single feedback record by using the feedback summarization skill. This image shows the AI-generated summary for a single feedback record.

    \[Omitted image "single-feedback-summarization-screen.png"\] Alt text: AI-generated summary for a single feedback record using feedback summarization skill.

    You can use the multi feedback summarization skill to generate summaries of one or multiple feedback records. For example, you can analyze the high-priority feedback, filter them, summarize the records, and gain insights into the requirements.

    \[Omitted image "multi-feedback-summarization-example.png"\] Alt text: AI-generated summary for multiple feedback records using the multi feedback summarization skill.

    **Note:** Because the information in these fields is automatically generated, it's a good idea to review the text and make sure it's accurate.

    The feedback or multi feedback summarization skill uses the name and description information of the feedback record to generate a paragraph or bullet-point summary from the feedback.

    View the hover animation for the Now Assist icon on the Summarize button in the feedback list and Docs.

5.  When you're finished summarizing the feedback, you can expand or collapse the summary, provide feedback, copy it, or view information about it.

<table id="choicetable_mzf_fyg_y1c"><thead><tr><th align="left" id="d88450e197">

Option

</th><th align="left" id="d88450e200">

Procedure

</th></tr></thead><tbody><tr><td id="d88450e206">

**Expand or collapse the summary**

</td><td>

Select the expand card icon \(\[Omitted image "icon-expand-spm.png"\] Alt text: Expand card icon.\) or the collapse card icon \(\[Omitted image "icon-collapse-spm.png"\] Alt text: Collapse card icon.\) to see more details or fewer summary details.

</td></tr><tr><td id="d88450e227">

**More information on summary**

</td><td>

If you want to check some details about the summary, select the more info icon \(\[Omitted image "icon-more-information-spm.png"\] Alt text: More information icon.\).

</td></tr><tr><td id="d88450e242">

**View more or less summary**

</td><td>

Select **View more** or **View less** to see more or less summary information.

</td></tr><tr><td id="d88450e257">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select the helpful icon \(\[Omitted image "icon-helpful-feedback.png"\] Alt text: Helpful icon.\). If you think that the summary wasn’t helpful, select the not helpful icon \(\[Omitted image "icon-nt-helpful.png"\] Alt text: Not helpful icon.\).This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d88450e281">

**Copy the feedback summary**

</td><td>

Select the copy to clipboard icon \(\[Omitted image "icon-copy-spm.png"\] Alt text: Copy to clipboard icon.\) to use the feedback summary information for another purpose, such as pasting it into an email.

</td></tr><tr><td id="d88450e296">

**Refresh the summary**

</td><td>

Select **Refresh** to reload the feedback summary.

</td></tr><tr><td id="d88450e308">

**Copy and create epic from summary**

</td><td>

Select **Copy and create epic** to create a planning or non-planning item by using the feedback summary.

</td></tr></tbody>
</table>    **Note:** The feedback summarization or multi summarization skill checks the feedback records to determine if enough information is available to generate a summary. If there isn't enough feedback content to summarize, you can add more content and retry.

    On the side panel, you can select the preview record icon \(\[Omitted image "preview-record-icon.png"\] Alt text: preview record icon.\) to view the additional details or select preview generated summary icon \(\[Omitted image "preview-generated-summary-icon.png"\] Alt text: Preview generated summary icon.\) to view the summarization output.

6.  Select **Copy and create epic** to copy the generated summary and create a planning item.

    Save time and streamline your work flow by linking the feedback with planning items, which eliminates the need to copy summaries. You can quickly create work items in Feedback and view them in the roadmap.


**Parent Topic:**[Using Now Assist for Strategic Portfolio Management \(SPM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/now-assist-for-strategic-portfolio-management-spm/using-now-assist-for-spm.md)

