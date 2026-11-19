---
title: Verify MID Server ineligibility
description: Verify that the MID Servers you configured to be ineligible for automatic MID Server selection can't be selected automatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/verify-mid-server-ineligibility.html
release: brazil
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-11-05"
reading_time_minutes: 1
breadcrumb: [Configure automatic MID selection based on ACC capabilities, Automatic MID Server selection, Configuring ACC with a MID Server, ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Verify MID Server ineligibility

Verify that the MID Servers you configured to be ineligible for automatic MID Server selection can't be selected automatically.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Deployment** &gt; **MID Servers**.

2.  Assign the **AgentClientCollector** capability to MID Server A and MID Server C, but not to MID Server B.

3.  Assign a different capability to MID Server B.

4.  Install Agent Client Collector Framework and specify MID Server A as the MID Server during installation.

    After installation, the agent has **Status=Up** and its MID Server is MID Server A.

5.  Execute the MID Server Selection scheduled job to determine which MID Servers are eligible for automatic MID Server selection.

    MID Server B is ineligible for automatic selection, because it doesn’t have the same ACC capability as MID Server A. MID Server C is eligible, because it has the same ACC capability as MID Server A.


**Parent Topic:**[Configure the automatic MID Server selection based on the Agent Client Collector capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/configure-auto-mid-eligibility-by-capability.md)

