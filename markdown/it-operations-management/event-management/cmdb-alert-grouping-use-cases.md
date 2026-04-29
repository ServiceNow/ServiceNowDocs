---
title: Use cases for CMDB based alert grouping
description: Use cases for CMDB grouping enhance alert management by correlating alerts based on Configuration Item relationships, improving visibility, and facilitating more efficient troubleshooting.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CMDB based alert grouping, Mixed alert grouping, Alert grouping types and creation methods, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Use cases for CMDB based alert grouping

Use cases for CMDB grouping enhance alert management by correlating alerts based on Configuration Item relationships, improving visibility, and facilitating more efficient troubleshooting.

## Common CMDB grouping use cases

In the context of CMDB grouping, organizations face several challenges when managing alerts related to Configuration Items \(CIs\).

<table id="table_c43_cky_gdc"><thead><tr><th>

Use Case

</th><th>

Challenges

</th><th>

Solutions

</th></tr></thead><tbody><tr><td>

Shared Configuration Item \(CI\)Scenario: An organization monitors a database server experiencing multiple issues, resulting in numerous alerts related to different applications using that database.

</td><td>

-   Delayed response: Teams may respond to alerts in isolation, potentially overlooking related alerts, leading to delayed resolutions.
-   Inefficient resource allocation: Time and resources may be wasted on investigating separate alerts that are actually related.
-   Lack of context: Alerts related to the same CI can be scattered across different alert groups, making it difficult to see the full picture.

</td><td>

-   Aggregate alerts related to the same CI into a single group for a unified view.
-   Facilitate faster alert resolution by addressing all related alerts together.

</td></tr><tr><td>

Hosting/Containment RelationsScenario: A physical server hosts several virtual machines \(VMs\), and an alert is generated for a hardware failure on the server. Multiple alerts also arise for the VMs due to their reliance on the server.

</td><td>

-   Visibility into dependencies: Teams may lack visibility into how CIs are interconnected, leading to inefficient troubleshooting processes.
-   Complex alert resolution: Understanding which CIs are affected and how they relate can be complicated, resulting in longer resolution times.
-   Resource drain: Mismanagement of alerts can lead to duplicated efforts across teams, wasting time and resources.

</td><td>

-   Group alerts using CMDB hosting/containment rules to aggregate alerts related to the physical server and its hosted VMs into a single alert group.
-   Provide a comprehensive view of all alerts tied to the physical server's failure.
-   Focus remediation efforts on the physical server while monitoring the VMs to ensure all aspects are addressed efficiently.

</td></tr><tr><td>

Applicative RelationsScenario: An enterprise application relies on multiple micro-services, and an issue arises with one of these services, generating alerts across several components, complicating diagnosis.

</td><td>

-   Understanding application dependencies: Teams may find it challenging to trace how application components interact, making it difficult to pinpoint issues in complex systems.
-   Slow incident resolution: Without a clear understanding of applicative flow, alert resolution can be slow and labor-intensive.
-   Inconsistent monitoring: Alerts related to applications may not be consistently monitored or prioritized, leading to potential oversights.

</td><td>

-   Implement grouping based on applicative flow relations to aggregate alerts related to the affected microservice and its dependent components.
-   Utilize dependency maps to visualize how different services interact.
-   Streamline the resolution process by addressing grouped alerts related to the application, improving response times.

</td></tr></tbody>
</table>