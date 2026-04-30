---
title: Components installed with Service Observability
description: Several types of components are installed with activation of the Service Observability plugin, including tables and user roles.
locale: en-US
release: yokohama
product: Service Observability
classification: service-observability
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Observability reference, Service Observability, ITOM AIOps, IT Operations Management]
---

# Components installed with Service Observability

Several types of components are installed with activation of the Service Observability plugin, including tables and user roles.

## Roles installed

<table id="table_hrh_vss_rdc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Operator/Operations manager \[snc\_sow\_svcobs.manager\]

</td><td>

Triages incidents in the SOW. Views basic health metrics for a service and more detailed service metrics from related entities.

</td><td>

-   sn\_sow\_srm.srm\_responder
-   connection\_admin
-   evt\_mgmt\_connector\_instance\_write

</td></tr><tr><td>

Service Observability admin \[sn\_sow\_svcobs.admin\]

</td><td>

Configures data sources and adds data mappings. Customizes dashboard templates.

</td><td>

-   sn\_sow\_srm.srm\_admin
-   connection\_admin
-   evt\_mgmt\_connector\_instance\_write
-   sn\_sow\_itsm\_admin.sow\_admin\_user

</td></tr></tbody>
</table>## Store applications installed

The following are installed when you install Service Observability.

<table id="table_kq3_shb_d2c"><thead><tr><th>

Store application \[plugin\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Observability UI\[sn\_service\_obs\_ui\]

</td><td>

The Overview and Observability tabs in the Service Details page of the SOW.

</td></tr><tr><td>

Service Reliability Management

</td><td>

Service Reliability Management and Service Observability display service performance metrics together to give a holistic view into service health.

</td></tr><tr><td>

Platform Analytics

</td><td>

Enables customizing the dashboards.

</td></tr></tbody>
</table>## Tables installed

<table id="table_lrh_vss_rdc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Dashboard fragments

 \[sn\_sow\_svcobs\_dashboard\_fragments\]

</td><td>

Contains the definitions of dashboards in JSON format.

</td></tr><tr><td>

Service to data mapping configuration map

 \[sn\_sow\_svcobs\_svc\_to\_config\_map\]

</td><td>

Associates data mapping configurations with a registered service using the CMDB Group Contains Configuration Item \[cmdb\_group\_contains\_ci\] table.

</td></tr><tr><td>

Data mapping configurations

 \[sn\_sow\_svcobs\_mapping\_config\]

</td><td>

Defines a data mapping configuration for a service.

</td></tr><tr><td>

Data mapping configuration rules

 \[sn\_sow\_svcobs\_mapping\_config\_rules\]

</td><td>

Defines a single tag-based mapping rule.

</td></tr><tr><td>

Observability data source

 \[sn\_sow\_svcobs\_data\_source\]

</td><td>

Defines a third-party APM vendor data source \(an `http_connections`\) that can be used to get telemetry for services.

</td></tr><tr><td>

Service Observability entity records

 \[sn\_sow\_svcobs\_entity\_records\]

</td><td>

Records configuration items and unknown monitored objects for entities that appear in dashboards.

</td></tr><tr><td>

Service Observability PA Dashboardssn\_sow\_svcobs\_pa\_dashboards

</td><td>

Contains reference information for customized dashboards.

</td></tr></tbody>
</table>**Parent Topic:**[Service Observability reference](service-observability-reference.md)

