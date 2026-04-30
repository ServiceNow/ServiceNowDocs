---
title: Control user access to application services
description: Assign user roles to service groups to grant users access to application services in your organization. Your organization may restrict access to some services for security or secrecy reasons.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Application services, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Control user access to application services

Assign user roles to service groups to grant users access to application services in your organization. Your organization may restrict access to some services for security or secrecy reasons.

## Before you begin

Make sure that you have performed the user provisioning tasks for the users you want to grant access:

1.  [Add users to user groups](https://www.servicenow.com/docs/access?context=t_CreateAGroup&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
2.  [Create new roles](https://www.servicenow.com/docs/access?context=t_CreateARole&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
3.  [Assign roles to users or user groups](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Also, make sure that you have created service groups as described in [Group application services](organizing_services-into-groups.md).

Role required: app\_service\_admin or service\_mapping\_admin

## About this task

In the base system, the following roles provide access to application services:

-   **app\_service\_admin**

    Creates and modifies service instances, creates service groups, views, and edits service instance maps.

-   **app\_service\_user**

    Views maps for operational service instances and retrieves service content using the getContent - GET REST API. The itil role that serves as the basic helpdesk technician role contains the app\_service\_user role.


Service Mapping provides these preconfigured roles:

-   **service\_mapping\_admin**

    Sets up the Service Mapping application. Maps, fixes, and maintains service instances. Also performs advanced configuration and customization of the product. Assign this role to application administrators.

-   **service\_mapping\_user**

    Views maps for operational service instances to plan change or migration, as well as analyze the continuity and availability of services. Assign this role to application users.

-   **sm\_app\_owner**

    Provides information necessary for successful mapping of a service instance. Once a service is mapped, this user reviews the results and either approves it or suggests changes. Assign the sm\_app\_owner role to users who own service instances and are familiar with the infrastructure and applications that make up the services.


**Note:** Users with the itil role only can view all service instances.

Event Management provides these preconfigured roles:

-   **evt\_mgmt\_admin**

    Has read and write access to all Event Management features to configure Event Management.

-   **evt\_mgmt\_operator**

    In addition to the evt\_mgmt\_user permissions, can also activate operations on alerts such as acknowledge, close, open incident, and run remediations.

-   **evt\_mgmt\_user**

    Has read access to all Event Management features. Has write access to alerts to manage the alert life. Has the itil role to be able to manage incidents that are created from alerts.

-   **evt\_mgmt\_integration**

    Has create access to the Event \[em\_event\] and Registered Nodes \[em\_registered\_nodes\] tables to integrate with external event sources.


Typically, enterprises have hundreds of services which makes it impractical to manage them individually. Service groups can make service lists much shorter and easier to manage, especially in large organizations or service providers. In a hierarchy of service groups, access to a parent service group automatically grants access to all the child service groups.

Users inherit permissions from roles that are assigned to them. You can assign some roles directly to service groups to allow all users with this role to access all application services belonging to this group. However, most enterprises choose to organize their roles as a hierarchy. It helps to manage roles across multiple ServiceNow applications. For example, the Service Mapping administrator \[service\_mapping\_admin\] can be part of a broader administrator role like administrator \[admin\]. You can add users to user groups and then assign roles to the user groups to give permissions of this role simultaneously to all the group users.

![Assigning a role to an service instance group for user access](../image/AccessToBusinessServiceGroups.png "Assigning a role to an application service group")

By default, all new services are assigned to the **All** service group that lets all users view and manage application services. When you assign a role to a service group, the users with this role can access application services in this service group and in the **All** service group. To enable users with this role to access other services, assign this role to the respective service group. Do not assign user roles directly to the **All** service group.

## Procedure

1.  Navigate to either of the following:

    -   **Configuration** &gt; **Application Services** &gt; **Service Group Responsibilities**.
    -   If Service Mapping is activated: **Service Mapping** &gt; **Services** &gt; **Service Group Responsibilities**.
    -   If Event Management is activated: **Event Management** &gt; **Services** &gt; **Service Group Responsibilities**.
2.  Click **New** and fill out the Application Service Group Responsibilities form.

<table id="table_kgf_xpc_12b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application Service Group

</td><td>

Service group to which you want to assign a role.

</td></tr><tr><td>

Role

</td><td>

Role you want to assign to the selected service group.

 For example, financial\_services\_admin.

</td></tr></tbody>
</table>3.  Click **Submit**.


## Example

To manage access to services that contain sensitive financial information in your organization:

1.  Organize the services into the Financial Services group.
2.  Create a new user role, financial services administrator \[financial\_services\_admin\] role, that contains the \[app\_service\_admin\] role.
3.  Assign the Financial Services administrator role to the Financial Services group.

As a result, only users with the Financial Services administrator role can access application services belonging to the Financial Services group.

