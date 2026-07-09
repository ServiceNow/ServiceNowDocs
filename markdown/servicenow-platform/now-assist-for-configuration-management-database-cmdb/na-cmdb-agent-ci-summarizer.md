---
title: View CI information with the Now Assist CI summarization skill
description: View a concise summary of key CI data. You can select the CI on a CI form, in a workspace page, or on any list view. The summary can include discovery data, ownership, and key related items such as open incidents, alerts, problems, upcoming change requests, and security vulnerabilities. Additionally, the summary lists the service instances that the CI is part of.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-agent-ci-summarizer.html
release: zurich
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2025-10-17"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View CI information with the Now Assist CI summarization skill

View a concise summary of key CI data. You can select the CI on a CI form, in a workspace page, or on any list view. The summary can include discovery data, ownership, and key related items such as open incidents, alerts, problems, upcoming change requests, and security vulnerabilities. Additionally, the summary lists the service instances that the CI is part of.

## Before you begin

Role required: sn\_cmdb\_user

## About this task

This procedure describes how you can manually access the skill in Core UI or in the CMDB Workspace. In addition, any agentic workflow can use the skill.

For more information, see [Working in the Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md).

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

## Procedure

1.  Select a CI from the workspace or from any list view.

    For example, select **All** and enter `cmdb_ci.list` in the search filter. Select a CI to open its CI form.

2.  Select **Summarize** in the Now Assist box.

    \[Omitted image "na-cmdb-summarize-button.png"\] Alt text: Summarize button on the CI form.

    Now Assist generates and displays summary information for the CI, as in this example.

    \[Omitted image "na-cmdb-ci-summary-example.png"\] Alt text: Summary information.

3.  Provide feedback, copy the summary text to the clipboard, or refresh the summary.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d392493e156">

Option

</th><th align="left" id="d392493e159">

Procedure

</th></tr></thead><tbody><tr><td id="d392493e165">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select thumbs-up \[Omitted image "icon-thumbs-up.png"\]. If you think that the summary wasn’t helpful, select thumbs-down \[Omitted image "icon-thumbs-down.png"\].This feedback improves the Agentic AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the Agentic AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d392493e180">

**Copy the summary**

</td><td>

Select the copy to clipboard icon \[Omitted image "icon-clipboard.png"\] to use the summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d392493e192">

**Refresh the summary**

</td><td>

If you think that data might have changed after you viewed the summary, select the redo icon \[Omitted image "icon-redo.png"\] to refresh the summary information.

</td></tr></tbody>
</table>
**Related topics**  


[Configure the CI summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-config-ci-summary.md)

