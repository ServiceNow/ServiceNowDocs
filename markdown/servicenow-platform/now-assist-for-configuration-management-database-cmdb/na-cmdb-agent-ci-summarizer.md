---
title: Use the Now Assist CI summarizer AI agent
description: View a concise summary of key configuration item \(CI\) data directly on a CI form, in the workspace, or from any list. The summary can include discovery and class details, associated business services, security vulnerabilities, and related records like incidents, alerts, problems, and change requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-agent-ci-summarizer.html
release: xanadu
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2025-04-16"
reading_time_minutes: 1
breadcrumb: [Using Now Assist for CMDB, Now Assist for Configuration Management Database \(CMDB\), CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Use the Now Assist CI summarizer AI agent

View a concise summary of key configuration item \(CI\) data directly on a CI form, in the workspace, or from any list. The summary can include discovery and class details, associated business services, security vulnerabilities, and related records like incidents, alerts, problems, and change requests.

## Before you begin

Role required: sn\_cmdb\_user

## About this task

The agent is available in Core UI or in the CMDB Workspace.

Like all agents, the agent is available for use by any agentic workflow. In addition, you can use the agent manually as described in this procedure.

## Procedure

1.  Select a CI from the workspace or from any list.

    For example, select **All** and enter `cmdb_ci.list` in the search filter. Select a CI to open its CI form.

2.  Select **Summarize**.

    \[Omitted image "na-cmdb-summarize-button.png"\] Alt text: Summarize button on the CI form.

    Now Assist generates and displays summary information for the CI, as in this example.

    \[Omitted image "na-cmdb-ci-summary-example.png"\] Alt text: Summary information.

3.  Provide feedback, copy the summary text to the clipboard, or refresh the summary.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d355103e133">

Option

</th><th align="left" id="d355103e136">

Procedure

</th></tr></thead><tbody><tr><td id="d355103e142">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select thumbs-up \[Omitted image "icon-thumbs-up.png"\] Alt text: thumbs up icon. If you think that the summary wasn’t helpful, select thumbs-down \[Omitted image "icon-thumbs-down.png"\] Alt text: thumbs down icon.This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d355103e165">

**Copy the summary**

</td><td>

Select the copy to clipboard icon \[Omitted image "icon-clipboard.png"\] Alt text: copy to clipboard icon to use the summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d355103e180">

**Refresh the summary**

</td><td>

If you think that data might have changed after you viewed the summary, select the redo icon \[Omitted image "icon-redo.png"\] Alt text: redo icon to refresh the summary information.

</td></tr></tbody>
</table>
