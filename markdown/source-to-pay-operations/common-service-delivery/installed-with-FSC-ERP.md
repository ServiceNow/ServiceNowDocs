---
title: Components installed with ERP Integration Framework
description: Several types of components are installed with the installation of the ERP Integration Framework application, including tables and user roles.
locale: en-US
release: yokohama
product: Common Service Delivery
classification: common-service-delivery
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Install the Finance and Supply Chain common applications, Configuring FSC common applications, Finance and Supply Chain common applications, Finance and Supply Chain applications, Finance and Supply Chain]
---

# Components installed with ERP Integration Framework

Several types of components are installed with the installation of the ERP Integration Framework application, including tables and user roles.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Integration user\[sn\_fcms\_intg.integration\_user\]

</td><td>

Configure integration setup for the applications \(SPO, SLO, or APO\) with ERP.

</td><td>

None

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_dx3_gb1_wdb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ERP User Sync

</td><td>

Fetches the list of users mapped under an ERP role in the ERP Role Mapping table. Assigns the ServiceNow user role to users based on the mapping.

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ERP Role Mapping\[sn\_fcms\_intg\_erp\_role\_map\]

</td><td>

Stores mapping of ServiceNow and ERP journal roles. The mapping helps to assign users to the Journal preparer and approver roles in ServiceNow applications \(SPO, SLO, or APO\) when they are granted the corresponding role in ERP.

</td></tr><tr><td>

ERP User Mapping\[sn\_fcms\_intg\_erp\_user\_map\]

</td><td>

Stores ServiceNow and ERP User ID mapping that is required for integration to work. The mapping is maintained for all active users who have the journal preparer or approver role in ERP.

</td></tr><tr><td>

Park Post Response\[sn\_fcms\_intg\_parkpostresponse\]

</td><td>

Stores the park and post response from ERP.

</td></tr><tr><td>

Reverse Response\[sn\_fcms\_intg\_reverse\_response\]

</td><td>

Stores the reverse response from ERP.

</td></tr><tr><td>

Service Element Map\[sn\_fcms\_intg\_service\_element\_map\]

</td><td>

Stores the mapping of the ERP journal Header and Line fields with those of the application \(SPO, SLO, or APO\) fields payload.

</td></tr><tr><td>

Service Map\[sn\_fcms\_intg\_service\_map\]

</td><td>

Stores mapping for all services to the ERP such as Journal Post, Journal Reverse, and Fetch Users.

</td></tr><tr><td>

Service Queue\[sn\_fcms\_intg\_service\_queue\]

</td><td>

Stores the requests being sent to ERP.

</td></tr><tr><td>

ERP Source Configuration\[sn\_fcms\_intg\_source\]

</td><td>

Maintains ERP details such as credentials and web service details.

</td></tr></tbody>
</table>**Parent Topic:**[Install the Finance and Supply Chain common applications](../../source-to-pay-operations/task/install-fsc-common-apps.md)

