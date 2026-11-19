---
title: Configure the automatic MID Server selection based on the Agent Client Collector capabilities
description: Configure the MID Servers that are ineligible for automatic MID Server selection with the agent. For example, you may want to block a MID Server from connecting to your agent due to firewall constraints.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/configure-auto-mid-eligibility-by-capability.html
release: brazil
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Automatic MID Server selection, Configuring ACC with a MID Server, ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Configure the automatic MID Server selection based on the Agent Client Collector capabilities

Configure the MID Servers that are ineligible for automatic MID Server selection with the agent. For example, you may want to block a MID Server from connecting to your agent due to firewall constraints.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

Agents with different levels of Agent Client Collector \(ACC\) capability can't be considered for automatic MID Server selection. To block a MID Server from automatic selection, assign it different ACC capabilities from all other MID Servers in your environment. Don't assign different capabilities from the primary MID Server.

## Procedure

1.  Configure the Agent Client Collector capabilities for MID Servers, as described in [Configure the Agent Client Collector capabilities for MID Servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/configure-acc-capability.md).

2.  Navigate to All &gt; Agent Client Collector &gt; MID Servers.

    1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **MID Servers**.

    2.  Select the MID Server that you want to be ineligible for automatic MID Server selection.

    3.  Select the additional actions icon \[Omitted image "additional-actions-icon.png"\] Alt text: Additional Actions icon. and select **View** &gt; **Default View**.

    4.  Select the **Capabilities** tab.

    5.  Ensure that the MID Server isn't assigned with the capabilities that have **Is ACC Capability=true** on the **Capabilities** tab.


## Result

You now have at least one MID Server ineligible for automatic MID Server selection.

-   **[Verify MID Server ineligibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/verify-mid-server-ineligibility.md)**  
Verify that the MID Servers you configured to be ineligible for automatic MID Server selection can't be selected automatically.

**Parent Topic:**[Automatic MID Server selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/acc-auto-mid-selection.md)

