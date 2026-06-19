---
title: Generate a Pattern allowlist
description: Generate an allowlist for a selection of patterns, to configure the patterns permitted to run on an agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/generate-patterns-allow-list.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACC deployment - endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Generate a Pattern allowlist

Generate an allowlist for a selection of patterns, to configure the patterns permitted to run on an agent.

## Before you begin

Ensure that the following plugins are installed on your instance:

-   Discovery \(com.snc.discovery\)
-   Pattern Designer Enhancements \(com.sn\_itom\_pde\)

Role required: discovery\_admin or agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Pattern Designer** &gt; **Patterns allowlist for ACC**.

    The **Pattern Allowlist Generator** page appears.

2.  Select the type of pattern selection in the **Pattern Selection** section.

    -   **All patterns**: The allowlist generates for all patterns on the agent.
    -   **Specific patterns**: The allowlist generates on the agent only for the patterns you select.

        After selecting this option, choose the patterns from which you want the allowlist to be generated.

3.  Select **Generate Allowlist**.

4.  Select **Copy** to copy the generated allow list.

5.  Append the copied allowlist into the existing `check-allow-list.json` allow list on the agent.

    The patterns specified in the allowlist are permitted to run on the agent.

    **Note:** To generate allowlist for commands nested within EVAL\(\) in a pattern step, ensure the Pattern Designer Enhancements plugin is v3.9.1 or above.


-   **[Define temporary variables for a pattern allowlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/define-temp-variables.md)**  
Define temporary variables by assigning values such as executable paths, config file paths, and so forth. If a Linux command contains a string that isn’t defined, the command fails when run.

**Parent Topic:**[Deploying Agent Client Collector on endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-endpoint-deployment.md)

