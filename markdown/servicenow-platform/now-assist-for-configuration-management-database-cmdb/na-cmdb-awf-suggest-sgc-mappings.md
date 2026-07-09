---
title: Recommend service graph connector agentic workflow
description: When you specify that you want to populate CMDB data for a particular CI class and attributes, Now Assist recommends the data sources or ingestion sources and SGCs that are best for your purpose.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-suggest-sgc-mappings.html
release: zurich
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-18"
reading_time_minutes: 2
breadcrumb: [Use agentic workflows, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Recommend service graph connector agentic workflow

When you specify that you want to populate CMDB data for a particular CI class and attributes, Now Assist recommends the data sources or ingestion sources and SGCs that are best for your purpose.

## Before you begin

Role required: sn\_cmdb\_admin or cmdb\_inst\_admin

## About this task

Incomplete CI data can lead to poor business outcomes and loss of trust in business-facing applications like Hardware Asset Management, IT Service Management, and ITSM Software Asset Management. Sometimes you're not sure which integration to use to capture required CI attribute data for a particular class \(and, by extension, which associated business outcomes are affected when the data is missing\). Now Assist provides recommendations for integrations that would help to capture the required data.

## Procedure

1.  Select the Now Assist icon \[Omitted image "icon-now-assist-sparkle.png"\] to open the Now Assist panel and then perform the following procedure.

    1.  To start the process, enter text similar to `recommend an SGC`.

    2.  Enter the classes that you want to populate.

        Include the `cmdb_ci` prefix in the class name. Optionally, specify the attributes that you want to populate.

        |Example prompt to start the process|Example CI classes|Example attributes|
        |-----------------------------------|------------------|------------------|
        |recommend sgc|cmdb\_ci\_computer|all fields|
        |recommend connectors|cmdb\_ci\_aix\_server|name, serial\_number, model\_id|
        |recommend sgc integrations|cmdb\_ci\_hardware|all attributes|
        |suggest connectors|cmdb\_ci\_cloud\_database, cmdb\_ci\_server, cmdb\_ci\_ip\_address|\[If no attributes are specified, Now Assist assumes all attributes.\]|

    Now Assist presents the recommended Service Graph Connectors for the classes and attributes that you specified.

    -   The list includes all data sources that populate the classes that you specified.
    -   The list is ordered by the number of classes supported.
    -   A connector might be listed for multiple classes.
    \[Omitted image "na-cmdb-sgc-recommendations.png"\] Alt text: Now Assist lists the classes and attributes

2.  Follow the guidance on the Now Assist panel to determine the SGC connection to use or the Service Graph Connectors to install and configure for the data set that you specified.

    For more information, see [Working in the Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md).

3.  Provide feedback, copy the response text to the clipboard, or refresh the response.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d505224e268">

Option

</th><th align="left" id="d505224e271">

Procedure

</th></tr></thead><tbody><tr><td id="d505224e277">

**Provide feedback for the summary**

</td><td>

If you think that the response was helpful, select thumbs-up \[Omitted image "icon-thumbs-up.png"\]. If you think that it wasn’t helpful, select thumbs-down \[Omitted image "icon-thumbs-down.png"\].This feedback improves the agentic AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated response and stores it in the agentic AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d505224e292">

**Copy the summary**

</td><td>

Select the copy to clipboard icon \[Omitted image "icon-clipboard.png"\] to use the response information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d505224e303">

**Refresh the summary**

</td><td>

If you think that data might have changed after you viewed the response, select the redo icon \[Omitted image "icon-redo.png"\] to refresh the response information.

</td></tr></tbody>
</table>
**Parent Topic:**[Using agentic workflows in Now Assist for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-using.md)

**Related topics**  


[Exploring Service Graph Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/exploring-sg-workspace.md)

