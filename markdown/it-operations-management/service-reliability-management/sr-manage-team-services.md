---
title: Manage or add a service to your SRM team
description: Add a service to an incident to increase the amount of data for the incident.
locale: en-US
release: australia
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Add an SRM team, Working with SRM teams, Using Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Manage or add a service to your SRM team

Add a service to an incident to increase the amount of data for the incident.

## Before you begin

Role required: srm\_manager, srm\_responder, or srm\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You're taken to your SRM Home page.

    **Note:** If you use other Service Operations Workspace \(SOW\) applications, you may see the SOW Home page instead of the SRM Home page. The SOW Home page includes SRM alerts and incidents in its metrics.

2.  From the primary navigation, select **Teams** \(![Teams.](../image/icon-sr-teams.png)\).

3.  Select a team card to open any team you want to view or add a service to.

4.  From the team page, select the **Services managed** tab.

    You can export the list of services. See [Export list information to a file](sr-export-to-file.md) for more information.

5.  Add a service to your team by selecting **Add**.

6.  Add a new service or register an existing one.

<table id="choicetable_m3m_brg_n1c"><thead><tr><th align="left" id="d230810e135">

Option

</th><th align="left" id="d230810e138">

Steps

</th></tr></thead><tbody><tr><td id="d230810e144">

**Add a new service**

</td><td>

1.  In the **New or existing** field, select **Create a new service in Service Reliability Management**.
2.  On the form, fill in the fields.

For more information on the field descriptions, see [Add service form](../reference/sr-add-service-form.md).

3.  Select **Next**.


</td></tr><tr><td id="d230810e186">

**Register an existing service**

</td><td>

1.  In the **New or existing** field, select **Associate existing CMDB services to Service Reliability Management**.
2.  Select one or more services.
3.  Select **Next**.


</td></tr></tbody>
</table>7.  In the Assign a team step, fill in the fields.

    -   In the **Service owner** field, select the user who will own the services.
    -   In the **Support Group** field, select a team that will monitor services.
    The service record has been added.

8.  Finish setting up your service or do it later.

<table id="choicetable_mrc_vh1_lbc"><thead><tr><th align="left" id="d230810e252">

Option

</th><th align="left" id="d230810e255">

Steps

</th></tr></thead><tbody><tr><td id="d230810e261">

**Finish setting up your service**

</td><td>

1.  Select **Continue to setup**.
2.  Select **Add integrations** and connect your service to a data source to monitor events.
3.  Select **Add SLO &amp; SLI** and create a service level objective and measure your service health with a service level indicator.


</td></tr><tr><td id="d230810e291">

**Do it later**

</td><td>

Select **Do it later**.

</td></tr></tbody>
</table>    See [Edit service details in SRM](sr-edit-service.md) and [Edit service details form](../reference/sr-edit-service-form.md)for information on the service and completion steps for setup.


**Parent Topic:**[Add an SRM team](sr-create-team.md)

