---
title: Choose the right method for discovery and mapping application services
description: Service Mapping deploys different methods for collecting information about configuration items \(CIs\) and organizing them into application services. The available mapping methods are: pattern-based, tag-based, traffic-based, and discovery based on Predictive Intelligence. Learn about the mapping methods to use the ones that best suit the needs of your organization.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Choose the right method for discovery and mapping application services

Service Mapping deploys different methods for collecting information about configuration items \(CIs\) and organizing them into application services. The available mapping methods are: pattern-based, tag-based, traffic-based, and discovery based on Predictive Intelligence. Learn about the mapping methods to use the ones that best suit the needs of your organization.

<table id="mapping-method-comparison"><thead><tr><th>

Mapping method

</th><th>

Description

</th><th>

Advantages

</th><th>

Disadvantages

</th></tr></thead><tbody><tr><td>

[Automated Service Suggestions](auto-serv-suggest.md)

</td><td>

Predictive Intelligence evaluates connections between application fingerprints, CIs, and processes, and ranks their relevancy. Service Mapping uses this information to create connections based on connection rules. It also generates connection suggestions for servers and load balancers for you to decide which connections to add or remove from the service instances.

</td><td>

Service Mapping automatically adds CI connections and CIs they lead to based on connection rules. You can modify the default connection rules or create your own to enhance this discovery method.Discovery based on Predictive Intelligence is effective for mapping multiple application services.

</td><td>

When using discovery based on Predictive Intelligence to identify TCP connections and processes, deploy it in large on-premise deployments. Predictive Intelligence is a machine learning solution and needs training. To achieve best results using this discovery method, you must run discovery repeatedly.

 Service Mapping may erroneously add or remove dynamic connections.

</td></tr><tr><td>

[Pattern-based discovery](pattern-based-discovery.md)

</td><td>

Service Mapping uses patterns to discover and map CIs. A pattern is a sequence of commands designed to detect attributes of a CI and its outbound connections. A typical Service Mapping pattern consists of separate algorithms for identifying CIs and finding CI connections.

</td><td>

Pattern-based discovery creates precise and complete service instances that reliably represent the service-aware view of your organization's IT infrastructure.

</td><td>

Pattern-based mapping requires configuring credentials, users, and user permissions to let Service Mapping access applications inside your organization private network. This process may take time and effort.

</td></tr><tr><td>

[Tag-based discovery](tag-based-mapping.md)

</td><td>

If your organization uses tags for asset management, you can use these tags to map service instances. Discovery and Cloud Provisioning and Governance discover tags assigned to CIs, and populate the CMDB with this data. Service Mapping uses the tag-related data from the CMDB to map services.

</td><td>

You can effectively use tags to map multiple application services.

 Starting with Service Mapping Plus version 1.16.3, take advantage of the Tag-based Service Mapping workspace to efficiently map you application services. For more information, see [Tag-based mapping in the Service Mapping Workspace](../reference/tag-based-mapping-dashboard.md) and [Tag-based discovery for the Service Mapping Workspace](tag-discovery-service-mapping-workspace.md).

</td><td>

Service instances mapped using tags might not include relevant CIs if those CIs do not have the correct tags.

</td></tr><tr><td>

[Traffic-based discovery](traffic-based-discovery.md)

</td><td>

Service Mapping can discover and map configuration items \(CIs\) following their traffic-based connections. This method is referred to as traffic-based mapping and complements pattern-based mapping.

 Depending on your configuration, the behavior of traffic-based discovery varies.

</td><td>

Using traffic-based discovery is like casting a finer net, allowing Service Mapping to find even those CIs that it failed to discover using patterns.

</td><td>

While using traffic-based discovery creates a more inclusive map, it may also result in mapping many redundant CIs that do not influence the application service operation. It may clutter an application service with irrelevant CIs. Use traffic-based discovery at the initial stages of discovering an application service and disable it once you completed discovery and fine-tuned the application service.

</td></tr></tbody>
</table>