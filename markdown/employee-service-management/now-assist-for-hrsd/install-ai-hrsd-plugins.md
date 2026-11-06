---
title: Install AI for HR Service Delivery plugins
description: Install the plugins that provide AI capabilities for HR Service Delivery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/now-assist-for-hrsd/install-ai-hrsd-plugins.html
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2026-10-13"
reading_time_minutes: 1
breadcrumb: [Configure, ServiceNow Otto for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Install AI for HR Service Delivery plugins

Install the plugins that provide AI capabilities for HR Service Delivery.

## Before you begin

Role required: admin

Confirm the following applications are already configured on your instance:

-   HR Service Delivery \[com.sn\_hr\_core\]
-   ServiceNow Otto for Platform \(sn\_genai\_platform\)
-   If installing HR Voice AI Agents plugin: ServiceNow Otto for Voice \[sn\_voice\_aia\]

## About this task

The following table lists the plugins and what each one provides.

<table><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ServiceNow Otto for HR Service Delivery \(HRSD\)\[sn\_hr\_gen\_ai\]

</td><td>

Adds AI capabilities to HR Service Delivery so employees and HR agents can get answers and complete HR tasks faster.

</td></tr><tr><td>

AI Agents for HR Service Delivery\[sn\_hr\_ai\_agents\]

</td><td>

Adds AI agents that automate HR tasks, such as helping HR agents work on cases.

</td></tr><tr><td>

HR Voice AI Agents \[sn\_hr\_voice\_aia\]

</td><td>

Lets employees and HR agents interact with HR AI capabilities by voice.

</td></tr><tr><td>

ServiceNow Otto for HRSD – Galileo Inside\[sn\_hr\_na\_galileo\]

</td><td>

Enable users to access HR articles and industry research from Galileo by The Josh Bersin Company.

</td></tr><tr><td>

HRSD MCP Server\[sn\_hr\_mcp\_server\]

</td><td>

Exposes HR Service Delivery capabilities to MCP-compatible clients, including Claude and Moveworks.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  In the search field, enter the name or ID of the plugin.

3.  Select the plugin.

4.  Select **Install**.

5.  In the dialog box, review the dependencies and select Install again.

6.  Repeat steps 2 through 5 for each plugin in the table.

7.  Wait for the installation to finish.


## Result

The plugins are installed on your instance. You can now configure the AI features for HR Service Delivery.

**Parent Topic:**[Configure ServiceNow Otto for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/configure-now-assist-hr.md)

