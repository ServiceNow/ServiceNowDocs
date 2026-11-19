---
title: Verify data collection in Agent Client Collector
description: Collect data by gathering essential information from an agent's host system before executing any checks or policies. This process ensures that the Agent Client Collector has accurate and up-to-date data on the infrastructure, processes, and applications running on the host.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-operations-management/agent-client-collector/acc-data-collection-concept.html
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Verify data collection in Agent Client Collector

Collect data by gathering essential information from an agent's host system before executing any checks or policies. This process ensures that the Agent Client Collector has accurate and up-to-date data on the infrastructure, processes, and applications running on the host.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

Collected data is stored as Configuration Item \(CI\) data, which serves as a foundation for monitoring, alerts, and Metric Intelligence in the ServiceNow® instance.

Before checks and polices can be executed, Agent Client Collector collects data on:

-   Host system details \(such as hardware and the system's OS version\)
-   Installed applications and services
-   Running processes
-   Resource usage metrics \(such as CPU, memory, and disk utilization\)

Collected data is stored in the ServiceNow instance in either the CMDB \(Configuration Management Database\) or events table.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agents**.

2.  On the Agent Client Collectors page, locate the **Host Data Collection** column for an agent.

    A green Collected icon \[Omitted image "collected-icon.png"\] Alt text: Collected icon indicates successful data collection for the specific agent.


**Parent Topic:**[Exploring Agent Client Collector Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/agent-client-collector/exploring-agent-client-collector-framework.md)

