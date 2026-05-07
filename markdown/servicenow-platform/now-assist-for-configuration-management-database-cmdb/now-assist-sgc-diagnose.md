---
title: Fix SGC import set issues with the Now Assist SGC diagnosis skill
description: To reduce debugging and resolution time and effort, the Service Graph Connector diagnosis skill generates summaries of errors and recommendations for resolving processing errors with SGC import sets.
locale: en-US
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Use generative AI skills, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Fix SGC import set issues with the Now Assist SGC diagnosis skill

To reduce debugging and resolution time and effort, the Service Graph Connector diagnosis skill generates summaries of errors and recommendations for resolving processing errors with SGC import sets.

## Before you begin

Enable the Service Graph Connector diagnosis skill as described in [Configure the Service Graph Connector diagnosis skill](now-assist-cmdb-config-sgc-diagnose.md).

Role required: cmdb\_inst\_admin and now\_assist\_panel\_user

## About this task

This procedure describes how you can manually access the skill. In addition, any agentic workflow can use the skill.

When a Now Assist skill is enabled, the Now Assist icon ![](../../../administer/virtual-agent/images/icon-now-assist-sparkle.png) appears in the toolbar of the workspace. For more information, see [Working in the Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Graph Workspace** or **Workspaces** &gt; **CMDB Workspace**.

2.  Select the Now Assist icon ![](../image/now-assist-sgc-ai.png) to open the Now Assist panel and then select or enter **Diagnose a Service Graph Connector**.

    ![Diagnose a Service Graph Connector in the Now Assist panel.](../image/now-assist-sgc-diagnose.png)

3.  Begin the diagnostic process by entering the connector name, specific data source, or import-set number of a Service Graph Connector.

    **Note:** If Now Assist doesn't recognize the entered text, it displays a list of the Service Graph Connectors installed on your instance by their discovery source names, such as `SG-Infoblox`. You can then select a connector for further diagnosis.

<table id="choicetable_x5w_r4d_zcc"><thead><tr><th align="left" id="d201391e206">

Option

</th><th align="left" id="d201391e209">

Description

</th></tr></thead><tbody><tr><td id="d201391e215">

**Connector name**

</td><td>

Service Graph Connector name to diagnose.The Now Assist for SGC displays the connector name in the discovery source format, such as `SG-Infoblox`. However, you can enter any text that is associated with the connector name, for example, `Service Graph Connector for Infoblox`, `Infoblox`, or `SG-Infoblox`.

After you enter a connector name, you can select a data source that is associated with the connector, followed by a failed import set that is associated with the data source. Based on the inputs, the latest failed import set number is displayed. Alternatively, you can select to view other failed import sets, if available. If no failed import sets are available, you can enter a different connector name, data source, or import set number.

![Diagnosing a failed import set with a connector name.](../image/now-assist-sgc-diagnose-connector.png)

</td></tr><tr><td id="d201391e251">

**Data source name**

</td><td>

Data source name for a connector to diagnose. For example, `SG-Infoblox IP Address`.After entering a data source that is associated with a connector, you can select a failed import set that is associated with the data source. Based on the inputs, the import set number that was last processed with errors is displayed. Alternatively, you can choose to view other failed import sets. If no failed import sets are available, you can select a different data source for the connector.

![Diagnosing a failed import set with a data source name.](../image/now-assist-sgc-diagnose-data-source.png)

</td></tr><tr><td id="d201391e271">

**Import set**

</td><td>

Import set number to diagnose. For example, `CISET0010075`.![Diagnosing a failed import set with the import set number.](../image/now-assist-sgc-diagnose-import-set.png)

After entering an import set number, you can view the error summary that is associated with that import set. If the import set was processed without errors, a message indicating no errors is displayed.

</td></tr></tbody>
</table>4.  Analyze other issues for the import set or other import set failures for the selected data source.

    ![Diagnosing other issues for the import set or other import set failures for the selected data source.](../image/now-assist-sgc-diagnose-more.png)

5.  If no other import set issues are observed within a data source, analyze a different data source for the connector.

    ![Diagnosing a different data source.](../image/now-assist-sgc-diagnose-connector-other.png)


## Result

Now Assist triggers the diagnosis process for the failed import sets. The Now Assist panel includes two key sections: Issue and Diagnosis recommendation, focused on the latest issue. The recommendation for an issue is based on a knowledge article matched using AI Search. A link to the knowledge article is provided in the Source section for additional guidance.

For issues related to Identification and Reconciliation engine \(IRE\), the panel provides a detailed summary of errors, including import errors, flow errors, partial payloads, and incomplete payloads.

![Failed import set diagnosis result.](../image/now-assist-sgc-diagnose-result.png "Diagnosis results for the failed import set with processing errors")

![Import set diagnosis result with IRE issues.](../image/now-assist-sgc-diagnose-result-ire.png "Diagnosis results for the failed import set with IRE issues")

**Tip:** To restart the conversation, select the reset icon \(![](../image/now-assist-reset-icon.png)\). If you reset the conversation, the existing messages are deleted, and a new conversation is started. You won't be able to access the previous messages after you reset the conversation. To learn more about how to use the Now Assist panel, see [Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## What to do next

You can hover over the diagnosis recommendation and select an option to provide feedback or copy the summary text to the clipboard.

<table id="table_g1q_hcy_x2c"><thead><tr><th>

Action

</th><th>

Procedure

</th></tr></thead><tbody><tr><td>

Provide feedback

</td><td>

If you think that the summary was helpful, select thumbs-up ![](../image/icon-thumbs-up.png). If you think that the summary wasn’t helpful, select thumbs-down ![](../image/icon-thumbs-down.png).This feedback improves the Agentic AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the Agentic AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td>

Copy the summary

</td><td>

Select the copy to clipboard icon ![](../image/icon-clipboard.png) to use the content for another purpose, such as pasting into an email.

</td></tr></tbody>
</table>**Related topics**  


[CMDB Workspace store app](../concept/cmdb-workspace.md)

[Service Graph Workspace store app](../concept/sg-workspace.md)

