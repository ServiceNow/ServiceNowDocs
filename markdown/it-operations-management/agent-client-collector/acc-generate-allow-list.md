---
title: Generate an Agent Client Collector allow list
description: Specify the checks to be included in the list of checks that are enabled to run on the agent.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Enabling Agent Client Collector data collection, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Generate an Agent Client Collector allow list

Specify the checks to be included in the list of checks that are enabled to run on the agent.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

The default allow list includes all validated checks, and is included in the base system policies. If the allow list cannot be read correctly, no checks run on the agent.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Check Definitions**.

    The **Check Definitions** page appears.

2.  In the **Related Links** section at the bottom of the page, click **Generate allow list**.

    **Note:** Alternatively, you can click a check definition or check instance record and click **Generate allow list** to generate a complete allow list.

    The **Agent Client Collector Command Allow-list Generator** page appears, with the list of checks scanned from the **Command** field of the check instance records.

    The values appear with the following attributes:

<table id="table_kzq_xh2_ylb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

exec

</td><td>

The executing command.

</td></tr><tr><td>

args

</td><td>

Possible argument strings.

</td></tr><tr><td>

skip\_arguments

</td><td>

Boolean. Determines whether to verify that the argument was added to the allow list.-   **true**: Skips argument validation and checks only for illegal characters, specifically \|;\\&lt;&gt;&amp;'$\(\)
-   **false**: Executes argument validation to ensure that the argument is included in the allow list. If it is not, the command cannot execute.


</td></tr></tbody>
</table>3.  Copy the entries you want to include in the allow list and add them to the agent's `check-allow-list.json` file, either manually or using an automation tool.

    The location of this file is indicated in the **allow-list** parameter of the agent's `acc.yml` file.


**Parent Topic:**[Enabling Agent Client Collector data collection](../concept/data-collection-enabling.md)

