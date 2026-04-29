---
title: Network ping metrics
description: The following table lists the metrics that are gathered as output from Network ping checks. Entries indicated as Featured metrics are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Monitoring default checks and policies, ACC-M reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# Network ping metrics

The following table lists the metrics that are gathered as output from Network ping checks. Entries indicated as **Featured metrics** are high-visibility metrics that are displayed in the Operator Workspace Metric tab after an alert is generated. These metrics provide the operator with additional information to help them further explore the specified issue.

|Metric type|Units|Metric type description|
|-----------|-----|-----------------------|
|ping.packets\_transmitted|count|Number of data packets sent to the target host during the ping test.|
|ping.packets\_received|count|Number of data packets successfully received by the target host.|
|ping.packet\_loss|percentage|Percentage of data packets that failed to reach the target host.|
|ping.time|ms|Amount of time for the data packets to travel to the destination and back.|
|ping.min|ms|Shortest amount of time for a series of ping requests on the data packets.|
|ping.avg|ms|Average amount of time for a series of ping requests on the data packets.|
|ping.max|ms|Longest amount of time for a series of ping requests on the data packets.|
|ping.mdev|ms|Mean deviation \(measure of the variability or dispersion\) of the round-trip time \(RTT\) of the packets sent during the ping test.|

**Parent Topic:**[Agent Client Collector Monitoring default checks and policies](agent-policies-checks.md)

