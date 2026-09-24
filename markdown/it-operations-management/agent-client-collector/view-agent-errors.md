---
title: View agent errors
description: Agent Client Collector \(ACC\) errors are visible in logs related to the agent and the ServiceNow instance. This feature provides improved visibility of agent errors, enabling faster error resolution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/view-agent-errors.html
release: brazil
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Collect data from your system devices, ACC deployment - shared between servers and endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# View agent errors

Agent Client Collector \(ACC\) errors are visible in logs related to the agent and the ServiceNow instance. This feature provides improved visibility of agent errors, enabling faster error resolution.

## Before you begin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agent Issues**.

    The **Errors** page appears and lists the errors compiled from the instance.

    The following columns display the indicated information about the errors.

<table id="table_dlc_s4b_fdc"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Key

</td><td>

Internal value used to identify the error.For data collection errors, specifies the **agent\_id** value.

</td></tr><tr><td>

Error Code

</td><td>

Error code assigned to the issue.

</td></tr><tr><td>

Refined Error Code

</td><td>

Optional modified error code. For example if the assigned **Error Code** is too generic, you can modify the value.

</td></tr><tr><td>

Error Category

</td><td>

The error category which the error is classified under.

</td></tr><tr><td>

Message

</td><td>

A message describing the error.

</td></tr><tr><td>

Error state

</td><td>

Indicates the state of the error: **Open** or **Resolved**.

</td></tr><tr><td>

Error Source

</td><td>

The application triggering the error.

</td></tr><tr><td>

Suppress

</td><td>

Indicates whether the error is to be ignored.

</td></tr><tr><td>

Last Occurrence

</td><td>

Time stamp with the most recent occurrence of the error.

</td></tr></tbody>
</table>    **Note:**

    -   Not all columns are visible by default on the page.
    -   Select the info icon \(\[Omitted image "info.png"\] Alt text: Info icon\) next to an error to view a pop-up window with full information about the error.

        \[Omitted image "acc-error-message-popup.png"\] Alt text: ACC Error Message popup window

        The info icon is visible when hovering under the search icon \(\[Omitted image "search-icon-magnifyingGlass.png"\] Alt text: Search icon\) next to the error entry.

    Alternatively, you can view information about the error by selecting it on the **Errors** page.

2.  To view errors for a specific agent:

    1.  Select **All** &gt; **Agent Client Collector** &gt; **Agents**.

        The **Agent Client Collectors** table appears.

    2.  Select an agent.

    3.  Select the **Automation Error Messages** tab at the bottom of the page to view errors relating to the agent.


## Result

If an error causes an agent's registration to fail, the agent's **Status** column displays **Registration Failure** on the Agent Client Collectors page \(**All** &gt; **Agent Client Collector** &gt; **Agents**\).

