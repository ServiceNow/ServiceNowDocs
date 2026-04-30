---
title: Adding additional managers
description: Appointing additional managers in your organization ensures the continuity of work in the absence of a primary manager.Appoint additional internal managers for an outsourced service provider to manage contractor companies and their employees in the absence of its primary internal contractor manager.Appoint additional external managers for an outsourced service provider to manage the agents and work of contractor companies in the absence of a primary external manager of the contractor company.
locale: en-US
release: xanadu
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Contractor Management, Configuring contractor capabilities, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Adding additional managers

Appointing additional managers in your organization ensures the continuity of work in the absence of a primary manager.

You can appoint additional managers for the external assignment groups of contractor companies.

Roles and responsibilities of additional managers:

-   **Internal manager**
    -   Onboard contractor companies and their employees
    -   Approve or reject onboarding agent requests
    -   Assign work to the contractor companies and their workforce
    -   Track the progress of work order tasks assigned to the contractor companies using the Contractor dashboard.
-   **External manager**
    -   Onboard agents for contractor companies
    -   Assign and manage work order tasks to the contractor agents using the Field Service Contractor portal.

**Note:** An off-boarded agent automatically gets deleted from the additional manager role if assigned to. For more information, see [Offboard agents on the Field Service Contractor Portal](../task/offboard-agents-fsmcp.md).

## Add additional internal managers

Appoint additional internal managers for an outsourced service provider to manage contractor companies and their employees in the absence of its primary internal contractor manager.

### Before you begin

Assign wm\_int\_contractor\_manager role to the employee of an internal company whom you want to add as additional internal manager. For more information, see [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Role required: admin, wm\_admin, or wm\_int\_contractor\_manager

### Procedure

1.  Navigate to **All** &gt; **Application** &gt; **Outsourced Field Service Providers**.

2.  Select a contractor company from the **Outsourced Service Providers** list.

3.  In the Internal Contractor Managers related list, click **Edit**.

4.  In the Collection list, select the desired user, and then click Add.

    **Note:** Collection list displays the users with wm\_int\_contractor\_manager role only.

5.  Click **Save**.


### Result

The additional internal manager is added to the company.

## Add additional external manager

Appoint additional external managers for an outsourced service provider to manage the agents and work of contractor companies in the absence of a primary external manager of the contractor company.

### Before you begin

Role required: admin, wm\_admin, or wm\_int\_contractor\_manager

Assign wm\_ext\_agent role to the employee of an external company whom you want to add as additional external manager. For more information, see [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

**Note:** The agent to be appointed as an additional external manager, should be the member of the assignment group of the same outsourced service provider.

### About this task

Internal manager of a company can onboard field service agents for contractor companies and also appoint them as additional external managers to manage the managerial activities of contractor companies.

External manager of the contractor company can also assign additional manager role to a field service agent while on boarding them or later. For more information, see [Onboard agents on the Field Service Contractor Portal](../task/onboard-field-service-agent.md) and [Assign additional manager assignments to an agent](../task/assign-additional-manager-assignments.md).

This procedure explains how an internal manager can onboard additional external manager using ServiceNow AI Platform.

### Procedure

1.  Navigate to **All** &gt; **Application** &gt; **Outsourced Field Service Providers**.

2.  Select a contractor company from the **Outsourced Service Providers** list.

3.  In the Groups related list, open the assignment group for which you want to appoint an additional manager.

    For example, Acme Services.

4.  In the Additional Managers related list, click **Edit**.

5.  In the Collection list, select the desired user, and then click Add.

6.  Click **Save**.


### Result

The additional external manager is added to the company.

