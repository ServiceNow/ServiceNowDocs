---
title: View CI information with the Now Assist CI summarization skill
description: View a concise summary of key CI data. You can select the CI on a CI form, in a workspace page, or on any list view. The summary can include discovery data, ownership, and key related items such as open incidents, alerts, problems, upcoming change requests, and security vulnerabilities. Additionally, the summary lists the service instances that the CI is part of.
locale: en-US
release: yokohama
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-02-06"
reading_time_minutes: 1
breadcrumb: [Use generative AI skills, Now Assist for Configuration Management Database \(CMDB\), CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View CI information with the Now Assist CI summarization skill

View a concise summary of key CI data. You can select the CI on a CI form, in a workspace page, or on any list view. The summary can include discovery data, ownership, and key related items such as open incidents, alerts, problems, upcoming change requests, and security vulnerabilities. Additionally, the summary lists the service instances that the CI is part of.

## Before you begin

Role required: sn\_cmdb\_user

## About this task

This procedure describes how you can manually access the skill in Core UI or in the CMDB Workspace. In addition, any agentic workflow can use the skill.

## Procedure

1.  Select a CI from the workspace or from any list view.

    For example, select **All** and enter `cmdb_ci.list` in the search filter. Select a CI to open its CI form.

2.  Select **Summarize** in the Now Assist box.

    ![Summarize button on the CI form.](../image/na-cmdb-summarize-button.png)

    Now Assist generates and displays summary information for the CI, as in this example.

    ![Summary information.](../image/na-cmdb-ci-summary-example.png)

3.  Provide feedback, copy the summary text to the clipboard, or refresh the summary.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d345927e139">

Option

</th><th align="left" id="d345927e142">

Procedure

</th></tr></thead><tbody><tr><td id="d345927e148">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select thumbs-up ![](../../configuration-management/image/icon-thumbs-up.png). If you think that the summary wasn’t helpful, select thumbs-down ![](../../configuration-management/image/icon-thumbs-down.png).This feedback improves the Agentic AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the Agentic AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d345927e163">

**Copy the summary**

</td><td>

Select the copy to clipboard icon ![](../../configuration-management/image/icon-clipboard.png) to use the summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d345927e175">

**Refresh the summary**

</td><td>

If you think that data might have changed after you viewed the summary, select the redo icon ![](../../configuration-management/image/icon-redo.png) to refresh the summary information.

</td></tr></tbody>
</table>
**Related topics**  


[Configure the CI summarization skill](../../configuration-management/task/now-assist-cmdb-config-ci-summary.md)

