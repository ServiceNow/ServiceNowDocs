---
title: Summarize a legal request or matter by using Now Assist for Legal Service Delivery \(LSD\)
description: Generate a summary from the fields that you selected on the legal request or matter record and quickly understand the request context by using the Legal Request or Legal Matter summarization skill in the Now Assist for Legal Service Delivery \(LSD\) application.
locale: en-US
release: zurich
product: Now Assist for Legal Service Delivery
classification: now-assist-for-legal-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Now Assist, generative AI]
breadcrumb: [Use, Now Assist for Legal Service Delivery \(LSD\), Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Summarize a legal request or matter by using Now Assist for Legal Service Delivery \(LSD\)

Generate a summary from the fields that you selected on the legal request or matter record and quickly understand the request context by using the Legal Request or Legal Matter summarization skill in the Now Assist for Legal Service Delivery \(LSD\) application.

## Before you begin

Role required: sn\_lg\_gen\_ai.request\_fulfiller

## About this task

The Legal Request or Legal Matter summarization skill provides you with a concise summary of a legal request or legal matter, including the actions taken and resolution details. By viewing a summary, you can understand the context, refresh the summary, and post the summary to the work notes.

You can configure the variables of practice areas that you want to be considered as inputs for legal request or matter summarization by using the Now Assist application. To add variables, see [Configure variables for Now Assist summarization](configure-variables-for-now-assist-summarization.md).

The summarization skills are available in Legal Counsel Center and in Core UI.

-   In Legal Counsel Center, you use the Legal Request summary by Now Assist component to generate a summary. This component appears above the activity stream.

    **Note:** You can also generate a summary on demand from the Now Assist panel. For more information, see [Use the Now Assist for Legal Service Delivery \(LSD\) capabilities from the Now Assist panel](now-assist-request-gen-ai-cap.md).

-   In Core UI, you select the **Summarize** button on the legal request or matter record to generate a summary.

## Procedure

1.  Navigate to **Workspaces** &gt; **Legal Counsel Center** and open a legal request or matter.

2.  In the Legal Request summary by Now Assist component, select **Summarize**.

    The summary by Now Assist component appears above the activity stream.

    **Note:** Generating and displaying the summary may take several seconds.

3.  When you finish summarizing a record, you can add it to the work notes, expand or collapse it, provide feedback, copy it, or view information about it.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d497805e168">

Option

</th><th align="left" id="d497805e171">

Procedure

</th></tr></thead><tbody><tr><td id="d497805e177">

**Save the summary information by adding it to the work notes**

</td><td>

1.  Select **Share as Work notes**.
2.  In the Share to work notes dialog box, edit the summary.
3.  Select **Save to Work notes**.


</td></tr><tr><td id="d497805e204">

**Expand or collapse the summary**

</td><td>

Select the expand card icon \(![Expand card icon.](../../human-resources/image/icon-expand.png)\) or the collapse card icon \(![Collapse card icon.](../../human-resources/image/icon-collapse.png)\) to see more details or fewer summary details.

</td></tr><tr><td id="d497805e225">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select the helpful icon \(![Helpful icon.](../../human-resources/image/icon-helpful.png)\). If you think that the summary wasn’t helpful, select the not helpful icon \(![Not helpful icon.](../../human-resources/image/icon-not-helpful.png)\).This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d497805e248">

**Copy the summary**

</td><td>

Select the copy to clipboard icon \(![Copy to clipboard icon.](../../human-resources/image/icon-copy.png)\) to use the summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d497805e264">

**Refresh the summary**

</td><td>

Select the Refresh icon \(![Refresh icon.](../../legal-matter-management/image/refresh-list-icon.png)\) to summarize the request again.

</td></tr><tr><td id="d497805e279">

**View the information about the summary**

</td><td>

If you want to check some details about the summary, select the more info icon \(![More info icon.](../../human-resources/image/icon-more-info.png)\).

</td></tr><tr><td id="d497805e294">

**Elaborate**

</td><td>

Select elaborate to get more comprehensive summary with additional details.

</td></tr></tbody>
</table>
-   **[Use the Now Assist for Legal Service Delivery \(LSD\) capabilities from the Now Assist panel](now-assist-request-gen-ai-cap.md)**  
Use the contextual generative AI capabilities, such as a request summary by using the conversational interface in the Now Assist panel.

**Parent Topic:**[Using Now Assist for Legal Service Delivery \(LSD\)](../concept/now-assist-lsd-using.md)

