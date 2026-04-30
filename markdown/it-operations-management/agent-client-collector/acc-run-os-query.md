---
title: Run an Agent Client Collector Security Incident Response OSQuery
description: Run an OSQuery on a machine referenced by an incident to retrieve information on each incident's CI. For example, if you run a select \* from system\_info query on an incident, the query gathers all information from the OSQuery system\_info table.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Security Incident Response, Agent Client Collector, IT Operations Management]
---

# Run an Agent Client Collector Security Incident Response OSQuery

Run an OSQuery on a machine referenced by an incident to retrieve information on each incident's CI. For example, if you run a `select * from system_info` query on an incident, the query gathers all information from the OSQuery **system\_info** table.

## Before you begin

Role required: sn\_si.admin or sn\_si.basic

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Incidents** &gt; **Show All Incidents**.

2.  Select an incident.

3.  In the Related Links section, go to the **Configuration Items** list and select each incident's CIs that you want to retrieve the information.

4.  From the right-click menu, select **Run ACC OSQuery**

    The **OSQuery to run** dialog box opens.

5.  Select the name of the query you want to run.

    The available queries are those configured on the ACC Integration OSQuery page, as described in [Create an Agent Client Collector Security Incident Response OSQuery](acc-create-os-query.md). Options are selectable according to their Name value.

6.  Select **Submit**.

    The query runs on each of the selected security incident's CIs.


**Parent Topic:**[Agent Client Collector Security Incident Response](../concept/acc-security-incident-response.md)

