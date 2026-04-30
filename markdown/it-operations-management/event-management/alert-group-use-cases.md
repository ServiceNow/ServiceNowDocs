---
title: Alert grouping and use cases
description: Alert grouping methods range from user-defined approaches, like Manual and Rule-based to advanced, fine-tunable algorithms, including Automatic, Mixed, Text-based, Log Analytics, and Network Traffic-based grouping.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Alert grouping and use cases

Alert grouping methods range from user-defined approaches, like Manual and Rule-based to advanced, fine-tunable algorithms, including Automatic, Mixed, Text-based, Log Analytics, and Network Traffic-based grouping.

<table id="table_dwb_r55_hcc"><thead><tr><th>

Type

</th><th>

Description

</th><th>

Use case

</th></tr></thead><tbody><tr><td>

Log Analytics Grouping

</td><td>

Alerts are grouped based on the analysis of log data. This involves correlating log entries to identify related alerts and issues. By leveraging log patterns and sequences, this method can detect complex, multi-step problems across the IT environment.

</td><td>

An online gaming company enhances server stability by implementing proactive log analytics. They monitor logs from game servers in real-time and use analysis tools to detect patterns of errors that occur before crashes.

 For instance, the analysis reveals that certain error patterns appear about 30 minutes prior to server crashes. By setting up automated alerts for these patterns, the company can initiate remediation actions, such as restarting services or reallocating resources, before a crash occurs. This proactive approach prevents disruptions, minimizes downtime, and improves the gaming experience by addressing issues before they impact players.

</td></tr><tr><td>

Rule-based Grouping

</td><td>

Alerts are grouped according to predefined rules and criteria set by users. These rules might include specific conditions, such as thresholds or event types. This method is effective for consistent and repeatable patterns but requires maintenance of the rules.

</td><td>

In a data center managing an e-commerce website, rule-based alert grouping helps handle high traffic during events like flash sales. Alerts about server issues, such as high CPU usage, are designated as parent alerts. These parent alerts are linked to child alerts that report related problems, like slow database queries.

 The rules ensure that server-related alerts are grouped with their symptoms, allowing the IT team to quickly identify and address server overload issues. This approach improves issue resolution efficiency and minimizes downtime.

</td></tr><tr><td>

Automated Grouping

</td><td>

Advanced algorithms automatically identify and group related alerts based on patterns and similarities in the alert data. This method leverages machine learning and AI to adapt to new and unknown issues, providing proactive alert management.

 Event Management groups alerts that are similar, but not necessarily identical, based on the proximity in time of the last event generation. Alerts with the same CI and the same pattern identifier are grouped together.

 Automatic alert grouping consists of the following components.

-   Alert Aggregation Learner \(**Service Analytics Alert Aggregation Learner - Daily**\): This offline job runs daily to process past alerts and perform statistical analysis to build alert patterns. For details, see [Configure pattern based alert grouping](../task/configure-alert-aggregation.md).
-   Real-time Alert Aggregation job \(**Service Analytics group alerts using RCA/Alert Aggregation**\): This job runs every minute to generate alert aggregation groups based on alert patterns, CMDB relationships, text similarity, user-defined alert clustering tags, and network traffic connection between processes.

</td><td>

A large financial institution uses machine learning to manage alerts from numerous servers and applications. The system analyzes historical alert data to recognize patterns, such as database server failures frequently being accompanied by client connection errors. It then automatically groups related alerts together. For instance, when a new database server failure alert is detected, it is grouped with previous connection error alerts.

 This automated grouping helps the IT and security teams quickly identify and address issues, improving response times and reducing downtime.

</td></tr><tr><td>

Mixed Grouping

</td><td>

Mixed Grouping method combines alerts using multiple grouping strategies, such as CMDB-based grouping and tag-based grouping, into a single, cohesive group. It leverages the strengths of each strategy to reduce alert noise, improve alert correlation, and highlight the true root cause of incidents.-   CMDB-based Grouping: Alerts are grouped based on Configuration Item \(CI\) relationships and dependencies from the Configuration Management Database \(CMDB\). This approach ensures that alerts related to specific infrastructure components or services are grouped together, providing context-aware alert management.
-   Tag Cluster Grouping: Alerts are categorized and grouped using tags or labels that represent common attributes, such as application, server type, or geographic location. This method allows for flexible and dynamic grouping based on evolving tagging strategies.

</td><td>

Use case for CMDB-based grouping:

 A telecommunications company uses CMDB data to manage alerts related to their network infrastructure. Alerts related to a specific network router and its connected devices are grouped together based on their CMDB relationships, enabling the network team to see all related issues and address the root cause efficiently.

 Use case for tag cluster grouping:

 An organization without a CMDB manages a Linux server running various services. The IT team uses a **Node** field in each alert to identify the server, and they group all events related to services on the same server based on this node value. For example, they cluster alerts like Service A down and Service B high CPU usage together if they share the same node value.

 This approach helps the IT team address server-related issues more efficiently. By clustering alerts for the same node, application, or IP address, the team streamlines their response efforts and resolves issues more effectively, even without a CMDB.

</td></tr><tr><td>

Network-traffic based Grouping

</td><td>

Network-traffic-based alert grouping analyzes network connections between processes across hosts to identify related alerts. This method leverages service candidates detected through ML Service Mapping, ensuring that alerts related to network traffic issues are grouped together for better context and faster alert resolution.

</td><td>

A cloud-based e-commerce platform experiences transaction slowdowns, causing delays in payment processing. Traditional alerting generates separate alerts for API timeouts, database lags, and network issues, making it difficult to pinpoint the root cause.

 With Network-Traffic Based Grouping, alerts are automatically grouped based on process-to-process connections identified through ML Service Mapping. The system detects that payment gateway services, fraud detection, and order processing are part of the same service candidate. This reveals that an overloaded fraud detection process is causing transaction bottlenecks. By scaling up the service, the team quickly resolves the issue, minimizing downtime and improving customer experience.

</td></tr><tr><td>

Text-based Grouping

</td><td>

Alerts are grouped by analyzing the text content of alerts to identify similarities and related issues. Natural language processing \(NLP\) techniques are used to find commonalities in alert description, metric name, and ci class, making this method effective for unstructured data.

</td><td>

In an organization that uses Zoom rooms for virtual meetings, the IT team receives numerous alerts when the Zoom room server experiences an outage. Each alert might indicate a different Zoom room being down, such as Zoom room no 10 is down, Zoom room no 11 is down, and so on, with the only difference being the room number.

 For organizations with a CMDB, these alerts can be grouped using CMDB relations, as the system can correlate the alerts based on the server's impact on all associated Zoom rooms. However, for organizations without a CMDB, text-based grouping can be used. The system applies natural language processing to group alerts with similar descriptions, helping the IT team quickly identify that multiple Zoom rooms are affected by the same underlying server issue. This approach allows the IT team to efficiently address the root cause of the problem, reducing downtime and improving response times.

</td></tr><tr><td>

Manual Grouping

</td><td>

Users manually select and group related alerts based on their expertise and understanding of the system. This approach allows for precise control but can be time-consuming and may miss automated correlations.

</td><td>

A system administrator receives multiple alerts about different services failing on a single server. The admin manually groups these alerts, recognizing that they are all related to a single hardware failure on that server, and prioritizes fixing the hardware issue to restore all services.

</td></tr></tbody>
</table>Manual and rule-based alert grouping differs from algorithm-based grouping mainly in how the parent alert is chosen. In manual, rule-based, or log analytics grouping, one of the real alerts is designated as the parent alert. In Automatic, CMDB, Text-based, Tag Cluster modes, and Network Traffic, a virtual alert, representing the oldest and most severe alert in the group, is created as the parent alert.

**Note:** In domain-separated environments, alert groups are created only for alerts within the same domain.

For information on scheduled jobs and parameters, refer to [Scheduled jobs and parameters for alert grouping](alert-grp-jobs-parameters.md). For detailed information on different grouping types, see [Alert grouping types and creation methods](Alert-Groups.md).

