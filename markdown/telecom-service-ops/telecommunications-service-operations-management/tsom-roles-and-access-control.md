---
title: Roles and access control in Telecommunications Service Operations Management
description: Access control lists \(ACLs\) restrict Telecommunications Service Operations Management \(TSOM\) records to users with a TSOM administrator role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/tsom-roles-and-access-control.html
release: brazil
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: reference
last_updated: "2026-11-09"
reading_time_minutes: 1
keywords: [ACL, tsom\_visibility\_admin, tsom\_assurance\_admin]
breadcrumb: [Reference, Telecommunications Service Operations Management]
---

# Roles and access control in Telecommunications Service Operations Management

Access control lists \(ACLs\) restrict Telecommunications Service Operations Management \(TSOM\) records to users with a TSOM administrator role.

## TSOM roles

<table id="table_tsom_roles"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_tsom\_core.tsom\_visibility\_admin

</td><td>

Telecom visibility operator or administrator. Grants access to TSOM Core discovery filters, telecom patterns, and guided setup for the service graph connectors.

</td><td>

-   agent\_admin
-   certification\_admin
-   cmdb\_inst\_admin
-   connection\_admin
-   discovery\_admin
-   import\_admin
-   sn\_cmdb\_admin
-   usage\_admin

</td></tr><tr><td>

sn\_tsom\_em\_core.tsom\_assurance\_admin

</td><td>

Telecom assurance operator or administrator. Grants access to the event and metric connector configuration records.

</td><td>

-   connection\_admin
-   dashboard\_admin
-   decision\_table\_admin
-   evt\_mgmt\_admin

</td></tr></tbody>
</table>## Access requirements by application

|Application|Records|Operations|Role required|
|-----------|-------|----------|-------------|
|Telecom Service Operations Core \(sn\_tsom\_core\)|Discovery filters \[Alias to Filter \(sn\_tsom\_alias\_to\_filter\)\]|Create, read, write, delete|sn\_tsom\_core.tsom\_visibility\_admin|
|Telecom Service Operations Core \(sn\_tsom\_core\)|Discovery filters \[Alias to Filter \(sn\_tsom\_alias\_to\_filter\)\]|Report view|Any of: sn\_tsom\_core.tsom\_visibility\_admin, cmdb\_read|
|Telecom Patterns \(sn\_tsom\_patterns\)|OIDs to pattern mappings \(sn\_tsom\_oids\_to\_pattern\)|Create, read, write, delete, report view|sn\_tsom\_core.tsom\_visibility\_admin|
|Service graph connectors for Nokia Altiplano, Fortinet, Meraki Telco SD-WAN, and VeloCloud Telco SD-WAN|Guided setup content \[Guided Setup Content \(gsw\_content\), Guided Setup Content Group \(gsw\_content\_group\), Guided Setup Content Information \(gsw\_content\_information\)\]|Create, write, delete|sn\_tsom\_core.tsom\_visibility\_admin|
|Service graph connectors for Nokia Altiplano, Fortinet, Meraki Telco SD-WAN, and VeloCloud Telco SD-WAN|Connector guided setup page|Read|sn\_tsom\_core.tsom\_visibility\_admin|
|All service graph connectors|Connection and credential aliases \[Alias \(sys\_alias\)\]|Read|Any of: import\_admin, connection\_admin, credential\_admin|
|Telecom Event and Metric Connectors \(sn\_tsom\_em\_connectors\)|Connector configuration \[Dynamic Alert Mapping \(sn\_tsom\_em\_connect\_dynamic\_alert\_mapping\), Dynamic Category Mapping \(sn\_tsom\_em\_connect\_dynamic\_category\_mapping\), Generic Recovery Queue \(sn\_tsom\_em\_connect\_generic\_recovery\_queue\), KPI Definitions \(sn\_tsom\_em\_conns\_kpi\_definitions\)\]|Create, read, write, delete, report view|sn\_tsom\_em\_core.tsom\_assurance\_admin|
|Telecom Event and Metric Connectors \(sn\_tsom\_em\_connectors\)|KPI Definitions \(sn\_tsom\_em\_conns\_kpi\_definitions\), Application \(cmdb\_ci\_appl\), Network Service Instance \(cmdb\_ci\_network\_service\_instance\)|Read|mid\_server|

**Important:**

Users without the required role can't see these records. Lists, forms, guided setup pages, and reports that use these tables display no records instead of an error. To grant access, assign the TSOM role for the application. For example, the sn\_tsom\_core.tsom\_visibility\_admin role includes the import\_admin and connection\_admin roles, so it also grants read access to connection and credential aliases.

**Parent Topic:**[Telecommunications Service Operations Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/components-installed-with-tsom.md)

