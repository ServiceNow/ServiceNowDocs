---
title: Agent Client Collector \(ACC\) diagnostic workflow
description: Enable and use AI agents to examine agent behavior through the Agent Client Collector \(ACC\) diagnostic workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/use-acc-diagnostic-workflow.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector \(ACC\) diagnostic workflow

Enable and use AI agents to examine agent behavior through the Agent Client Collector \(ACC\) diagnostic workflow.

## Before you begin

-   Ensure that the ServiceNow Otto panel is enabled on your instance. For details, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md).
-   Ensure that ServiceNow Otto for IT Operations Management \(ITOM\) is installed on your instance. For more information, see [Install the ServiceNow Otto for IT Operations Management \(ITOM\) application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/install-now-assist-itom.md).
-   Enable the Agent Client Collector diagnostic workflow in AI Agent Studio.
    1.  Select **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
    2.  On the **Agentic workflows** tab, select **Agent Client Collector \(ACC\) Diagnostic**.
    3.  Select the **Select channels and status** option.
    4.  In the **Engage via the ServiceNow Otto** panel, slide the **Display** toggle bar to the right \(active\).
-   Role required: agent\_client\_collector\_admin, agent\_client\_collector\_user, or now\_assist\_panel\_user

## About this task

Invoke the Agent Client Collector \(ACC\) diagnostic workflow to:

-   Question issues of an ACC agent while on an ACC form.
-   Request suggestions to remediate a specific ACC error code.

## Procedure

1.  In a ServiceNow instance, select the ServiceNow Otto icon \(\[Omitted image "now-assist-icon.png"\] Alt text: ServiceNow Otto icon\).

2.  In the ServiceNow Otto panel, enter prompts to invoke the ACC diagnostic workflow and perform remediation actions on the agent.

    Possible prompts include:

    -   Diagnose issues with ACC agent &lt;agent name&gt;
    -   Multiple errors on &lt;agent name&gt;, diagnose them
    -   Provide suggestions to remediate ACC error code &lt;error code number&gt;

## Result

An error report is generated, based on the activity logged by the Agent Client Collector Framework.

