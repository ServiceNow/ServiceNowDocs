---
title: Components installed with Workplace Central
description: Several types of components are installed with activation of the Workplace Central application, including tables, user roles, and business rules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-central/components-installed-with-workplace-central.html
release: australia
product: Workplace Central
classification: workplace-central
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Components installed with Workplace Central

Several types of components are installed with activation of the Workplace Central application, including tables, user roles, and business rules.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

Demo data is available for this feature.

## Roles

|Roles|Description|Contains roles|
|-----|-----------|--------------|
|sn\_wsd\_central.workspace\_user|Has access to the Workplace Central workspace.|canvas\_user|
|sn\_wsd\_central.workplace\_analytics\_user|Has access to the Workplace Analytics workspace|sn\_wsd\_central.workspace\_user|

For details of roles that are required to use the Workplace Central, refer to the roles installed with Workplace Space Management and Workplace Move Management.

## Tables

<table id="table_x31_wb4_wvb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Utilization vs Capacity​\[sn\_wsd\_spcmgmt\_utilization\_capacity​\]

</td><td>

A table to store Capacity and Utilization drilled down to the area level.​

</td></tr></tbody>
</table>## Scripts

|Table|Description|
|-----|-----------|
|WSDSpaceMgmtAnalyticsSNC|Script which populates the capacity vs utilization table for Space Management in Workplace Analytics​|

**Parent Topic:**[Workplace Central reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/workplace-central-references.md)

**Related topics**  


[Space Optimization - Key features and actions]()

[Workplace Central Event planner]()

[Scenario and Building - Views, states, settings, and key features]()

[Space request approvals, states, actions, and key features]()

[Move management key features and actions]()

[Case Management - Key features, Actions &amp; Case details]()

[Schedule Plan details form]()

[Scenario details form]()

[Space Deployment Plan]()

[User Deployment Plan]()

[Excel column lengths for move projects]()

[Move conflicts for projects created via Excel upload]()

[Workplace Central troubleshooting]()

[Workplace Task form - Space Assignment task]()

[Neighborhood User Assignment Rule form]()

[User Workplace Profile form]()

