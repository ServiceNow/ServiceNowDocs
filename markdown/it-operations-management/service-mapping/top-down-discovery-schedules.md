---
title: Top-down discovery schedules
description: Learn about schedules that trigger top-down discovery of application services.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Schedule a top-down discovery by Service Mapping, Application service completion, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Top-down discovery schedules

Learn about schedules that trigger top-down discovery of application services.

When you define a new application service, Service Mapping performs discovery of all CIs that participate in this application service and creates its map. After the initial mapping is complete, Service Mapping regenerates application service maps regularly by rediscovering the CIs making up an application service.

By default, Service Mapping is preconfigured with these generic schedules:

-   **All Applications**

    This schedule triggers the top-down discovery of all CIs of the application type \[cmdb\_ci\_appl\].

-   **Load Balancer Service**

    This schedule starts the top-down discovery of all CIs of the load balancer service type \[cmdb\_ci\_lb\_service\].


The generic schedules trigger discovery of all applications and load balancer services in your organization once a day. Typically, these preconfigured schedules are enough to update information for application services. However, if it is necessary to discover specific CIs or services more frequently, you can create the following custom discovery schedules:

<table id="table_knt_3pl_bhb"><thead><tr><th>

Schedule type

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Services

</td><td>

Service Mapping discovers all CIs belonging to certain services that answer filtering criteria.

</td><td>

In your organization, some application services are more critical than others and it is important for you to rediscover such services with high criticality more frequently. Create a custom discovery schedule to discover all services with the business criticality value set to **most critical**. Alternatively, certain services in your organization are undergoing changes more often than once a day. You may want to create custom schedules to rediscover such services more frequently.

 You can also create a schedule of this type to discover application services in a sub-production instance, where services are not in the **operational** state yet.

</td></tr><tr><td>

Services belonging to a group

</td><td>

Service Mapping discovers all CIs belonging to services assigned to groups that answer filtering criteria. Service Mapping discovers only services located directly inside the group that answers defined filtering criteria. Service Mapping does not discover services inside embedded groups.

 Notice that you can define schedules based on service groups, even if your role does not have access to these service groups.

</td><td>

In a distributed organization with offices in several geographic locations, you may want to create a custom discovery schedule to rediscover services in one of these locations. For example, one schedule can trigger rediscovery of all services relevant for the EMEA site at 7am GMT, while another schedule can start rediscovery of services for the US headquarters at 7am PT.

</td></tr><tr><td>

For CI types

</td><td>

Service Mapping discovers all application CIs belonging to this application type. Some application CI types are prone to more frequent changes and updates than others, so you can manage the load by adjusting the discovery schedule to match the nature of each CI type. When you define discovery schedules based on application CI types, several schedules may apply to the same CI. To avoid discovering the same CIs more than once, the most specific schedule always has precedence. For example, if you create separate discovery schedules for a parent CI type and its child CI type, CIs belonging to the child CI type are discovered using its dedicated schedule. At the same time, if there is no schedule for a child CI type, the parent CI type schedule is used to discover the child CIs.

 This schedule discovers only CIs belonging to application services in the **operational** state.

</td><td>

If you modify a certain application more often than the rest of your applications, you may want to discover it more frequently than other CIs. In that case, create a custom discovery schedule for such an application CI type.

</td></tr><tr><td>

Specific CIs

</td><td>

Service Mapping discovers only one CI that you specified for this schedule.If you define a discovery schedule for a specific CI as well as a schedule for the CI type to which this CI belongs, Service Mapping uses the schedule for this specific CI, and not the generic schedule for its CI type.

 This schedule discovers only CIs belonging to application services in the **operational** state.

</td><td>

For rare cases of rediscovering a specific CI that causes discovery errors frequently.

</td></tr></tbody>
</table>Part of discovering an application CI is identifying its host. Service Mapping checks if the device hosting this application CI exists in the CMDB. For a load balancer service, Service Mapping checks if the load balancing device hosting this load balancer service exists in the CMDB. If not, Service Mapping triggers Discovery to perform the horizontal discovery. As a result, Discovery performs host detection and updates the information on hosts in the CMDB. If necessary, you can manage the schedules that trigger horizontal discovery as described in:

-   [Schedule a horizontal discovery](../../discovery/task/t_CreateADiscoverySchedule.md#) — for standard horizontal discovery.
-   [Create a schedule for standard serverless Discovery](../../discovery/task/create-pattern-for-serverless.md#) — for discovering CIs using a protocol such as REST, without using the IP address of any devices or hosts.
-   [Create a schedule for host-based serverless Discovery](../../discovery/task/create-pattern-for-proxy-serverless.md#) — for discovering CIs that reside on an already discovered host using this host as a Proxy server.

**Parent Topic:**[Schedule a top-down discovery by Service Mapping](../task/t_CreateDiscoSchedForCITypes.md)

**Related topics**  


[Schedule a top-down discovery by Service Mapping](../task/t_CreateDiscoSchedForCITypes.md)

