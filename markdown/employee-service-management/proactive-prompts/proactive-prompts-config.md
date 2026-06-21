---
title: Configuring Proactive Prompts
description: If you have the admin role, you can install the Proactive Prompts application and configure it to display the relevant prompts to the employees in your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/employee-service-management/proactive-prompts/proactive-prompts-config.html
release: xanadu
product: Proactive Prompts
classification: proactive-prompts
topic_type: concept
last_updated: "2024-08-21"
reading_time_minutes: 1
breadcrumb: [Proactive Prompts, HR Service Delivery, Employee Service Management]
---

# Configuring Proactive Prompts

If you have the admin role, you can install the Proactive Prompts application and configure it to display the relevant prompts to the employees in your organization.

A signal is the configuration for prompts about when to send them, what to send, whom to send them to, where to send them, and the related actions to generate and deliver them. You can define whom to send the signal to, how often, and on what channels. The Proactive Prompts application supports all conversational interface \(CI\) channels in the portal.

**Note:** You must install and activate both the Proactive Prompts and the Now Assist for HRSD application to use the capability and prompts from the base system. The two new signals that are available for use are the Approvals pending prompt and the High leave balance prompt.

Configuring Proactive Prompts is a multi-step process:

-   [Creating a signal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/proactive-prompts/proactive-prompts-signal-create.md). A signal determines when to send the prompt, what to send, whom to send it to, where to send it, and the related actions to generate and deliver the prompts.
-   [Creating a data source for the signal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/proactive-prompts/proactive-prompts-signal-data-source.md). The signal data source brings in the most relevant information for your employees.
-   [Configuring channels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/proactive-prompts/proactive-prompts-config-channels.md). Choose where to display the prompts that would be the most benefit to your users.
-   [Configure actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/proactive-prompts/proactive-prompts-signal-actions.md). You determine the actions to generate and deliver the prompts.
-   [Configuring schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/proactive-prompts/proactive-prompts-signal-schedules.md). You choose the frequency that you want the data source to process the data and to generate the prompts in the selected channels.

