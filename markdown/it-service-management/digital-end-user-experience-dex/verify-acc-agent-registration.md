---
title: Verify that an Agent Client Collector agent is registered
description: Confirm that an Agent Client Collector \(ACC\) agent registered with your ServiceNow instance and is collecting host data. This allows you to validate the installation on a single device before deploying to your entire environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/verify-acc-agent-registration.html
release: brazil
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [verify acc agent registration, agent registered, host data collection status, check acc agent status, agents list, verify agent deployment, acc agent verification, digital end-user experience]
breadcrumb: [Installing DEX on your local machine, Configure, Digital End-User Experience, IT Service Management]
---

# Verify that an Agent Client Collector agent is registered

Confirm that an Agent Client Collector \(ACC\) agent registered with your ServiceNow instance and is collecting host data. This allows you to validate the installation on a single device before deploying to your entire environment.

## Before you begin

Install the Agent Client Collector agent on at least one device. For details, see [Install ACC for DEX on macOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/install-acc-for-dex-macos.md) or [Install ACC for DEX on Windows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/install-acc-for-dex-windows.md).

Role required: agent\_client\_collector\_admin

## About this task

Use this procedure to confirm that the agent is properly installed and communicating with your instance. Verify agent registration after installing the agent on a single device and after bulk deployments to track which devices have running agents.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agents**.

2.  Locate the device where you installed the agent.

    Search by device name or filter the list to find your device.

3.  Verify the agent status.

    Confirm that the agent is registered and that the host data collection status shows **Collected** or **Collecting**.

    An agent that is registered and collecting is ready to report DEX metrics.


If the agent doesn't appear in the agents list within 5 minutes, or if the host data collection status doesn't show **Collected** or **Collecting**, test the agent's connectivity to your instance. To troubleshoot connectivity issues, see [Test Agent Client Collector connectivity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/test-acc-connectivity.md).

**Related topics**  


[Test Agent Client Collector connectivity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/test-acc-connectivity.md)

[Deregister an Agent Client Collector agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/deregister-acc-agent.md)

