---
title: Discovery for containerized resources
description: Container discovery enables IT departments of companies to collect detailed information about their container management tools in the infrastructure. Discovery finds resources in major container management services providers.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Patterns, Kubernetes, ECS, Foundry, OpenShift, Docker]
breadcrumb: [Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery for containerized resources

Container discovery enables IT departments of companies to collect detailed information about their container management tools in the infrastructure. Discovery finds resources in major container management services providers.

-   **[Kubernetes discovery using patterns](../../service-mapping/concept/kubernetes-discovery.md)**  
The ServiceNow ITOM Visibility finds Kubernetes and OpenShift components using patterns and creates application services containing them. Discovery also finds Kubernetes events and frequently updates the CMDB to reflect the dynamic Kubernetes environment.
-   **[Container image scanning for software decomposition](../../service-mapping/concept/container-image-concept.md)**  
The ITOM Visibility apps, Discovery and Service Mapping Patterns and Kubernetes Visibility Agent integrate with Aqua Trivy to collect data on container images and OS packages. You can increase your control over container deployment by having visibility to the container components.
-   **[Kubernetes Visibility Agent](../../agent-client-collector/concept/acc-kubernetes-visibility-landing-page.md)**  
Kubernetes Visibility Agent detects changes on resources in a Kubernetes cluster. It performs continuous discovery, reports any changes back to your instance, and updates the Configuration Management Database \(CMDB\) with the latest data.

**Parent Topic:**[Discovery](../reference/r-discovery.md)

**Related topics**  


[Amazon ECS resource discovery with Patterns](../../service-mapping/reference/aws-ecs-fargate-discovery.md)

[Pivotal Cloud Foundry discovery](../../service-mapping/concept/pivotal-cloud-foundry.md)

[Docker virtualization](c-docker-virtualization.md)

