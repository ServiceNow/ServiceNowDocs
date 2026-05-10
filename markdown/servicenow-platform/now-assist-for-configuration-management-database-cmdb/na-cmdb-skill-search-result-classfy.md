---
title: Search the Service Graph database using natural language
description: Now Assist for CMDB uses the search result classifier skill to analyze your search criteria, identify and apply implicit filters, determine the optimum search method \(keyword search or query generation\), query Service Graph data, and then display the results. You then have the option to refine the search using natural language in the Now Assist panel.
locale: en-US
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Search the Service Graph database using natural language

Now Assist for CMDB uses the search result classifier skill to analyze your search criteria, identify and apply implicit filters, determine the optimum search method \(keyword search or query generation\), query Service Graph data, and then display the results. You then have the option to refine the search using natural language in the Now Assist panel.

## Before you begin

Starting with Now Assist for CMDB v3.0, the Now Assist for CMDB ServiceNow Store app must be installed. When the app is installed, several agents and skills are auto-activated. If you deactivate a skill, some features will not appear.

For more information, see [Configure Now Assist for CMDB 3.0](../../configuration-management/task/now-assist-cmdb-configure-3.0.md).

The Service Graph database on your instance includes CIs, services, and related data such as company and location data.

Role required: sn\_cmdb\_user and now\_assist\_panel\_user

## Procedure

1.  On the Service Graph Workspace, select the search icon ![](../../../administer/conversational-interfaces/image/sidebar-search-icon.png) in the side panel.

2.  On the **Search** tab, enter the search text in the text box and then press **Enter** or select the search icon.

    ![Two sections in the search results.](../image/na-cmdb-search-rsult-class-skill.png)

    Two sections appear.

    -   The first section displays the count of matches with your search request and identifies the tables in which the matches were found and the filters that were applied. In addition, you can select the link to ask a follow-up question in the Now Assist panel.
    -   The second section displays the list of records that match the search criteria. Select a record name to view details.
3.  If you select the link to ask a follow-up question, the Now Assist panel opens.

    Now Assist guides you through the process of refining the search. For more information, see [Working in the Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md).

4.  Provide feedback, copy the response text to the clipboard, or refresh the response.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d277958e188">

Option

</th><th align="left" id="d277958e191">

Procedure

</th></tr></thead><tbody><tr><td id="d277958e197">

**Provide feedback for the summary**

</td><td>

If you think that the response was helpful, select thumbs-up ![](../../configuration-management/image/icon-thumbs-up.png). If you think that it wasn’t helpful, select thumbs-down ![](../../configuration-management/image/icon-thumbs-down.png).This feedback improves the Agentic AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated response and stores it in the Agentic AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d277958e212">

**Copy the summary**

</td><td>

Select the copy to clipboard icon ![](../../configuration-management/image/icon-clipboard.png) to use the response information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d277958e223">

**Refresh the summary**

</td><td>

If you think that data might have changed after you viewed the response, select the redo icon ![](../../configuration-management/image/icon-redo.png) to refresh the response information.

</td></tr></tbody>
</table>
**Related topics**  


[Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md)

