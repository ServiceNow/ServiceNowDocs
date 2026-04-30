---
title: Generate a Pattern allow list
description: Generate an allow list for a specific scope or selection of patterns.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-12-04"
reading_time_minutes: 1
breadcrumb: [ACC deployment - endpoints, Agent Client Collector, IT Operations Management]
---

# Generate a Pattern allow list

Generate an allow list for a specific scope or selection of patterns.

## Before you begin

Ensure that the following plugins are installed on your instance:

-   Discovery \(com.snc.discovery\)
-   Pattern Designer Enhancements \(com.sn\_itom\_pde\)

Role required: discovery\_admin or agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Pattern Designer** &gt; **Patterns allowlist for ACC**.

    The **Pattern Allowlist Generator** page appears.

2.  Select the type of pattern selection in the **Pattern Selection** section.

    -   **All patterns**: The allow list generates for all patterns on the agent.
    -   **Specific patterns**: The allow list generates on the agent only for the patterns you select.

        After selecting this option, choose the patterns from which you want the allow list to be generated.

3.  Select an application scope from which to choose patterns to be included in the allow list.

    -   All
    -   Discovery and Service Mapping Patterns
    -   Global
    **Note:** Choosing an application scope is possible only when selecting **All patterns** in the **Pattern Selection** section.

4.  Select **Generate Allowlist**.

5.  Select **Copy** to copy the generated allow list.

6.  Append the copied allow list into the existing `check-allow-list.json` allow list on the agent.

    The patterns specified in the allow list are permitted to run on the agent.

    **Note:** The pattern allow list generator does not add an entry for commands nested under EVAL\(\) in the pattern steps.


