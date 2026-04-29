---
title: Agent Client Collector API
description: Use the Agent Client Collector \(ACC\) API to create a flow that executes an osquery command on agents and processes the results. By leveraging the ACC API, you can automate the querying of agent data and streamline the processing of results, making it easier to monitor and manage system performance.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACC deployment - shared between servers and endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector API

Use the Agent Client Collector \(ACC\) API to create a flow that executes an `osquery` command on agents and processes the results. By leveraging the ACC API, you can automate the querying of agent data and streamline the processing of results, making it easier to monitor and manage system performance.

The system supports osquery 5.7.0, providing compatibility with a range of queries for efficient data collection.

The ACC API enables seamless integration and automation for executing queries and managing agents. Here's how it works:

1.  Execute osquery commands: You can use the ACC API to send osquery commands to agents. These commands collect a wide range of system and performance data from the target machines.
2.  Process results: After the osquery command is executed on the agents, the ACC API processes the results and returns the necessary data. This data can be used for monitoring, troubleshooting, or reporting purposes.
3.  Support for osquery 5.7.0: The ACC API is compatible with osquery 5.7.0, which ensures it supports the latest features and improvements, enabling you to leverage advanced query capabilities for enhanced data collection.
4.  Enable API features: To use the ACC API, enable the agent and policy APIs. This allows you to configure and manage various aspects of your agents, including their communication, data collection, and query execution.

For details on agent APIs, see [Enable agent APIs](https://www.servicenow.com/docs/access?context=AccAgentsAPIAPIScoped&version=australia&pubname=australia-api-reference&ft:locale=en-US).

For details on enabling policy APIs, see [Enable policy APIs](https://www.servicenow.com/docs/access?context=agnt_clnt_cll-api&version=australia&pubname=australia-api-reference&ft:locale=en-US).

**Parent Topic:**[Deploying Agent Client Collector on both servers and endpoints](acc-shared-deployment.md)

