---
title: Components installed with SGC Central
description: Several types of components are installed with activation of the SGC Central \(sn\_sgc\_central\) plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SGC Central reference, SGC Central, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Components installed with SGC Central

Several types of components are installed with activation of the SGC Central \(sn\_sgc\_central\) plugin, including tables, user roles, and scheduled jobs.

## Scheduled jobs installed

<table id="table_i3r_5hv_tbc"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SGC central collection

</td><td>

Reads from the imports brought in by the connectors and updates the dashboard data.

</td></tr><tr><td>

SGC central collection onDemand with lookback

</td><td>

Collects historical data for the lookback period from when the data is retrieved for connectors. The default lookback period is set to 30 days.

</td></tr></tbody>
</table>## Tables installed

<table id="table_k3r_5hv_tbc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Record Tabs

 \[sn\_sgc\_central\_connection\_record\_tabs\]

</td><td>

Includes the tabs displayed on the page to edit connection, including default tabs like Details, Data Sources, Scheduled Imports, and Errors, and additional tabs specific to individual connectors, arranged by order.

</td></tr><tr><td>

Connection property config

 \[sn\_sgc\_central\_conn\_prop\_config\]

</td><td>

Stores the connection property fields for the Connection Properties tab displayed on the page to create or edit a connection, including group ordering, descriptions, mandatory fields, and default values for auto-population.

</td></tr><tr><td>

Service Graph Connection Trigger

 \[sn\_sgc\_central\_service\_graph\_connection\_trigger\]

</td><td>

Stores the trigger record to initialize playbook context in the create connection flow when a new record is inserted. The playbook is selected based on the referred metadata record's application scope field that is the Service Graph Connector scope.

</td></tr><tr><td>

Service Graph Connector

 \[sn\_sgc\_central\_service\_graph\_connector\]

</td><td>

Stores Service Graph Connector details such as scope, app ID, and associated provider.

</td></tr><tr><td>

SGC Installed Connection

 \[sn\_sgc\_central\_st\_installed\_connection\]

</td><td>

Stores all installed or draft connections, including details such as connection, processing status, last run, and import frequency information.

</td></tr><tr><td>

SGC IntegrationHub ETL

 \[sn\_sgc\_central\_st\_integrationhub\_etl\]

</td><td>

Stores the Extract Transform Load \(ETL\) list for display under the IntegrationHub ETL list view in SGC Central.

</td></tr></tbody>
</table>## ServiceNow Store applications installed

|Application|Description|
|-----------|-----------|
|Integration Commons for CMDB \(sn\_cmdb\_int\_util\)|Contains the CMDB Integrations Dashboard and a set of Robust Transform Engine \(RTE\) transforms and script includes.|
|CMDB Workspace \(sn\_cmdb\_ws\)|Provides a single place to access CMDB-focused features including SGC Central.|

**Parent Topic:**[SGC Central reference](sgcc-reference.md)

