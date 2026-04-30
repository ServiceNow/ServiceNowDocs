---
title: Components installed with Continual Improvement Management
description: Several types of components are installed with activation of the com.sn\_cim plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: xanadu
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Continual Improvement Management reference, Continual Improvement Management, IT Service Management]
---

# Components installed with Continual Improvement Management

Several types of components are installed with activation of the com.sn\_cim plugin, including tables, user roles, and scheduled jobs.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

## Roles installed with Continual Improvement Management

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Roles inherited

</th></tr></thead><tbody><tr><td>

Improvement Requester

 \[sn\_cim.improvement\_requester\]

</td><td>

Able to perform these application functions:-   Create improvement initiative
-   View **My CIM requests**
-   View **Watched CIM requests**
-   View **All** CIM requests

</td><td>

None

</td></tr><tr><td>

Improvement Coordinator

 \[sn\_cim.improvement\_coordinator\]

</td><td>

Able to perform all functions for improvements to which they are assigned as Improvement Coordinator except:-   Create Enterprise Strategies
-   Delete improvement

 Although able to perform Improvement Manager functions, an Improvement Coordinator can only perform those functions for improvements that they are assigned as Improvement Coordinator by the Improvement Manager.

 Primary responsibility is to coordinate improvements within their area of expertise \(at the process or service level\).

 Can access both Continual Improvement Workbench and dashboard.

</td><td>

-   sn\_cim.improvement\_requester
-   app\_service\_user
-   certification
-   cmdb\_query\_builder
-   dependency\_views
-   itil

Problem/change/incident records can be added.

-   knowledge
-   pa\_analyst
-   pa\_contributor
-   pa\_power\_user

Existing Performance Analytics indicators can be accessed, and new ones created.

-   pa\_target\_admin
-   pa\_threshold\_admin
-   pa\_viewer
-   sn\_bm\_client.benchmark\_data\_viewer
-   sn\_bm\_client.benchmark\_recommendation\_viewer

Benchmarks data and recommendations can be viewed and an improvement initiative can be created from Benchmarks recommendations.

-   template\_editor
-   view\_changer
-   sn\_coaching.admin
-   scrum\_story\_creator

</td></tr><tr><td>

Improvement Manager

 \[sn\_cim.improvement\_manager\]

</td><td>

Able to perform all application functions. The Improvement Manager is primarily responsible for all improvements, including initial acceptance of new improvement requests, assignment, and closure. The Improvement Manager also monitors the overall progress of all improvements.

</td><td>

-   sn\_cim.improvement\_coordinator
-   sn\_process\_optimization\_viewer

</td></tr></tbody>
</table>## Scheduled jobs installed with Continual Improvement Management

|Scheduled job|Description|
|-------------|-----------|
|\[PA Continual Improvement\]|Daily CIM data collection.|
|\[PA Continual Improvement\]|Historical CIM data collection.|

## Tables installed

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

Contains M2M tables to integrate Continual Improvement Management with other ServiceNow applications. With an inbound CIM integration, you can create a CIM record from the application that is integrated with Continual Improvement Management.

</td></tr><tr><td>

Outbound CIM Integration\[sn\_cim\_outbound\_m2m\]

</td><td>

Contains M2M tables that integrates other ServiceNow applications withContinual Improvement Management. With an outbound CIM integration, you can create an outcome based on the integrated application, for example, a story or knowledge article from a CIM record.

</td></tr></tbody>
</table>## Properties installed with Continual Improvement Management

To access Continual Improvement Management properties, navigate to **Continual Improvement** &gt; **Administration** &gt; **Properties**.

**Note:** System admin role is required to set Continual Improvement Management properties.

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

When a copy of the improvement initiative is created, the list of attributes \(field values\) that will be copied to the new initiative.

</td></tr><tr><td>

sn\_cim.create\_default\_phase

</td><td>

Enable the property to create the default phase when an improvement initiative is created.-   Type: Yes\|No
-   Default value: No

</td></tr></tbody>
</table>**Parent Topic:**[Continual Improvement Management reference](cim-reference.md)

