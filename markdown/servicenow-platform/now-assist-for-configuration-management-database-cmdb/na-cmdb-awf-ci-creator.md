---
title: Create a CI using ServiceNow Otto
description: The Create configuration item agentic workflow accepts your natural language request to manually generate a valid CI in the class that you specify.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-ci-creator.html
release: zurich
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using agentic workflows, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a CI using ServiceNow Otto

The Create configuration item agentic workflow accepts your natural language request to manually generate a valid CI in the class that you specify.

## Before you begin

Role required:

-   ServiceNow Otto for CMDB v2.4 and earlier: sn\_cmdb\_editor and now\_assist\_panel\_user
-   Starting with ServiceNow Otto for CMDB v2.5: sn\_cmdb\_admin and now\_assist\_panel\_user
-   Starting with ServiceNow Otto for CMDB v3.0: sn\_cmdb\_editor and now\_assist\_panel\_user

## About this task

Occasionally, you might create a CI manually. To help you, the Create configuration item agentic workflow accepts your natural language request and verifies that it understands which class the new CI should belong to. The workflow then checks Identification and Reconciliation engine \(IRE\) rules to determine the required attributes for the CI and requests that information. After you provide sufficient data, the workflow promotes that the proposed CI includes the attributes that you requested, complies with IRE rules, and is not a duplicate. The workflow then creates the CI.

The Create configuration item agentic workflow is particularly useful for adding CIs to tables accessed by Operational Technology because users might add physical CIs while unaware of the importance of managing CI data in the CMDB.

**Note:** The workflow helps avoid creation of a CI whose class does not have an identification rule. For more information, see [Identification rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/c_IdentificationRules.md).

To learn more about using the ServiceNow Otto panel, see [Working in the ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md).

## Procedure

1.  Use either of the following methods to start the process.

    -   While working in the Service Graph Workspace orCMDB Workspace, select **Create CI** in the Quick Links section.
    -   While working in the Service Graph Workspace orCMDB Workspace, select the ServiceNow Otto icon \[Omitted image "icon-otto-outline-24.svg"\] and then enter `create a ci`.
2.  Enter the class of CI to create and then continue by answering the ServiceNow Otto questions.

3.  Provide feedback, copy the response text to the clipboard, or refresh the response.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d524649e202">

Option

</th><th align="left" id="d524649e205">

Procedure

</th></tr></thead><tbody><tr><td id="d524649e211">

**Provide feedback for the summary**

</td><td>

If you think that the response was helpful, select thumbs-up \[Omitted image "icon-thumbs-up.png"\]. If you think that it wasn’t helpful, select thumbs-down \[Omitted image "icon-thumbs-down.png"\].This feedback improves the agentic AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated response and stores it in the agentic AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d524649e226">

**Copy the summary**

</td><td>

Select the copy to clipboard icon \[Omitted image "icon-clipboard.png"\] to use the response information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d524649e237">

**Refresh the summary**

</td><td>

If you think that data might have changed after you viewed the response, select the redo icon \[Omitted image "icon-redo.png"\] to refresh the response information.

</td></tr></tbody>
</table>
**Parent Topic:**[Using agentic workflows in ServiceNow Otto for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-using.md)

