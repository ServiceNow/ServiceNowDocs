---
title: Exploring Event Management
description: Explore Event Management to understand its overview, process flow, user roles, and benefits for comprehensive IT issue monitoring and resolution.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Event Management, ITOM Health, IT Operations Management]
---

# Exploring Event Management

Explore Event Management to understand its overview, process flow, user roles, and benefits for comprehensive IT issue monitoring and resolution.

Event Management provides comprehensive monitoring, analysis, and remediation of IT issues by effectively managing various components within an IT environment. These components include discovered services, application services, dynamic CI groups, and alert groups.

-   Discovered Services: Defined by interrelated Configuration Items \(CIs\) from the CMDB, a discovered service is identified through Service Mapping. It includes a service map with mapping relationships, an impact tree showing outage severity, active and related alerts, and CI properties. This service information is displayed on dashboards, the Alerts list, and the Events list.
-   Application Services: Created by selecting specific CIs, application services allow for targeted monitoring and management. For more details, refer to the Application Services documentation.
-   Dynamic CI Groups: These are collections of CIs grouped based on shared criteria, such as location. Dynamic CI groups help populate application services, simplifying management.
-   Alert Groups: Alert groups organize sets of alerts to streamline maintenance and management, making it easier to respond to IT issues efficiently.

## Process flow

Event Management receives external events and generates alerts based on predefined rules. The MID Server polls external event tracking tools and sends data to Event Management for storage and processing. Events are stored in the Event \[em\_event\] table, and alerts are created by matching event rules. Alerts are then transformed and enriched with additional content, accumulated if thresholds are met, and mapped to specific fields. The system searches for matching message keys to update existing alerts or create new ones, associating related events under a single alert. Alerts are bound to specific Configuration Items \(CIs\) for root cause analysis. For more information, see [Event Management process flow](em-process-flow.md).

## Users

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Admin\[evt\_mgmt\_admin\]

</td><td>

Configures and sets up Event Management properties and rules.**Note:** Exercise caution with the evt\_mgmt\_admin role, as it can be elevated to the admin role. A user with the evt\_mgmt\_admin role has the ability to add and modify scripts that run on a global scope. Ensure proper access control. With this role, the user can create and/or update the following scripts:

-   Alert correlation rules
-   Alert management rules
-   Maintenance rules
-   Advanced scripts
-   Event field mapping
-   Pre- and post-binding scripts

</td></tr><tr><td>

Operator\[evt\_mgmt\_operator\]

</td><td>

Manages alerts, including closing and acknowledging them.

</td></tr><tr><td>

User\[evt\_mgmt\_user\]

</td><td>

Manages the lifecycle of alerts, including performing basic operations such as viewing and acknowledging them.

</td></tr></tbody>
</table>## Benefits

-   Rapid Issue Detection: Quickly identifies and highlights potential IT issues.
-   Efficient Alert Handling: Aggregates and correlates alerts for streamlined management.
-   Automated Actions: Initiates automatic remediation processes to speed up issue resolution.
-   Comprehensive Monitoring: Integrates with multiple tools for a complete system overview.
-   Root Cause Analysis: Offers tools to identify underlying causes of issues.
-   Customizable Rules: Tailors event and alert management rules to specific needs.
-   Reduced Downtime: Minimizes system downtime with prompt problem resolution.
-   Enhanced Visibility: Real-time dashboards offer insights into system health.
-   Cost Efficiency: Lowers operational costs by preventing prolonged issues.

