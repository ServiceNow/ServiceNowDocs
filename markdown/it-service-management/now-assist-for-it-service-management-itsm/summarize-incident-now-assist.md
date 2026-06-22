---
title: Summarize an incident by using Now Assist for IT Service Management \(ITSM\)
description: Quickly understand the incident context and respond to a requester’s inquiries by using the incident summarization skill in the Now Assist for IT Service Management \(ITSM\) application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/now-assist-for-it-service-management-itsm/summarize-incident-now-assist.html
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

The Incident summarization skill is turned on by default. The skill will be automatically available to appropriate role users for the application.When new customers install a Now Assist product, designated skills are turned on automatically. For existing users who upgrade, there will be no change to the skill activation. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

An incident summary provides you with a concise summary of an incident. The summary is based on the incident state and is generated from the information that you enter in the following fields:

-   Short description
-   Description
-   State
-   Priority
-   Work notes
-   Additional comments
-   Resolution notes \(for a resolved incident\)

For information about the incident states, see [Life cycle of an Incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/incident-management/c_IncidentManagementStateModel.md).

You can summarize an incident in Core UI and Service Operations Workspace for ITSM.

## Procedure

1.  In Core UI or Service Operations Workspace for ITSM, open an incident that is assigned to you.

2.  Select **Summarize**.

    \[Omitted image "itsm-incident-summarize.png"\] Alt text: Summarize action in the Overview tab.

    -   In Core UI, the summary appears in a banner of the incident record.

        \[Omitted image "incident-summary-core-ui.png"\] Alt text: Incident summary in Core UI that specifies the issue and actions taken.

    -   In Service Operations Workspace for ITSM, the summary is generated in the **Overview** tab.

        You can provide feedback by selecting the thumbs up or thumbs down icon. You can also share the summary using the **Share** button.

        \[Omitted image "incident-summary-now-assist.png"\] Alt text: Incident summary in Service Operations Workspace for ITSM that specifies the issue and actions taken.

3.  When you're finished summarizing an incident, you can add it to the work notes, expand or collapse it, provide feedback, copy it, or view information about it.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d119912e215">

Option

</th><th align="left" id="d119912e218">

Procedure

</th></tr></thead><tbody><tr><td id="d119912e224">

**Save the summary information by adding it to the incident work notes**

</td><td>

1.  Select **Share as Work notes**.
2.  In the Share Incident summary as Work notes dialog box, edit the summary.
3.  Select **Save to Work notes**.


</td></tr><tr><td id="d119912e251">

**Expand or collapse the summary**

</td><td>

Select the expand card icon \(\[Omitted image "icon-expand.png"\] Alt text: expand card icon.\) to view the complete summary or the collapse card icon \(\[Omitted image "icon-collapse.png"\] Alt text: collapse card icon.\) to view a collapsed summary.

</td></tr><tr><td id="d119912e272">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select the helpful icon \(\[Omitted image "icon-helpful.png"\] Alt text: Helpful icon.\). If you think that the summary wasn’t helpful, select the not helpful icon \(\[Omitted image "icon-not-helpful.png"\] Alt text: Not helpful icon.\).**Note:** This feedback improves the generative AI model and can help to improve future versions of this skill.

</td></tr><tr><td id="d119912e295">

**Copy the incident summary**

</td><td>

If you want to reuse the summary, select the copy to clipboard icon \(\[Omitted image "icon-copy.png"\] Alt text: Copy to clipboard icon.\).

</td></tr><tr><td id="d119912e311">

**View the information about the incident summary**

</td><td>

If you want to check some details about the summary, select the more info icon \(\[Omitted image "icon-more-info.png"\] Alt text: More info icon.\).

</td></tr></tbody>
</table>
