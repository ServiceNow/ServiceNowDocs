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

-   Ensure that the Error Framework \(**com.glide.error\_framework**\) plugin is active.
-   Ensure that the system property **sn\_agent.use\_glide\_error\_framework** is set to **true** \(**All** &gt; **System properties** &gt; **All Properties**\).
-   Ensure that ACC Admin Workspace \(**sn\_acc\_wrksp**\) store application is active.

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **ITOM Infra Services Workspace**.

2.  Select the ACC agents \[Omitted image "acc-agents-icon.png"\] Alt text: ACC agents icon icon.

3.  Select **Errors** to view the errors existing on ACC agents.\[Omitted image "acc-agents-page.png"\] Alt text: ACC agents error page

4.  Filter the displayed errors by selecting severity and category values in the **Filter By** options.

    If you don't configure a filter, all agent errors appear.

5.  Select an error to view additional information, including the error's root cause and remediation instructions.\[Omitted image "agent-error-additional-info.png"\] Alt text: ACC error - additional info page

    1.  Select the **Errors** subtab to view detailed information about the error.

    2.  Select the information \[Omitted image "info.png"\] Alt text: Information icon icon to open the **Error details** panel.

        \[Omitted image "error-details-panel.png"\] Alt text: Error details panel

6.  To view errors for a specific agent:

    1.  Select **All** &gt; **Agent Client Collector** &gt; **Agents**.

        The **Agent Client Collectors** table appears.

    2.  Select an agent.

    3.  Select the **Automation Error Messages** tab at the bottom of the page to view errors relating to the agent.


