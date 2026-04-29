---
title: Properties installed with Operational Resilience
description: When you install the Operational Resilience application, several system properties are added to your instance. You may not need to modify these properties. The user with the sn\_oper\_res.admin role can maintain these properties.
locale: en-US
release: australia
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Operational Resilience reference, Operational Resilience, Governance, Risk, and Compliance]
---

# Properties installed with Operational Resilience

When you install the Operational Resilience application, several system properties are added to your instance. You may not need to modify these properties. The user with the sn\_oper\_res.admin role can maintain these properties.

## Properties installed

<table id="table_dx3_gb1_wdb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_oper\_res.allowed\_task\_tables

</td><td>

Property used to assign the task relevant tables, such as problems and incidents, that are referenced in the Operational Resilience \[sn\_oper\_res\_task\] table. When a configuration item is used by both the Operational Resilience application and the task relevant tables, a record is generated and maintained in the \[sn\_oper\_res\_task\] table.

 Type: string

 Value: Problem

</td></tr><tr><td>

sn\_oper\_res.business\_process\_pillar

</td><td>

sys\_id of the Process pillar.

 Type: string

 Value: 6408bde4537310108722ddeeff7b121e

</td></tr><tr><td>

sn\_oper\_res.critical\_business\_processes

</td><td>

sys\_id of the business process entity type.

 Type: string

 Value: 221c1c9a53d310108722ddeeff7b12ae

</td></tr><tr><td>

sn\_oper\_res.critical\_services

</td><td>

sys\_id of the service entity type.

 Type: string

 Value: 2d7bd49a53d310108722ddeeff7b1297

</td></tr><tr><td>

sn\_oper\_res.dependency\_pillars

</td><td>

sys\_id of the Dependency pillars. It uses a comma-separated list of dependency pillars. For a new pillar, create a new record in \[sn\_grc\_choice\] table with the **Choice** category set to **Pillar** and append the sys\_id to the Value using a comma as shown in the example: e4f77de4537310108722ddeeff7b1263,ab5c78b0533112105806ddeeff7b126f,9c38fde4537310108722ddeeff7b12d0,a5187de4537310108722ddeeff7b127a,c4c775e4537310108722ddeeff7b12d7,2fad3034533112105806ddeeff7b123f. Refer to the following pillars and their corresponding sys\_ids:

-   Application Service: e4f77de4537310108722ddeeff7b1263
-   People: ab5c78b0533112105806ddeeff7b126f
-   Data: 9c38fde4537310108722ddeeff7b12d0
-   Suppliers: a5187de4537310108722ddeeff7b127a
-   Technology: c4c775e4537310108722ddeeff7b12d7
-   Facilities: 2fad3034533112105806ddeeff7b123f

 Type: string

 Value: e4f77de4537310108722ddeeff7b1263,ab5c78b0533112105806ddeeff7b126f,9c38fde4537310108722ddeeff7b12d0,a5187de4537310108722ddeeff7b127a,c4c775e4537310108722ddeeff7b12d7

</td></tr><tr><td>

sn\_oper\_res.logging.verbosity

</td><td>

Level of detail recorded in the log files, ranging from minimum to highly detailed information.

 Type: choice list

 Debug=0, Info=1, Warn=2, Error=3 Default: 2

</td></tr><tr><td>

sn\_oper\_res.max\_levels

</td><td>

Maximum number of levels to be processed \(The default value is 1\). For current release, only 1 level is supported.

 Type: string

 Value: 1

</td></tr><tr><td>

sn\_oper\_res.max\_nodes

</td><td>

Maximum number of nodes to be processed when the Operational Resilience API is called.

 -   Type: integer
-   Default value: 10,000

 For example, when the API is called, it displays the results for a maximum 10,000 nodes.

</td></tr><tr><td>

sn\_oper\_res.max\_top

</td><td>

Number of vulnerabilities to be displayed in the **Top vulnerabilities to be fixed** report in the Operational Resilience dashboard.-   Type: integer
-   Default value: 5

</td></tr><tr><td>

sn\_oper\_res.opres\_csdm\_main\_node\_config

</td><td>

Main node configuration that is used to get the data and create records in the \[sn\_grc\_m2m\_profile\_profile\] table.

 Type: string

 Value: c483a911ff2a311051b15c97d53bf1db

</td></tr><tr><td>

sn\_oper\_res.red\_flags\_exclusion

</td><td>

Classes that are excluded from red flags.

 Type: string

 Value: sn\_oper\_res\_profile, sn\_oper\_res\_bcm\_plan, sn\_oper\_res\_task

</td></tr><tr><td>

sn\_oper\_res.top\_class\_name

</td><td>

Property to designate any class as the top class in the dashboard.

 Type: string

 Value: cmdb\_ci\_service\_business

</td></tr><tr><td>

sn\_oper\_res.useAdvancedRisk

</td><td>

Property to define if the Operational Resilience High Risk computation should use Advanced Risk or Risk management.

 Type: True \| False

 Value: True

</td></tr><tr><td>

glide.ui.sn\_oper\_res\_importance\_impact\_tolerance\_assessment\_activity.fields

</td><td>

Impact and Importance Assessment activity formatter fields.

 Type: string

 Value: assigned\_to, state,work\_notes,comments, Attachments, opened\_by, active, approver

</td></tr><tr><td>

glide.ui.sn\_oper\_res\_scenario\_analysis\_activity.fields

</td><td>

Scenario Analysis activity formatter fields.

 Type: string

 Value: state, assigned\_to, plan\_approver, result\_approver, work\_notes, comments, Attachments

</td></tr></tbody>
</table>