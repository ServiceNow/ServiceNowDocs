---
title: Components installed with Emergency Exposure Management
description: Several types of components are installed with Emergency Exposure Management, including tables and user roles.
locale: en-US
release: zurich
product: Emergency Exposure Management
classification: emergency-exposure-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Install Emergency Exposure Management, Emergency Exposure Management, Emergency Response Management, Workplace Service Delivery, Employee Service Management]
---

# Components installed with Emergency Exposure Management

Several types of components are installed with Emergency Exposure Management, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Emergency Exposure Admin\[sn\_imt\_diagnosis.diagnostics\_admin\]

</td><td>

Can create a new diagnostic request and view or download the list of impacted users.

</td><td>

-   sn\_imt\_diagnosis.workplace\_exposure\_analyst
-   sn\_imt\_monitoring.monitoring\_user

</td></tr><tr><td>

Workplace exposure analyst\[sn\_imt\_diagnosis.workplace\_exposure\_analyst\]

</td><td>

Identifies potentially exposed employees using workplace reservations from the ServiceNow® Workplace Core application.

</td><td>

None

</td></tr></tbody>
</table>## Scheduled jobs installed

|Scheduled job|Description|
|-------------|-----------|
|Execute employee diagnostic events|Looks up pending events from the Diagnostic Events \[sn\_imt\_diagnosis\_diagnostics\_event\] table and processes them to populate the Impacted Users \[sn\_imt\_diagnosis\_impacted\_users\] table.|

## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Diagnostic Request\[sn\_imt\_diagnosis\_diagnostic\_request\]

</td><td>

Allows a user to create a diagnostic request for the affected user.

</td></tr><tr><td>

Diagnostic Events\[sn\_imt\_diagnosis\_diagnostics\_event\]

</td><td>

Subtasks generated for diagnostic requests. A scheduled job processes the tasks to identify the list of potentially impacted employees.

</td></tr><tr><td>

Diagnostic Request Task\[sn\_imt\_diagnosis\_diagnostic\_request\_task\]

</td><td>

Diagnostic request tasks created automatically for diagnostic requests to identify the list of potentially impacted employees. The task is created based on the selected data source in a diagnostic request.

</td></tr><tr><td>

Diagnostic Request Task Config\[sn\_imt\_diagnosis\_diagnostic\_request\_task\_config\]

</td><td>

Configuration for a diagnostic request task. For a data source selected in a diagnostic request, the corresponding diagnostic request task when created matches the type of task configuration.

</td></tr><tr><td>

Impacted Users\[sn\_imt\_diagnosis\_impacted\_users\]

</td><td>

Employees who may have been exposed to infectious diseases through an affected employee. Populated by analyzing multiple data sources for the affected employees.

</td></tr><tr><td>

Impacted Visitors\[sn\_imt\_diagnosis\_impacted\_visitor\]

</td><td>

Visitors who might have been exposed to infection. Populated by analyzing the visitors request entry records invited by the affected employees.The table is available for use only if you also subscribe to ServiceNow® Contact Tracing and ServiceNow® Employee Health Screening. The data of this table is displayed in the Impacted visitors related list on the Diagnostic Report form.

</td></tr><tr><td>

Potential Workplace Exposure\[sn\_imt\_diagnosis\_potential\_workplace\_exposure\]

</td><td>

Potentially exposed employees who had reservations for the same shifts as the affected employee during the specified time period.

 The table is available for use only if you also subscribe to Workplace Core.

</td></tr><tr><td>

Tracing system\[sn\_imt\_diagnosis\_tracing\_system\]

</td><td>

Data source configuration to identify potentially exposed employees by using diagnostic requests.

</td></tr><tr><td>

Tracing system properties\[sn\_imt\_diagnosis\_m2m\_tracing\_system\_properties\]

</td><td>

System properties for additional configuration of tracing systems.

</td></tr></tbody>
</table>**Parent Topic:**[Install Emergency Exposure Management](../task/install-emergency-exposure-mgt.md)

