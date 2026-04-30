---
title: Configuring CIs in a manual service as a manual cluster
description: Configure or modify a CI as a specific CI or a generic CI class in a manual service \(that was not discovered automatically\) as a manually defined cluster. A manual cluster delivers redundancy capabilities in the cluster and provides continued operations or services of the entire cluster in case of failure of one or more CIs in that cluster.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Application services in Event Management, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configuring CIs in a manual service as a manual cluster

Configure or modify a CI as a specific CI or a generic CI class in a manual service \(that was not discovered automatically\) as a manually defined cluster. A manual cluster delivers redundancy capabilities in the cluster and provides continued operations or services of the entire cluster in case of failure of one or more CIs in that cluster.

Manual cluster allows you to group CIs under a logical cluster in a service. In the impact tree you can set the relative impact of a cluster member on the cluster.

**Note:** Creation of nested manual clusters \(cluster inside cluster\) is currently not supported.

Once the CI is defined as a manual cluster its impact calculation shows the magnitude of an outage on its children CIs. Impact calculation uses factors such as impact rules and CI relationships to calculate the severity of a generated alert. Impact rules, which are used for impact calculation, estimate the magnitude or severity of an outage based on affected CIs and determines how the impact applies to parent or child entities that are part of an application service.

The magnitude of an outage can be 100% down, 60% affected, 40% impaired, or 20% impaired.

Redundancy is defined in impact rules. For example, you can define that the parent CI is critical if at least two child CIs are critical. The impact from child to parent CIs is not always 100%. If the CIs of all three children are affected, the impact is 100% down.

In a service map, you can configure or modify a specific CI or a generic CI class in a manual service as a manually defined cluster. When configuring as a generic CI class, all the CIs of the selected class in that service are configured the same.

**Note:** Visual representation of a manual cluster may differ from the visual representation of a cluster that is discovered automatically.

-   **[Configure a manual cluster](../task/configure-manual-cluster.md)**  
Provide redundancy capabilities of an entire cluster in case of failure of one or more CIs in that cluster. By viewing the relative impact of a cluster member on the cluster information, you can better understand the source of alerts and take remediation steps.
-   **[Modify a manual cluster](../task/modify-a-manual-cluster.md)**  
Modify an existing manual cluster by changing the service, the specific CI, the generic CI class, or the description in case of an incorrect initial configuration, changes in the network, or other issues.

**Parent Topic:**[Application services in Event Management](application-service-event-management.md)

**Related topics**  


[Alert impact calculation](c_EMImpactCalculation.md)

