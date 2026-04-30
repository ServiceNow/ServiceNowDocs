---
title: Components installed with Universal Request
description: Several types of components are installed with activation of the Universal Request plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: xanadu
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Activate Universal Request, Universal Request plugins, Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Components installed with Universal Request

Several types of components are installed with activation of the Universal Request plugin, including tables, user roles, and scheduled jobs.

Demo data is available for this feature.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Routing Agent\[sn\_uni\_req.routing\_agent\]

</td><td>

Responsible for initial triaging of the universal requests and routing them to right department or queues. **Note:** Only users with this role can have universal requests assigned to them.

</td><td>

sn\_uni\_req.universal\_request\_write

</td></tr><tr><td>

Universal Request read\[sn\_uni\_req.universal\_request\_read\]

</td><td>

Access to view the Universal Request records.

</td><td>

None

</td></tr><tr><td>

Universal Request write\[sn\_uni\_req.universal\_request\_write\]

</td><td>

Access to create or update the universal request in the application.

</td><td>

sn\_uni\_req.universal\_request\_read

</td></tr><tr><td>

Universal Request admin\[sn\_uni\_req.ur\_admin\]

</td><td>

View the configuration of the Universal Request application.

</td><td>

sn\_uni\_req.routing\_agent

</td></tr><tr><td>

Universal Request Service Owner\[sn\_uni\_req.ur\_service\_owner\]

</td><td>

Access the process overview reports of the Universal Request application.

</td><td>

None

</td></tr><tr><td>

Universal Request SensitiveInfo Agent\[sn\_uni\_req.sensitiveinfo\_agent\]

</td><td>

View and work on the tickets that are marked as **Restricted**. Restricted tickets contain sensitive information and are secured from general viewing.

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Universal Request\[universal\_request\]

</td><td>

Stores the Universal Request records and the state reasons.

</td></tr><tr><td>

Transfer Configuration

 \[universal\_request\_route\_conf\]

</td><td>

Holds the routing configuration that is used when the task is routed.

</td></tr><tr><td>

Service Assignment Group\[universal\_request\_service\_assignment\_group\]

</td><td>

Stores the assignment group details of different services configured in UR.

</td></tr><tr><td>

State Mapping\[universal\_request\_state\_mapping\]

</td><td>

Holds the state mapping configuration that maps the department ticket states to the Universal Request states.

</td></tr><tr><td>

Service Configuration\[universal\_request\_service\_conf\]

</td><td>

Stores the details of the services that are configured in the Universal Request application.

</td></tr><tr><td>

Service set\[universal\_request\_service\_set\]

</td><td>

Stores the service set \(department\) details of the organization.

</td></tr><tr><td>

Service Set Assignment Group\[universal\_request\_service\_set\_assignment\_group\]

</td><td>

Stores the assignment group details of the service set \(department\).

</td></tr><tr><td>

SLA Breakdown by Primary ticket and Assignment group\[sla\_breakdown\_by\_primary\_ticket\_and\_group\]

</td><td>

 

</td></tr><tr><td>

Mapping Configuration\[universal\_request\_transfer\_mapping\]

</td><td>

 

</td></tr><tr><td>

Transfer Fields Mapping\[universal\_request\_transfer\_fields\_mapping\]

</td><td>

 

</td></tr><tr><td>

Universal Request Priority Data Lookup\[dl\_universal\_request\_priority\]

</td><td>

 

</td></tr><tr><td>

Universal Request Activity Log\[universal\_request\_activity\_log\]

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Activate Universal Request](../task/activate-ur-plugin.md)

