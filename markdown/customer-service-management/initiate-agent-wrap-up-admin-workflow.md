---
title: Configure agent-initiated wrap-up
description: Enable the agent-initiated wrap-up option and define the wrap-up codes that agents can select during an active call.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/initiate-agent-wrap-up-admin-workflow.html
release: australia
topic_type: task
last_updated: "2026-06-18"
reading_time_minutes: 1
keywords: [agent-initiated wrap-up, wrap-up, call wrap-up, wrap-up configuration, wrap-up codes, CCaaS]
breadcrumb: [Call Wrap-Up, ICC for voice calls, Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# Configure agent-initiated wrap-up

Enable the agent-initiated wrap-up option and define the wrap-up codes that agents can select during an active call.

## Before you begin

The ICC for voice is integrated with a supported CCaaS platform.

Role required: CCaaS administrator

## About this task

The following is a high-level overview of how a CCaaS administrator configures agent-initiated wrap-up in the ServiceNow instance.

## Procedure

1.  Navigate to **Integration** &gt; **Wrap-Up Configuration** in the ServiceNow instance.

2.  Create or open an existing wrap-up configuration for the relevant external channel.

3.  Enable the agent-initiated wrap-up option and define the wrap-up codes that agents can select during a call.


## Result

Agents can select **Open Wrap-Up** during an active call and submit the configured wrap-up codes.

**Note:** Agent-initiated wrap-up applies only to supported CCaaS integrations. Call flows on unsupported platforms do not surface the **Open Wrap-Up** control, even if the configuration is enabled.

