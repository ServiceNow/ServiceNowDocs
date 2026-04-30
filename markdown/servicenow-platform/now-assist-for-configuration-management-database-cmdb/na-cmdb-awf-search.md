---
title: Use Now Assist to search the CMDB for CIs
description: The Search CMDB agentic workflow enables you to search for CIs by specifying any of several attributes of the CI of interest. The workflow accepts your natural language request, verifies your search goal, and then generates a keyword search, a single-table search with dot walks, or a multi-table searches that involve relationship navigation, depending on the information you provided. The workflow can infer CI relationship data to generate an appropriate query.
locale: en-US
release: zurich
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-02-06"
reading_time_minutes: 2
breadcrumb: [Use agentic workflows, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Use Now Assist to search the CMDB for CIs

The Search CMDB agentic workflow enables you to search for CIs by specifying any of several attributes of the CI of interest. The workflow accepts your natural language request, verifies your search goal, and then generates a keyword search, a single-table search with dot walks, or a multi-table searches that involve relationship navigation, depending on the information you provided. The workflow can infer CI relationship data to generate an appropriate query.

## Before you begin

**Important:** This agentic workflow is turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

Verify that Query Generation skills are activated. For instructions, see [Configuring Query Generation](https://www.servicenow.com/docs/access?context=configuring-query-generation&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

**Note:** Because activation configures a large amount of data, wait one day after activation to use the Search CMDB agentic workflow.

Role required: sn\_cmdb\_user and now\_assist\_panel\_user

## About this task

The Search CMDB agentic workflow can perform the following types of search:

-   CMDB searches that are keyword searches for a specific CI. You can search using name, IP address, serial number, MAC address, or asset tag. For example, "Search the CMDB for Linux Servers", or "List all IPs".
-   CMDB searches that are single-table queries \(including dot walk conditions for one level\). For example,"What servers does Wile E. Coyote own?" or "Search the CMDB for operational windows servers that aren't assigned to anyone".

## Procedure

1.  On the CMDB Workspace or in any form or list view, select the Now Assist icon ![](../../../administer/virtual-agent/images/icon-now-assist-sparkle.png).

2.  Start a Now Assist query with "`Search the CMDB for`" and then enter the search criteria as described in the next step.

3.  Enter the information that describes the searched-for CI.

    -   Provide as much as you know about the CI. Ideally provide the class type followed by other search values and conditions. For example, name, IP address, serial number, MAC address, or asset tag.
    -   If a query fails, you can check query generation events to determine the cause. Select **All** &gt; **Query Generation** &gt; **Event Queue** to view events. In some cases, a log will exist for the query. Select **All** &gt; **Query Generation** &gt; **Logs** to view the logs. For more information, see [Query Generation logs](https://www.servicenow.com/docs/access?context=query-generation-logs&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).
4.  Refine the query if Now Assist returns a CI, but not the CI that you're interested in.

    For example, you might have specified an IP address that is duplicated in multiple tables. In such cases, provide details that narrow the search.


## Result

If fewer than five search results are returned, they are summarized. If more results are returned, they appear in a linked list \(limited to 100 records\).

To learn more about using the Now Assist panel, see [Working in the Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

**Parent Topic:**[Using agentic workflows in Now Assist for CMDB](../../configuration-management/concept/now-assist-cmdb-using.md)

