---
title: Create an Agent Client Collector Security Incident Response OSQuery
description: Define an OSQuery to gather information on a security incident's CI. OSQuery provides an SQL layer on top of OS tables, and is bundled together with the Agent Client Collector as part of the base system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-operations-management/agent-client-collector/acc-create-os-query.html
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Security Incident Response, Agent Client Collector, IT Operations Management]
---

# Create an Agent Client Collector Security Incident Response OSQuery

Define an OSQuery to gather information on a security incident's CI. OSQuery provides an SQL layer on top of OS tables, and is bundled together with the Agent Client Collector as part of the base system.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector SIR Integration** &gt; **ACC Integration OSQuery**.

2.  Select **New**.

    The **ACC Integration OSQuery - New Record** page appears.

3.  Configure the fields on the page.

    |Field|Description|
    |-----|-----------|
    |Name|A descriptive name for the query.|
    |Query|The query string.|

4.  To validate that the Query you are writing works, select **Test OSQuery**.

    The **Test OSQuery** page appears.

    |Field|Description|
    |-----|-----------|
    |Agent|The specific end-point where the Query is run.|

5.  Enter the specific end-point Agent where the result of the test is displayed.

6.  -   \[Omitted image "acc-create-command-ok.png"\] Alt text: successful If it was successful
-   \[Omitted image "acc-create-command-large.png"\] Alt text: large too large of an output
-   \[Omitted image "acc-create-command-error.png"\] Alt text: error or an Error occurred with the error message displayed to the sn\_si.admin.
7.  Select **Submit**.

    OSQueries gather information on the target machine, where the incident commands are listed by operating system. For example, a query defined as `select * from system_info` gathers all information from the OSQuery **system\_info** table.


**Parent Topic:**[Agent Client Collector Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/agent-client-collector/acc-security-incident-response.md)

