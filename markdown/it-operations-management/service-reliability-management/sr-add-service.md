---
title: Add a service to SRM
description: Add services to Service Reliability Management \(SRM\) to help your teams manage service health.
locale: en-US
release: yokohama
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Working with SRM services, Using Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Add a service to SRM

Add services to Service Reliability Management \(SRM\) to help your teams manage service health.

## Before you begin

If you’re adding a technical service to SRM, make sure it doesn’t have a support group. You assign the support group when you add the service to SRM.

Role required: srm\_admin, srm\_manager, or srm\_responder

## About this task

Add a service to SRM to assign it to your teams and let them access its incidents and alerts. You can either create a service or import an existing one. SRM supports both application and technical services:

-   Application services - Business-facing services, such as an HR portal. Application services often have multiple infrastructure components.
-   Technical services - IT-focused services that support a business or application service. For example, an authentication service or database service.

When you add a technical service to SRM, you also add its Technical Service Offerings \(TSOs\). TSOs are specific components within a parent technical service. For example, Spam filtering is a TSO within the Email technical service. In SRM, you can assign a parent technical service and its TSOs to different teams.

**Note:** When you import an existing technical service, its TSOs don’t inherit its support group. TSOs either keep their existing support group or, if they don’t have one, you must assign it before setting up SRM Service Level Objectives \(SLOs\).

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You're taken to your SRM Home page.

    **Note:** If you use other Service Operations Workspace \(SOW\) applications, you may see the SOW Home page instead of the SRM Home page. The SOW Home page includes SRM alerts and incidents in its metrics.

2.  Select the Services icon ![Services page icon](../image/icon-sr-services.png) and then select **Add a service**.

3.  In the Add services for your teams modal, you can either create a service or add existing services.

<table id="choicetable_m3m_brg_n1c"><thead><tr><th align="left" id="d104802e148">

Option

</th><th align="left" id="d104802e151">

Steps

</th></tr></thead><tbody><tr><td id="d104802e157">

**Create a new service**

</td><td>

1.  Select **Create a new service**.
2.  Fill in the fields. For field descriptions, see [Add service form](../reference/sr-add-service-form.md).
3.  Select **Next**.


</td></tr><tr><td id="d104802e195">

**Select existing services**

</td><td>

1.  Select **Select existing services**.
2.  Search for and select your service. You can add more than one.
3.  Select **Next**.
 **Tip:** Select the search box to view up to 25 services not yet in SRM, ordered by creation time. After you enter three characters, it shows up to 25 matching results. Both lists can include services with or without a support group. If a service has one, the support group can be an SRM team or a group outside SRM.

</td></tr></tbody>
</table>4.  In the Assign a team step, assign your service to an existing or new support group.

    In SRM, support groups are also known as teams.

    |Option|Steps|
    |------|-----|
    |**Select an existing team**|Enter your team's name in the search box.|
    |**Create a team**|Select **Create a team**. For more information about creating teams, see [Add an SRM team](sr-create-team.md).|

5.  Select **Add service**.

    If approvals aren't enabled, your service appears in the service list. If approvals are enabled, your request is sent for approval. After it's approved, the service appears in the services list.

    **Note:** If you added a technical service, its TSOs appear in the Offerings tab on the parent technical service’s page. TSOs also appear in the services list. To view a TSO without an assigned support group, remove all filters from the services list.


## What to do next

If a TSO doesn't have a support group, assign it to a support group before setting up SLOs. For how to assign support groups, see [Edit SRM service details](sr-edit-service.md).

You can also add integrations to your service to start monitoring its health.

-   **[Working with SRM integrations](../concept/sr-work-integrations.md)**  
Connect your services to monitoring tools using the Integrations Launchpad . Integrations send information to Service Reliability Management \(SRM\), helping you track alerts, manage incidents, and maintain service health.

**Parent Topic:**[Working with SRM services](../concept/sr-work-services.md)

