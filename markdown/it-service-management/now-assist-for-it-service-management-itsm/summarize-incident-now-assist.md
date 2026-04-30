---
title: Summarize an incident by using Now Assist for IT Service Management \(ITSM\)
description: Quickly understand the incident context and respond to a requester’s inquiries by using the incident summarization skill in the Now Assist for IT Service Management \(ITSM\) application.
locale: en-US
release: zurich
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Use generative AI skills, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Summarize an incident by using Now Assist for IT Service Management \(ITSM\)

Quickly understand the incident context and respond to a requester’s inquiries by using the incident summarization skill in the Now Assist for IT Service Management \(ITSM\) application.

## Before you begin

Role required: itil

## About this task

The Incident summarization skill is turned on by default. The skill will be automatically available to appropriate role users for the application.When new customers install a Now Assist product, designated skills are turned on automatically. For existing users who upgrade, there will be no change to the skill activation. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

An incident summary provides you with a concise summary of an incident. The summary is based on the incident state and is generated from the information that you enter in the following fields:

-   Short description
-   Description
-   State
-   Priority
-   Work notes
-   Additional comments
-   Resolution notes \(for a resolved incident\)

For information about the incident states, see [Life cycle of an Incident](../../incident-management/concept/c_IncidentManagementStateModel.md).

You can summarize an incident in Core UI and Service Operations Workspace for ITSM.

## Procedure

1.  In Core UI or Service Operations Workspace for ITSM, open an incident that is assigned to you.

2.  Select **Summarize**.

    ![Summarize action in the Overview tab.](../image/itsm-incident-summarize.png)

    -   In Core UI, the summary appears in a banner of the incident record.

        ![Incident summary in Core UI that specifies the issue and actions taken.](../image/incident-summary-core-ui.png)

    -   In Service Operations Workspace for ITSM, the summary is generated in the **Overview** tab.

        You can provide feedback by selecting the thumbs up or thumbs down icon. You can also share the summary using the **Share** button.

        ![Incident summary in Service Operations Workspace for ITSM that specifies the issue and actions taken.](../image/incident-summary-now-assist.png)

3.  When you're finished summarizing an incident, you can add it to the work notes, expand or collapse it, provide feedback, copy it, or view information about it.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d119758e215">

Option

</th><th align="left" id="d119758e218">

Procedure

</th></tr></thead><tbody><tr><td id="d119758e224">

**Save the summary information by adding it to the incident work notes**

</td><td>

1.  Select **Share as Work notes**.
2.  In the Share Incident summary as Work notes dialog box, edit the summary.
3.  Select **Save to Work notes**.


</td></tr><tr><td id="d119758e251">

**Expand or collapse the summary**

</td><td>

Select the expand card icon \(![expand card icon.](../image/icon-expand.png)\) to view the complete summary or the collapse card icon \(![collapse card icon.](../image/icon-collapse.png)\) to view a collapsed summary.

</td></tr><tr><td id="d119758e272">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select the helpful icon \(![Helpful icon.](../image/icon-helpful.png)\). If you think that the summary wasn’t helpful, select the not helpful icon \(![Not helpful icon.](../image/icon-not-helpful.png)\).**Note:** This feedback improves the generative AI model and can help to improve future versions of this skill.

</td></tr><tr><td id="d119758e295">

**Copy the incident summary**

</td><td>

If you want to reuse the summary, select the copy to clipboard icon \(![Copy to clipboard icon.](../image/icon-copy.png)\).

</td></tr><tr><td id="d119758e311">

**View the information about the incident summary**

</td><td>

If you want to check some details about the summary, select the more info icon \(![More info icon.](../image/icon-more-info.png)\).

</td></tr></tbody>
</table>
