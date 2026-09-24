---
title: Deregister an Agent Client Collector agent
description: Remove the registration record for an Agent Client Collector \(ACC\) agent from your ServiceNow instance after uninstalling the agent from a device.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/deregister-acc-agent.html
release: brazil
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [deregister acc agent, remove agent registration, delete agent record, agent registration list, deregister agent client collector]
breadcrumb: [Installing DEX on your local machine, Configure, Digital End-User Experience, IT Service Management]
---

# Deregister an Agent Client Collector agent

Remove the registration record for an Agent Client Collector \(ACC\) agent from your ServiceNow instance after uninstalling the agent from a device.

## Before you begin

Uninstall the agent from the device. For details, see [Uninstall the Agent Client Collector agent from a device](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/uninstall-acc-agent.md).

Role required: agent\_client\_collector\_admin

## About this task

Deregistering an agent deletes its registration record. Deregister an agent only after you uninstall it from the device. If the agent is still installed and running, it can re-register with your instance.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agents**.

2.  Note the agent IDs that you want to deregister.

3.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agent Registration**.

4.  Select the agents that you want to deregister.

5.  Delete the selected records.

    The agents no longer appear as registered on your instance.


**Related topics**  


[Uninstall the Agent Client Collector agent from a device](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/uninstall-acc-agent.md)

[Verify that an Agent Client Collector agent is registered](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/verify-acc-agent-registration.md)

