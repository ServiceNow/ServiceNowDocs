---
title: Recommend service graph connector agentic workflow
description: Sometimes you're not sure which integration to use to capture CI data. When you provide ServiceNow Otto with the name of a particular CI class, it can recommend the data sources or Service Graph Connectors and ingestion sources that can best populate CMDB data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-suggest-sgc-mappings.html
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-18"
reading_time_minutes: 2
breadcrumb: [Using agentic workflows, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Recommend service graph connector agentic workflow

Sometimes you're not sure which integration to use to capture CI data. When you provide ServiceNow Otto with the name of a particular CI class, it can recommend the data sources or Service Graph Connectors and ingestion sources that can best populate CMDB data.

## Before you begin

Role required: sn\_cmdb\_admin or cmdb\_inst\_admin

## About this task

Incomplete CI data can lead to poor business outcomes and loss of trust in business-facing applications like Hardware Asset Management, IT Service Management, and ITSM Software Asset Management. Sometimes you're not sure which integration to use to capture required CI attribute data for a particular class \(and, by extension, which associated business outcomes are affected when the data is missing\). ServiceNow Otto provides recommendations for integrations that would help to capture the required data.

## Procedure

1.  Select the ServiceNow Otto icon \[Omitted image "icon-otto-outline-24.svg"\] to open the ServiceNow Otto panel and then perform the following procedure.

    1.  To start the process, enter text similar to `recommend an SGC`.

    2.  Enter the classes that you want to populate.

        Include the `cmdb_ci` prefix in the class name. Optionally, specify the attributes that you want to populate.

        |Example prompt to start the process|Example CI classes|Example attributes|
        |-----------------------------------|------------------|------------------|
        |recommend sgc|cmdb\_ci\_computer|all fields|
        |recommend connectors|cmdb\_ci\_aix\_server|name, serial\_number, model\_id|
        |recommend sgc integrations|cmdb\_ci\_hardware|all attributes|
        |suggest connectors|cmdb\_ci\_cloud\_database, cmdb\_ci\_server, cmdb\_ci\_ip\_address|\[If no attributes are specified, ServiceNow Otto assumes all attributes.\]|

    ServiceNow Otto presents the recommended Service Graph Connectors for the classes and attributes that you specified.

    -   The list includes all data sources that populate the classes that you specified.
    -   The list is ordered by the number of classes supported.
    -   A connector might be listed for multiple classes.
    \[Omitted image "na-cmdb-sgc-recommendations.png"\] Alt text: ServiceNow Otto lists the classes and attributes

2.  Follow the guidance on the ServiceNow Otto panel to determine the SGC connection to use or the Service Graph Connectors to install and configure for the data set that you specified.

    For more information, see [Working in the ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md).

3.  Provide feedback, copy the response text to the clipboard, or refresh the response.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d510245e271">

Option

</th><th align="left" id="d510245e274">

Procedure

</th></tr></thead><tbody><tr><td id="d510245e280">

**Provide feedback for the summary**

</td><td>

If you think that the response was helpful, select thumbs-up \[Omitted image "icon-thumbs-up.png"\]. If you think that it wasn’t helpful, select thumbs-down \[Omitted image "icon-thumbs-down.png"\].This feedback improves the agentic AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated response and stores it in the agentic AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d510245e295">

**Copy the summary**

</td><td>

Select the copy to clipboard icon \[Omitted image "icon-clipboard.png"\] to use the response information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d510245e306">

**Refresh the summary**

</td><td>

If you think that data might have changed after you viewed the response, select the redo icon \[Omitted image "icon-redo.png"\] to refresh the response information.

</td></tr></tbody>
</table>
**Parent Topic:**[Using agentic workflows in ServiceNow Otto for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-using.md)

**Related topics**  


[Exploring Service Graph Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/exploring-sg-workspace.md)

