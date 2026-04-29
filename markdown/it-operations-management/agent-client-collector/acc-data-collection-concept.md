---
title: Verify data collection in Agent Client Collector
description: Collect data by gathering essential information from an agent's host system before executing any checks or policies. This process ensures that the Agent Client Collector has accurate and up-to-date data on the infrastructure, processes, and applications running on the host.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Collect data from your system devices, ACC deployment - shared between servers and endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
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

    A green Collected icon ![Collected icon](../image/collected-icon.png) indicates successful data collection for the specific agent.


