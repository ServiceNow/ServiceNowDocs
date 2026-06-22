---
title: Configure integrations and ITSM experiences in Simplified IT Service Management
description: Enable ITSM requester and fulfiller experiences by completing the essential configurations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/configure-ai-native-itsm.html
release: australia
product: IT Service Management
classification: it-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure and integrate, Simplified IT Service Management, IT Service Management]
---

# Configure integrations and ITSM experiences in Simplified IT Service Management

Enable ITSM requester and fulfiller experiences by completing the essential configurations.

## Before you begin

Role required: admin

Ensure that both the Setup Hub and the relevant IT Service Management application based on your subscription are installed on your ServiceNow instance.

## Procedure

1.  From the header of your ServiceNow instance, navigate to **Admin** &gt; **Admin Home**.

2.  From the **Manage your products** section, select IT Service Management.

    \[Omitted image "aiNativegetStartedwithInstall.png"\] Alt text: Set up Simplified ITSM application

3.  On the Product Hub page for IT Service Management, from the **Configure your product** section, select **Configure**.

    \[Omitted image "ai-native-configure-product-hub.png"\] Alt text: configuring IT Service Management

4.  From the Configure IT Service Management page, perform any of the following tasks.

<table><thead><tr><th align="left" id="d147418e148">

Choice

</th><th align="left" id="d147418e151">

Description

</th></tr></thead><tbody><tr><td id="d147418e157">

**Configuration summary in the left navigation pane**

</td><td>

Provides the summary of configuration activity and progress.

</td></tr><tr><td id="d147418e166">

**Configure with Now Assist**

</td><td>

Configures Simplified IT Service Management using the Now Assist agent. It also displays all available AI agents in IT Service Management. Ensure that the Now Assist with Setup Hub application is installed. See [Set up Now Assist with Setup Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/ia-setup-now-assist.md).

</td></tr><tr><td id="d147418e191">

**Configurations for Platform setup, employee, and fulfiller experiences in the left navigation pane**

</td><td>

For each module in the left navigation pane, view the default configurations \(if available\) and modify if necessary. -   Platform setup and integrations. See [Platform module configuration in Setup Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/ia-config-platform-il.md).
-   Employee experience. See [Configuring the employee experience in Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configuring-employee-experience-ai-native-itsm.md).
-   Fulfiller experience. See [Configuring the fulfiller experience in Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configuring-fulfiller-experience-ai-native-itsm.md).
For information about configuration page options, see [Understand the Configuration page flow in Setup Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/ia-configure-il.md).

**Important:** For each configuration, use the guided configuration experience or the conversation AI agent \(if available\). You can use the conversation AI agent by selecting **Configure with Now Assist** on that configuration UI page. For information about AI agents for configurations, see [AI agents and agentic workflows in Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/agents-ai-native-it-service-desk.md).

</td></tr><tr><td id="d147418e259">

**Package and download**

</td><td>

Packages all configuration changes into an update set \(XML file\) and downloads it. You can upload this file for simplified migration to another instance.

</td></tr></tbody>
</table>    \[Omitted image "ai-native-config-summary.png"\] Alt text: Configuring ITSM


-   **[Configuring the employee experience in Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configuring-employee-experience-ai-native-itsm.md)**  
Enable an AI-first comprehensive employee experience focused on a simplified portal with an AI-first chat approach to find answers, order items, check status, and create incidents.
-   **[Configuring the fulfiller experience in Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configuring-fulfiller-experience-ai-native-itsm.md)**  
Enable an AI-first fulfiller experience for simplified incident and request management.

**Parent Topic:**[Configuring Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configuring-ai-native-itsm.md)

