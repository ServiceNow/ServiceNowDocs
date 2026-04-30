---
title: Components installed with Continual Improvement Management
description: Several types of components are installed with the CIM plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: yokohama
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Continual Improvement Management reference, Continual Improvement Management, IT Service Management]
---

# Components installed with Continual Improvement Management

Several types of components are installed with the CIM plugin, including tables, user roles, and scheduled jobs.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

## Roles

-   Improvement Requester \[sn\_cim.improvement\_requester\]
-   Improvement Coordinator \[sn\_cim.improvement\_coordinator\]
-   Improvement Manager \[sn\_cim.improvement\_manager\]

For more information about the inherited roles and functions that users with different CIM roles can perform, see [CIM roles](cim-roles.md).

## Scheduled jobs

|Scheduled job|Description|
|-------------|-----------|
|\[PA Continual Improvement\]|Daily CIM data collection.|
|\[PA Continual Improvement\]|Historical CIM data collection.|

## Tables

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Improvement Initiative\[sn\_cim\_register\]

</td><td>

Contains all improvement initiatives.

</td></tr><tr><td>

CIM Task\[sn\_cim\_task\]

</td><td>

Contains the CIM tasks created for an improvement initiative.

</td></tr><tr><td>

Impacted KPIs\[sn\_cim\_related\_kpi\]

</td><td>

Contains KPIs related to the CIM improvement initiative.

</td></tr><tr><td>

Inbound CIM Integration\[sn\_cim\_inbound\_m2m\]

</td><td>

Contains M2M tables to integrate CIM with other ServiceNow applications. With an inbound CIM integration, you can create a CIM record from the application that is integrated with CIM.

</td></tr><tr><td>

Outbound CIM Integration\[sn\_cim\_outbound\_m2m\]

</td><td>

Contains M2M tables that integrates other ServiceNow applications withCIM. With an outbound CIM integration, you can create an outcome based on the integrated application, for example, a story or knowledge article from a CIM record.

</td></tr></tbody>
</table>## Properties

To access CIM properties, navigate to **Continual Improvement** &gt; **Administration** &gt; **Properties**.

**Note:** System admin role is required to set CIM properties.

<table id="table_k5g_bfn_mnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_cim.need\_approval

</td><td>

Enables approval process for Continual Improvement initiatives. By default, an improvement requires approval before it can progress to the Implement state. When the check box is enabled, it indicates that manual approval is required for the improvement to progress from Accepted state to Approved state.-   Type: Yes\|No
-   Default value: Yes

 If this property is not checked, the improvement automatically progresses to Approved state once it is accepted, and the **Approver group** field and the **Approvers** related list on the Improvement Initiative form are not shown.

</td></tr><tr><td>

sn\_cim.initiative\_copy\_attributes

</td><td>

List of comma-separated attributes or field values copied from the improvement initiative or CIM task to the application task record \(example, demand, project, change record\) created from the improvement initiative.-   Short description \(short\_description\)
-   Description \(description\)
-   Priority \(priority\)
-   CIM estimate \(cim\_estimate\)
-   Benefit \(benefit\)
-   Assigned to \(assigned\_to\)
-   Strategic objective \(strategic\_objective\)
-   Business process \(business\_process\)
-   Business service \(business\_service\)
-   Approver group \(approver\_group\)
-   Type \(type\)

</td></tr><tr><td>

sn\_cim.create\_default\_phase

</td><td>

Enable the property to create the default phase when an improvement initiative is created.-   Type: Yes\|No
-   Default value: No

</td></tr></tbody>
</table>**Parent Topic:**[Continual Improvement Management reference](cim-reference.md)

