---
title: View agent errors
description: Agent Client Collector \(ACC\) errors are visible in logs related to the agent and the ServiceNow instance. This feature provides improved visibility of agent errors, enabling faster error resolution.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Collecting data from your system devices, ACC deployment - shared between servers and endpoints, Agent Client Collector, IT Operations Management]
---

# View agent errors

Agent Client Collector \(ACC\) errors are visible in logs related to the agent and the ServiceNow instance. This feature provides improved visibility of agent errors, enabling faster error resolution.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agent Issues**.

    The **ACC Error Messages** page appears and lists the agents containing errors.![ACC Error Messages page](../image/acc-error-messages.png)

    The following columns display the indicated information about the errors.

<table id="table_dlc_s4b_fdc"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CI ID

</td><td>

The name of the agent containing the error, or a configuration item \(CI\) with an issue.

</td></tr><tr><td>

Code

</td><td>

Error code assigned to the issue.

</td></tr><tr><td>

Message

</td><td>

A message describing the error.

</td></tr><tr><td>

Source application

</td><td>

The application triggering the error.

</td></tr><tr><td>

Error status

</td><td>

Indicates the state of the error: **Active** or **Resolved**.

</td></tr><tr><td>

Category

</td><td>

The error category which the error is classified under.

</td></tr><tr><td>

Key

</td><td>

Internal value used to identify the error.For data collection errors, specifies the **agent\_id** value.

</td></tr><tr><td>

Key extension

</td><td>

Internal value used to identify the error.For check execution errors, specifies the check name.

</td></tr><tr><td>

Command

</td><td>

The command executed when the error occurred \(if applicable\).

</td></tr><tr><td>

Stack trace

</td><td>

A reference to the **ecc\_queue** record that was processed and triggered the error \(if applicable\).

</td></tr></tbody>
</table>    **Note:**

    -   Not all columns are visible by default on the page.
    -   Select the info icon \(![Info icon](../../event-management/image/info.png)\) next to an error to view a pop-up window with full information about the error.

        ![ACC Error Message popup window](../image/acc-error-message-popup.png "ACC Error Message pop-up window")

        The info icon is visible when hovering under the search icon \(![Search icon](../../cloud-management-v2/image/search-icon-magnifyingGlass.png)\) next to the error entry.

2.  To view errors for a specific agent:

    1.  Select **All** &gt; **Agent Client Collector** &gt; **Agents**.

        The **Agent Client Collectors** table appears.

    2.  Select an agent.

    3.  Select the **Automation Error Messages** tab at the bottom of the page to view errors relating to the agent.


## Result

If an error causes an agent's registration to fail, the agent's **Status** column displays **Registration Failure** on the Agent Client Collectors page \(**All** &gt; **Agent Client Collector** &gt; **Agents**\).

