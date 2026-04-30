---
title: Agent Client Collector log policies
description: Agent Client Collector data inputs stream log messages to your ServiceNow instance using the ServiceNow Agent Client Collector. The Agent Client Collector Log Analytics \(ACC-L\) application provides predefined log policies for collecting log data from the CIs monitored by the ACC.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Agent Client Collector Log Analytics, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector log policies

Agent Client Collector data inputs stream log messages to your ServiceNow instance using the ServiceNow Agent Client Collector. The Agent Client Collector Log Analytics \(ACC-L\) application provides predefined log policies for collecting log data from the CIs monitored by the ACC.

You can work with Agent Client Collector log policies in the following ways:

-   Use the system's predefined log policies.

    The default ACC-L log policies consist of the monitored CIs and the check that runs on those CIs. For a complete list of the predefined log policies and monitored CI types, see [Agent Client Collector Log Analytics default policies and checks](../../agent-client-collector/reference/acc-log-analytics-policies-checks.md).

-   Edit a predefined log policy.

    For example, you can modify a default policy if your organization always uses a specific non-default log path. For more information, see [Edit a log policy](../../agent-client-collector/task/accl-edit-log-policy.md).

-   Customize a published log policy by creating a child policy from it.

    You can use an existing log policy \(the parent policy\) as a template to create a new log policy \(the child policy\). You then customize the parameters that the child policy inherits from the parent to focus on a subgroup of its CIs or services. For example, create a child policy if your organization saves a subset of IIS Server logs to a different location. For more information, see [Create a child log policy](../../agent-client-collector/task/accl-create-child-log-policy.md).

    **Note:** The child policy is inherently more specific than its parent policy. When Agent Client Collector matches a condition defined in the child policy, it will not try to match the parent policy.

-   Define a new log policy when no policy exists for the CI that you want Agent Client Collector to monitor.

    For more information, see [Create an Agent Client Collector log policy](../task/hla-acc-log-policies.md). For a general explanation of Agent Client Collector policies, see [Checks and policies](../../agent-client-collector/concept/checks-policies.md).


