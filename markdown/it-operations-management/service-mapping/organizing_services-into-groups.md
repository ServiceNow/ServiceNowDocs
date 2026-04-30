---
title: Group application services
description: Organize application services by groups to perform actions simultaneously on multiple services, and to control user access to services. You can use Event Management to track service health by service groups.
locale: en-US
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Application service completion, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Group application services

Organize application services by groups to perform actions simultaneously on multiple services, and to control user access to services. You can use Event Management to track service health by service groups.

## Before you begin

Role required: service\_mapping\_admin or app\_service\_admin

## About this task

Typically, enterprises have hundreds of services which makes it impractical to manage them individually. Service groups can make service lists much shorter and easier to manage, especially in large organizations or service providers.

How you group service instances depends on the user and on service provisioning policies in your enterprise. The relation between service instances in groups is purely logical and the same service instance can belong to multiple groups. For example, the Mobile service can be part of the following service groups: Sales, Beijing, and Telephony.

![A service instance belonging to different groups](../image/BusinessService3Groups.png "Example of a service instance belonging to different groups")

You can embed a service group within another service group to create a hierarchy of service groups. If users have access to a parent service group, they automatically have access to all its child groups. By default, all new services are assigned to the **All** service group that lets all users view and manage service instances. When you assign a role to a service group, the users with this role can access service instances in this service group and in the **All** service group. To enable users with this role to access other services, assign this role to the respective service group. Do not assign user roles directly to the **All** service group.

If Service Mapping is activated, service groups can contain a mixture of manually created application services and application services discovered by Service Mapping.

You can use ServiceNow AI Platform Notifications to alert users if the service group severity changes to critical. The overall severity of the group is determined by the highest alert severity within the group.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Application Services** &gt; **Service Groups**.

2.  Click **New**.

3.  Enter the name of the new service instance group in the **Name** field.

4.  To embed this group in another group, enter the name of the other group in the **Parent Group** field.

5.  Right-click the form header and click **Save**.

6.  Add a service instance to the newly created service group.

    1.  In the Service Group Members section, click **New**.

    2.  In the **Name** field, enter the name of the service instance.

        If you are using Event Management, you can also enter an alert group name.

    3.  Click **Submit**.

7.  Alternatively, add a service instance to a group from the service instance form.

    1.  Navigate to **All** &gt; **Configuration** &gt; **Service Instances** &gt; **Service Instances**.

    2.  Select the service instance you want to add to a service group.

    3.  In the **Service Group Members** section, double-click **Insert a new row**.

    4.  Enter the name of the service group to which you want to add the selected service instance.

    5.  Click the **OK** icon \(![OK icon](../image/BusinessMappingOKicon.png)\).

    6.  Click **Update**.


**Parent Topic:**[Application service completion](../concept/advanced-business-service-definitions.md)

**Related topics**  


[Define criticality for application services](define-criticality-for-business-services.md)

[Control user access to application services](control-user-access-to-business-services.md)

[Schedule a top-down discovery by Service Mapping](t_CreateDiscoSchedForCITypes.md)

[Service definition transfer from one instance to another](../concept/transfer-service-definitions.md#)

