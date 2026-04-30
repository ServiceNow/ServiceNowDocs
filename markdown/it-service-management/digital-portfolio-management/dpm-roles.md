---
title: Roles for Digital Portfolio Management
description: Several types of components are installed with Digital Portfolio Management \(DPM\) when you activate the application from the ServiceNow ServiceNow Store. DPM has two roles - admin and user.
locale: en-US
release: xanadu
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Digital Portfolio Management reference, Digital Portfolio Management, IT Service Management]
---

# Roles for Digital Portfolio Management

Several types of components are installed with Digital Portfolio Management \(DPM\) when you activate the application from the ServiceNow® ServiceNow Store. DPM has two roles - admin and user.

## Roles installed with DPM

There are two roles for DPM.

-   The DPM admin \[sn\_dpm.dpm\_admin\] role configures the DPM Workspace for users. The DPM admin role can create, retrieve, update, and delete \(CRUD\) all personal portfolios created by anyone. The DPM admin role can also assign the DPM manager role to groups so a personal portfolio owner can select groups to view or edit personal portfolios.
-   The DPM manager \[sn\_dpm.dpm\_manager\] role is the end user of the DPM Workspace. The DPM manager role can only CRUD personal portfolios that they create.

See the following table for information about each role.

<table id="table_fbd_qxp_dlb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

DPM admin \[sn\_dpm.dpm\_admin\]

</td><td>

-   View all DPM system properties and admin pages.
-   Update all DPM system properties.

**Note:** The DPM Admin role can't CRUD service portfolios unless they have the appropriate service portfolio admin or manager roles from Service Portfolio Management.

-   Use Key performance indicator \(KPI\) functions:
    -   View KPI group tables for KPI groups and KPI group mappings.
    -   Create KPI groups.
    -   Update and delete all KPI groups.
    -   Map KPI groups.

</td><td>

-   sn\_dpm.dpm\_manager
-   sn\_ep.enterprise\_portfolio\_admin \(can CRUD enterprise portfolios that are created using the enterprise portfolio tables\).

**Important:** The DPM admin only gets this role if you install the enterprise portfolio plugin. After you install the plugin:

    -   The DPM admin role inherits the enterprise portfolio admin role.
    -   The DPM manager role inherits the enterprise portfolio viewer role.

</td></tr><tr><td>

DPM Manager \[sn\_dpm.dpm\_manager\]

</td><td>

-   Retrieve and update personal portfolios that they’re editors of.
-   Retrieve personal portfolios that they’re viewers of.
-   Read all available data in the DPM Workspace.
-   Create demands.
-   Create Continual Improvement Management \(CIM\) items.
-   Update roadmaps.
-   View KPIs in the DPM Workspace.

**Note:** The DPM manager can't view or map KPI groups in the ServiceNow AI Platform but users with the service\_editor, service\_admin, or service\_author roles can map KPI groups to their services.

-   Functions that the DPM manager can't do:
    -   Edit services, offerings, business applications, or application services.
    -   Edit and update relationships to services, offerings, business applications, or application services.
    -   Create or edit a service in Service Builder.

**Note:** Service Builder buttons are hidden for the DPM manager role unless the user has the correct role that provides edit access to a particular solution.


</td><td>

-   sn\_devops.viewer
-   cmdb\_read
-   sn\_team\_perf.team\_performance\_user
-   service\_viewer
-   sn\_ep.enterprise\_portfolio\_viewer

</td></tr></tbody>
</table>## Assign the DPM manager role to groups

To edit a personal portfolio, a group must have the DPM manager role.

To assign the DPM manager role to a group, the admin does the following:

1.  Enter `dpm_personal_portfolio.list` in the Filter navigator.
2.  Open the personal portfolio record that you want to assign the DPM manager role.
3.  Select **Edit user groups**, and then search for the user groups to add to the DPM manager role.
4.  Repeat the previous step for **View user groups** if you want to add the DPM manager role to the groups that view personal portfolios.
5.  Select **Update**.

## Tables installed with DPM

|Table|Description|
|-----|-----------|
|dpm\_available\_item\_type|Stores records for each type in a personal portfolio.|
|dpm\_navigation\_history|Stores records for navigating each type in a personal portfolio.|
|dpm\_personal\_portfolio|Stores records for each created personal portfolio.|
|dpm\_personal\_portfolio\_item|Stores records for all types that are in a personal portfolio.|
|dpm\_unified\_backlog|Stores records for backlog information in a personal portfolio.|
|sn\_dpm\_kpi\_group\_m2m\_spm\_nodes|Stores records for key performance indicator \(KPI\) group nodes from Service Portfolio Management.|
|sn\_dpm\_kpi\_group\_m2m\_viz\_config|Stores records for KPIs grouped by data visualization.|
|sn\_team\_perf\_kpi\_group|Stores records for KPIs grouped by team performance.|

**Parent Topic:**[Digital Portfolio Management reference](dpm-reference-cfw.md)

**Related topics**  


[Activate Digital Portfolio Management](../task/dpm-activate.md)

