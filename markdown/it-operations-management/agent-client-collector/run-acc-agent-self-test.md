---
title: Run Agent Client Collector self-diagnostic tests
description: Run built-in self-diagnostic tests to validate agents' configuration, connectivity, and system requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/run-acc-agent-self-test.html
release: brazil
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
keywords: [agent, diagnostic, self-test, validation]
breadcrumb: [ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Run Agent Client Collector self-diagnostic tests

Run built-in self-diagnostic tests to validate agents' configuration, connectivity, and system requirements.

## Before you begin

Ensure that you have installed the following:

-   Agent Client Collector agent: Version 6.0.1 or higher
-   Agent Client Collector Framework Store Application Plugin: Version 6.0.1 or higher

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agents**.

2.  Select an agent record.

3.  Select **Run Self Test** from the **Related Links** section.

4.  Verify that tests execute automatically.

    Test results appear in the Agent Self Test Run \(`sn_agent_self_test_run`\) table.

    For details on the diagnostic self-tests that the agent runs, see [Agent Client Collector diagnostic self tests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/acc-agent-self-tests.md).


**Parent Topic:**[Deploying Agent Client Collector on servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/acc-server-deployment.md)

