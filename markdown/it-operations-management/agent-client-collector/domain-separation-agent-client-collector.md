---
title: Domain separation and Agent Client Collector
description: If any conkeyrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file.In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conkeyref at the end that describes domain separation.Domain separation is supported for Agent Client Collector \(ACC\). Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Domain separation and Agent Client Collector

Domain separation is supported for Agent Client Collector \(ACC\). Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## How domain separation works in Agent Client Collector

Domain separation in ACC allows the isolation of data collected by the Agent Client Collector to a particular domain. As a result, only users within that domain can access and view this data. Similarly, agents and their associated configurations are tied to specific domains, ensuring that operations within one domain do not affect or leak into others. This creates a more organized and secure environment for managing multiple groups, business units, or regions.

-   Data Security and Privacy: Restricting data access based on domains reduces the risk of unauthorized access and cross-domain data leakage, ensuring that sensitive information stays within its designated domain.
-   Access Control: By isolating domains, organizations can enforce strict access controls, allowing only designated users or teams to view or interact with the data relevant to their domain.

## Use cases for domain separation in Agent Client Collector

-   Multi-department collaboration with data isolation: IT and Finance departments can independently monitor their respective systems without data overlap. For example, if there’s an issue with a server in the payment processing system, Finance can run specific checks in their domain without interference from IT.
-   Regulatory compliance: Domain separation helps comply with regulations like GDPR or SOX by ensuring that only authorized personnel can access sensitive data. For instance, the Compliance department can monitor regulatory checks while being restricted from accessing IT infrastructure data.
-   Incident management and troubleshooting: IT can troubleshoot network issues, while Finance monitors transaction systems. Domain separation allows both departments to work independently, ensuring faster resolution and preventing data exposure.

**Related topics**  


[bundle-psec.domain-sep-landing-page]

