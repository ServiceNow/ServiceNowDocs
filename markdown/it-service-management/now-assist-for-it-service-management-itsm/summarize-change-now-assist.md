---
title: Summarize a change request by using Now Assist for IT Service Management \(ITSM\)
description: Quickly capture the important details of a change request, including the current status, by using the change request summarization skill in the Now Assist for IT Service Management \(ITSM\) application.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Use generative AI skills, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Summarize a change request by using Now Assist for IT Service Management \(ITSM\)

Quickly capture the important details of a change request, including the current status, by using the change request summarization skill in the Now Assist for IT Service Management \(ITSM\) application.

## Before you begin

Role required: itil

## About this task

The Change summarization skill is turned on by default. The skill will be automatically available to appropriate role users for the application.When new customers install a Now Assist product, designated skills are turned on automatically. For existing users who upgrade, there will be no change to the skill activation. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

A change request summary provides you with a concise summary of a change request. The summary is based on the change request state and is generated from the information that you enter in the following fields:

-   Short description
-   Description
-   Work notes
-   Additional comments
-   Risk
-   Impact
-   Justification
-   Implementation plan
-   Risk and impact analysis
-   Test plan
-   Backout plan
-   Close code
-   Close notes
-   Service offering
-   State
-   Conflict status
-   Type

For information about the change request states, see [State progression for normal, standard, and emergency changes](../../change-management/concept/normal-standard-emergency-states.md).

You can summarize a change request in Core UI and Service Operations Workspace for ITSM.

## Procedure

1.  In Core UI or Service Operations Workspace for ITSM, open a change request that is assigned to you.

2.  Select **Summarize**.

    **Note:** The Summarize UI action isn’t available for the New or Canceled state.

    The summary appears in a banner on the change request record in Core UI.![Change summary in Core UI](../image/itsm-now-assist-change-summary-core-ui.png)

    The summary appears in the **Overview** tab on the change request record in Service Operations Workspace.

    ![Change summary in Service Operations Workspace](../image/itsm-now-assist-change-summary-workspace.png)

    You can provide feedback by selecting the thumbs up or thumbs down icon. You can also share the summary using the **Share** button.

3.  When you're finished summarizing a change request, you can add it to the work notes, expand or collapse it, provide feedback, copy it, or view information about it.

<table id="choicetable_c2n_fsz_xbc"><thead><tr><th align="left" id="d338506e228">

Option

</th><th align="left" id="d338506e231">

Procedure

</th></tr></thead><tbody><tr><td id="d338506e237">

**Save the summary information by adding it to the change request work notes**

</td><td>

1.  Select **Share as Work notes**.
2.  In the Share Change Request summary as Work notes dialog box, edit the summary.
3.  Select **Save to Work notes**.


</td></tr><tr><td id="d338506e264">

**Expand or collapse the summary**

</td><td>

Select the expand card icon \(![expand card icon.](../image/icon-expand.png)\) to view the complete summary or the collapse card icon \(![collapse card icon.](../image/icon-collapse.png)\) to view a collapsed summary.

</td></tr><tr><td id="d338506e285">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select the helpful icon \(![Helpful icon.](../image/icon-helpful.png)\). If you think that the summary wasn’t helpful, select the not helpful icon \(![Not helpful icon.](../image/icon-not-helpful.png)\).**Note:** This feedback improves the generative AI model and can help to improve future versions of this skill.

</td></tr><tr><td id="d338506e308">

**Copy the change request summary**

</td><td>

If you want to reuse the summary, select the copy to clipboard icon \(![Copy to clipboard icon.](../image/icon-copy.png)\).

</td></tr><tr><td id="d338506e324">

**View the information about the change request summary**

</td><td>

If you want to check some details about the summary, select the more info icon \(![More info icon.](../image/icon-more-info.png)\).

</td></tr></tbody>
</table>
