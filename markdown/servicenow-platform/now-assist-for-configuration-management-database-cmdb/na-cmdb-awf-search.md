---
title: Use Now Assist to search the CMDB
description: The Search CMDB agentic workflow enables you to search for CIs by specifying any of several attributes of the CI of interest. The workflow accepts your natural language request, verifies your search goal, and then, depending on the information you provided, generates a keyword search, a single-table search with dot walks, or a multi-table search that involves relationship navigation. The workflow can infer CI relationship data to generate an appropriate query.
locale: en-US
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-04-10"
reading_time_minutes: 3
breadcrumb: [Use agentic workflows, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Use Now Assist to search the CMDB

The Search CMDB agentic workflow enables you to search for CIs by specifying any of several attributes of the CI of interest. The workflow accepts your natural language request, verifies your search goal, and then, depending on the information you provided, generates a keyword search, a single-table search with dot walks, or a multi-table search that involves relationship navigation. The workflow can infer CI relationship data to generate an appropriate query.

## Before you begin

Confirm that Query Generation skills are activated. For instructions, see Configuring Query Generation.

**Note:** Because activation configures a large amount of data, wait one day after activation to use the Search CMDB agentic workflow.

Role required: sn\_cmdb\_user and now\_assist\_panel\_user

## About this task

The Search CMDB agentic workflow can perform the following types of search:

-   Keyword searches for a specific CI. You can search using name, IP address, serial number, MAC address, or asset tag. For example, "search the CMDB for 192.168.1.1".
-   CMDB searches that are single-table queries \(including dot walk conditions for one level\). For example,"What servers does Wile E. Coyote own?" or "Search the CMDB for operational windows servers that aren't assigned to anyone".
-   Starting with Now Assist for CMDB v3.0, searches can include parent-child nodes spanning multiple tables and can traverse relationship graphs \(searches that traverse the cmdb\_rel\_ci\), for example, "Search for servers that depend on databases".

**Note:** The **sn\_cmdb\_gen\_ai.cmdb\_rel\_ci.search.enabled** system property is a Boolean that controls relational search \(search queries that traverse the cmdb\_rel\_ci\). The default value is true. Set the value to false to disable relational search.

## Procedure

1.  On the CMDB Workspace or in any form or list view, select the Now Assist icon ![](../../../administer/virtual-agent/images/icon-now-assist-sparkle.png).

2.  Start a Now Assist query with "`Search the CMDB for`" and then enter the search criteria as described in the next step.

3.  Enter the information that describes the searched-for CIs.

    -   Provide as much as you know about the CIs. Ideally provide the class type followed by other search values and conditions. For example, name, IP address, serial number, MAC address, or asset tag.
    -   If a query fails, you can check query generation events to determine the cause. Select **All** &gt; **Query Generation** &gt; **Event Queue** to view events. In some cases, a log will exist for the query. Select **All** &gt; **Query Generation** &gt; **Logs** to view the logs. For more information, see Query Generation logs.
4.  Refine the query if Now Assist does not return the CI that you're interested in.

    For example, you might have specified an IP address that is duplicated in multiple tables. In such cases, provide details that narrow the search.

5.  Provide feedback, copy the response text to the clipboard, or refresh the response.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d72478e233">

Option

</th><th align="left" id="d72478e236">

Procedure

</th></tr></thead><tbody><tr><td id="d72478e242">

**Provide feedback for the summary**

</td><td>

If you think that the response was helpful, select thumbs-up ![](../../configuration-management/image/icon-thumbs-up.png). If you think that it wasn’t helpful, select thumbs-down ![](../../configuration-management/image/icon-thumbs-down.png).This feedback improves the Agentic AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated response and stores it in the Agentic AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d72478e257">

**Copy the summary**

</td><td>

Select the copy to clipboard icon ![](../../configuration-management/image/icon-clipboard.png) to use the response information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d72478e268">

**Refresh the summary**

</td><td>

If you think that data might have changed after you viewed the response, select the redo icon ![](../../configuration-management/image/icon-redo.png) to refresh the response information.

</td></tr></tbody>
</table>
## Result

If fewer than five search results are returned, they are summarized. If more results are returned, they appear in a linked list \(limited to 100 records\).

To learn more about using the Now Assist panel, see Working in the Now Assist panel.

**Parent Topic:**[Using agentic workflows in Now Assist for CMDB](../../configuration-management/concept/now-assist-cmdb-using.md)

