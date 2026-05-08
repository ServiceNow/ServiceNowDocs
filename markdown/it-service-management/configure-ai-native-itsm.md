---
title: Configure integrations and ITSM experiences in Simplified IT Service Management
description: Enable ITSM requester and fulfiller experiences by completing the essential configurations.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure and integrate, Simplified IT Service Management, IT Service Management]
---

# Configure integrations and ITSM experiences in Simplified IT Service Management

Enable ITSM requester and fulfiller experiences by completing the essential configurations.

## Before you begin

Role required: admin

Ensure that both the Now Assist for Setup and IT Service Management applications are installed on your ServiceNow instance.

## Procedure

1.  From the header of your ServiceNow instance, navigate to **Admin** &gt; **Admin Home**.

2.  From the **Manage your products** section, select **View product overview** for IT Service Management.

    ![Set up Simplified ITSM application](../image/getStartedInstall2.png)

3.  On the Product Hub page for IT Service Management, from **Configuration insights** section, select **Configure**.

    ![Applying default configurations for Simplified IT Service Management](../image/ai-native-configure-product-hub2.png)

    **Important:** Do not change the current scope while presets are being configured.

4.  From the Configure IT Service Management page, perform any of the following tasks.

<table><thead><tr><th align="left" id="d460421e156">

Choice

</th><th align="left" id="d460421e159">

Description

</th></tr></thead><tbody><tr><td id="d460421e165">

**Configuration summary in the left navigation pane**

</td><td>

Provides the summary of configuration activity and progress.

</td></tr><tr><td id="d460421e174">

**Configure with Now Assist**

</td><td>

Configures Simplified IT Service Management using the Now Assist agent. It also displays all available AI agents in IT Service Management.

</td></tr><tr><td id="d460421e192">

**Configurations for Platform setup, employee, and fulfiller experiences in the left navigation pane**

</td><td>

For each module in the left navigation pane, view the default configurations \(if available\) and modify if necessary. -   Platform setup and integrations. See [Platform module configuration in Now Assist for Setup](https://www.servicenow.com/docs/access?context=ia-config-platform-il&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Employee experience. See [Configuring the employee experience in Simplified IT Service Management](../concept/configuring-employee-experience-ai-native-itsm.md).
-   Fulfiller experience. See [Configuring the fulfiller experience in Simplified IT Service Management](../concept/configuring-fulfiller-experience-ai-native-itsm.md).
For information about configuration page options, see [Understand the Configuration page flow in Now Assist for Setup](https://www.servicenow.com/docs/access?context=ia-configure-il&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

**Important:** For each configuration, use the guided configuration experience or the conversation AI agent \(if available\). You can use the conversation AI agent by selecting **Configure with Now Assist** on that configuration UI page. For information about AI agents for configurations, see [AI agents and agentic workflows in Simplified IT Service Management](../reference/agents-ai-native-it-service-desk.md).

</td></tr><tr><td id="d460421e260">

**Package and download**

</td><td>

Packages all configuration changes into an update set \(XML file\) and downloads it. You can upload this file for simplified migration to another instance.

</td></tr></tbody>
</table>    ![Applying default configurations for AI-native IT Service Management](../image/ai-native-itsm-config-ui-page2.png "Service Level Management admin UI page with guided configuration experience and a conversation AI agent")


