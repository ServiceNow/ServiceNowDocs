---
title: Summarize a safety incident by using Now Assist for Health and Safety
description: Generate a summary from the fields that you selected on the safety incident and quickly understand the incident context by using the Health and Safety incident summarization skill in the Now Assist for Health and Safety application.
locale: en-US
release: australia
product: Now Assist for Health and Safety
classification: now-assist-for-health-and-safety
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Now Assist for Health and Safety, Health and Safety, Employee Service Management]
---

# Summarize a safety incident by using Now Assist for Health and Safety

Generate a summary from the fields that you selected on the safety incident and quickly understand the incident context by using the Health and Safety incident summarization skill in the Now Assist for Health and Safety application.

## Before you begin

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

Verify that the Health and Safety incident summarization skill is enabled. For more information, see [Activate a Now Assist for Health and Safety skill](now-assist-hs-activate-skill.md).

Role required: sn\_ohs\_im.agent or sn\_ohs\_im.manager

## About this task

The Health and Safety incident summarization skill provides the summary of Health and Safety incidents including the details, actions taken, and root cause analysis. The safety agent and safety manager can view a summary to understand the context, refresh the summary, and post the summary to the work notes.

The incident summarization skill is available in Health and Safety Workspace and in the Core UI. When this skill is enabled on an instance, the Now Assist icon \(![now assist icon](../image/na-hs-panel-icon.png)\) appears in the workspace.

-   In Health and Safety Workspace, use the Health and Safety incident summary by Now Assist component to generate a summary. This component appears above the activity stream.

    **Note:** You can also generate a summary on demand from the Now Assist panel. For more information, see [Standard chat](https://www.servicenow.com/docs/access?context=now-assist-panel-standard&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

-   In the Core UI, select the **Summarize** button on the incident record to generate a summary.

## Procedure

1.  Navigate to **Workspaces** &gt; **Health and Safety Workspace** and open a safety incident.

2.  Select **Activity** to open the activity stream.

3.  In the Health and Safety incident summary by Health and Safety component, select **Summarize**.

    **Note:** Generating and displaying the summary may take several seconds.

    ![AI-generated incident summarization](../image/na-hs-incident-summarization.png "Safety incident summary")

4.  When you're finished summarizing an incident, you can add it to the incident work notes, expand or collapse it, provide feedback, copy it, or view information about the incident.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d304011e232">

Option

</th><th align="left" id="d304011e235">

Procedure

</th></tr></thead><tbody><tr><td id="d304011e241">

**Save the summary information by adding it to the work notes**

</td><td>

1.  Select **Share as work notes**.
2.  In the Share to work notes dialog box, edit the summary.
3.  Select **Save to work notes**.


</td></tr><tr><td id="d304011e268">

**Expand or collapse the summary**

</td><td>

Select the expand card icon \(![Expand card icon.](../../human-resources/image/icon-expand.png)\) or the collapse card icon \(![Collapse card icon.](../../human-resources/image/icon-collapse.png)\) to see more details or fewer summary details.

</td></tr><tr><td id="d304011e289">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select the helpful icon \(![Helpful icon.](../../human-resources/image/icon-helpful.png)\). If you think that the summary wasn’t helpful, select the not helpful icon \(![Not helpful icon.](../../human-resources/image/icon-not-helpful.png)\).This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d304011e312">

**Copy the case summary**

</td><td>

Select the copy to clipboard icon \(![Copy to clipboard icon.](../../human-resources/image/icon-copy.png)\) to use the case summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d304011e328">

**Refresh the summary**

</td><td>

Select the refresh icon \(![Refresh icon.](../../legal-matter-management/image/refresh-list-icon.png)\) to summarize the request again.

</td></tr><tr><td id="d304011e343">

**View the information about the case summary**

</td><td>

If you want to check details about the summary, select the more info icon \(![More info icon.](../../human-resources/image/icon-more-info.png)\).

</td></tr></tbody>
</table>5.  Share the AI-generated summary with relevant stakeholders through the **Email** tab in the activity stream.

    The **Email** tab appears only when the following conditions are met:

    -   The email client is enabled for the Health and Safety incident \[sn\_ohs\_im\_incident\] table on your ServiceNow instance. For more information, see [Enable the email client for a table](https://www.servicenow.com/docs/access?context=enable-email-client&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
    -   The user sending the email has the Email composer \[email\_composer\] role. For more information, see [Email composer \[email\_composer\]](https://www.servicenow.com/docs/access?context=email-client-roles-2&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

