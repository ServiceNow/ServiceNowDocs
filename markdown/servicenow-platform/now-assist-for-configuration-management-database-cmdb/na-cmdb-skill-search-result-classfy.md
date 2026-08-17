---
title: Search the Service Graph database using natural language
description: ServiceNow Otto for CMDB uses the search result classifier skill to analyze your search criteria, identify and apply implicit filters, determine the optimum search method \(keyword search or query generation\), query Service Graph data, and then display the results. You then have the option to refine the search using natural language in the ServiceNow Otto panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-skill-search-result-classfy.html
release: zurich
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Search the Service Graph database using natural language

ServiceNow Otto for CMDB uses the search result classifier skill to analyze your search criteria, identify and apply implicit filters, determine the optimum search method \(keyword search or query generation\), query Service Graph data, and then display the results. You then have the option to refine the search using natural language in the ServiceNow Otto panel.

## Before you begin

Starting with ServiceNow Otto for CMDB v3.0, the ServiceNow Otto for CMDB ServiceNow Store app must be installed. When the app is installed, several agents and skills are auto-activated. If you deactivate a skill, some features will not appear.

For more information, see [Configure ServiceNow Otto for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-configure-3.0.md).

The Service Graph database on your instance includes CIs, services, and related data such as company and location data. Search Service Graph database can invoke the "Analyze the CMDB search request" skill.

Role required: sn\_cmdb\_user and now\_assist\_panel\_user

## Procedure

1.  On the Service Graph Workspace, select the search icon \[Omitted image "sidebar-search-icon.png"\] Alt text: in the side panel.

2.  On the **Search** tab, enter the search text in the text box and then press **Enter** or select the search icon.

    \[Omitted image "na-cmdb-search-rsult-class-skill.png"\] Alt text: Two sections in the search results.

    Two sections appear.

    -   The first section displays the count of matches with your search request and identifies the tables in which the matches were found and the filters that were applied. In addition, you can select the link to ask a follow-up question in the ServiceNow Otto panel.
    -   The second section displays the list of records that match the search criteria. Select a record name to view details.
3.  If you select the link to ask a follow-up question, the ServiceNow Otto panel opens.

    ServiceNow Otto guides you through the process of refining the search. For more information, see [Working in the ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md).

4.  Provide feedback, copy the response text to the clipboard, or refresh the response.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d286608e188">

Option

</th><th align="left" id="d286608e191">

Procedure

</th></tr></thead><tbody><tr><td id="d286608e197">

**Provide feedback for the summary**

</td><td>

If you think that the response was helpful, select thumbs-up \[Omitted image "icon-thumbs-up.png"\]. If you think that it wasn’t helpful, select thumbs-down \[Omitted image "icon-thumbs-down.png"\].This feedback improves the agentic AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated response and stores it in the agentic AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d286608e212">

**Copy the summary**

</td><td>

Select the copy to clipboard icon \[Omitted image "icon-clipboard.png"\] to use the response information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d286608e223">

**Refresh the summary**

</td><td>

If you think that data might have changed after you viewed the response, select the redo icon \[Omitted image "icon-redo.png"\] to refresh the response information.

</td></tr></tbody>
</table>
**Related topics**  


[ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)

