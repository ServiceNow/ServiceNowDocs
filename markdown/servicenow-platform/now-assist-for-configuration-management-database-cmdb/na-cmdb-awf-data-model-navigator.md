---
title: Data model navigator
description: ServiceNow Otto can answer deep questions about Personal Computing devices, Server infrastructure, IP Address Management, and Core CMDB tables in the CMDB data model. Search results are pulled from the Data Model Navigator tables, which are indexed to increase performance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-data-model-navigator.html
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-04-20"
reading_time_minutes: 2
breadcrumb: [Using agentic workflows, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Data model navigator

ServiceNow Otto can answer deep questions about Personal Computing devices, Server infrastructure, IP Address Management, and Core CMDB tables in the CMDB data model. Search results are pulled from the Data Model Navigator tables, which are indexed to increase performance.

## Before you begin

Role required: sn\_cmdb\_user and sn\_data\_model\_nav.data\_model\_navigator\_read

## About this task

CMDB users, admins, and architects need advice on how to organize their CMDB so that it conforms to CSDM guidelines. The Data model navigator agentic workflow helps you to properly classify CIs and provides advice on critical individual columns in CMDB tables. This is important because the meaning of certain columns depends on the context of their use. Agentic AI helps you to identify and focus on the critical columns to promote a high quality CMDB implementation.

There are two modes of interaction with the Data model navigator: natural language queries and direct investigation in the indexed tables.

## Procedure

1.  On the Service Graph Workspace orCMDB Workspace or in any form or list view, select the ServiceNow Otto icon \[Omitted image "icon-now-assist-sparkle.png"\] and then enter your question in the Now Assist panel.

    Example questions:

    -   `What is the purpose of the subcategory field for a CI?`
    -   `What is storage device table used for?`
    -   `When should a CI's life cycle be in "Design"?`
    -   `Which table is used to store flexible key value pairs for a CI?`
    Agentic AI responds to your questions. Continue to refine your questions until you get the required information. For more information, see [Working in the ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md).

2.  Provide feedback, copy the response text to the clipboard, or refresh the response.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d140203e157">

Option

</th><th align="left" id="d140203e160">

Procedure

</th></tr></thead><tbody><tr><td id="d140203e166">

**Provide feedback for the summary**

</td><td>

If you think that the response was helpful, select thumbs-up \[Omitted image "icon-thumbs-up.png"\]. If you think that it wasn’t helpful, select thumbs-down \[Omitted image "icon-thumbs-down.png"\].This feedback improves the agentic AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated response and stores it in the agentic AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d140203e181">

**Copy the summary**

</td><td>

Select the copy to clipboard icon \[Omitted image "icon-clipboard.png"\] to use the response information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d140203e192">

**Refresh the summary**

</td><td>

If you think that data might have changed after you viewed the response, select the redo icon \[Omitted image "icon-redo.png"\] to refresh the response information.

</td></tr></tbody>
</table>3.  Navigate to **All** &gt; **Data Model Navigator** to inspect the indexed tables directly.

    \[Omitted image "na-cmdb-data-model-navigator-nav.png"\] Alt text: Supported aspects of the CMDB data model.

    Select an aspect of the data model that you want to research more deeply:

    -   Contexts
    -   Tables
    -   Fields
    -   Relationships

**Parent Topic:**[Using agentic workflows in ServiceNow Otto for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-using.md)

**Related topics**  


[ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md)

