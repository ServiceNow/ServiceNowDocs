---
title: Agent-based data flow
description: The Agent Client Collector gathers information on the health of the CI that the Agent is installed on, and the applications that run on the hosts. The Agent runs several checks and pushes the checks' results to the MID Server, where they are converted into events or metrics.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exploring ACC Framework, Agent Client Collector, IT Operations Management]
---

# Agent-based data flow

The Agent Client Collector gathers information on the health of the CI that the Agent is installed on, and the applications that run on the hosts. The Agent runs several checks and pushes the checks' results to the MID Server, where they are converted into events or metrics.

Events are stored in the instance's Events database, while metrics are stored in the Metrics database.

The following image displays the data flow from the Agent Client Collector to the instance.

![Agent client collector data flow](../image/acc-dataflow.png)

The numbered entries in the flow indicate the following:

1.  Specified checks run on the agent. Data, including metrics, is pushed to the MID Server.
2.  The MID Server analyzes the data and classifies the results as events or metrics. MID Server uses REST API to send the results to the instance.
3.  The instance receives the data and stores it in the relevant database.

**Parent Topic:**[Exploring Agent Client Collector Framework](exploring-agent-client-collector-framework.md)

