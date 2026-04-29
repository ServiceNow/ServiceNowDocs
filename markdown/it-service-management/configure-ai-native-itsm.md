---
title: Configure integrations and ITSM experiences in AI-native IT Service Management
description: Enable ITSM requester and fulfiller experiences by completing the essential configurations.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, AI-native IT Service Management, IT Service Management]
---

# Configure integrations and ITSM experiences in AI-native IT Service Management

Enable ITSM requester and fulfiller experiences by completing the essential configurations.

## Before you begin

Role required: admin

Ensure that both the Now Assist for Setup and AI-native IT Service Management applications are installed on your ServiceNow instance.

## Procedure

1.  From the header of your ServiceNow instance, navigate to **Admin** &gt; **Admin Home**.

2.  From the **Manage your products** section, select **View product overview** for AI-native IT Service Management.

    ![Set up AI-native ITSM application](../image/getStartedInstall.png)

3.  On the Product Hub page for AI-native IT Service Management, from **Configuration insights** section, select **Configure**.

    ![Applying default configurations for AI-native IT Service Management](../image/ai-native-configure-product-hub.png)

    **Important:** Do not change the current scope while presets are being configured.

4.  From the Configure AI-native IT Service Management page, perform any of the following tasks.

<table><thead><tr><th align="left" id="d457955e148">

Choice

</th><th align="left" id="d457955e151">

Description

</th></tr></thead><tbody><tr><td id="d457955e157">

**Configuration summary in the left navigation pane**

</td><td>

Provides the summary of configuration activity and progress.

</td></tr><tr><td id="d457955e166">

**Configure with Now Assist**

</td><td>

Configures AI-native IT Service Management using the Now Assist agent. It also displays all available AI agents in AI-native IT Service Management.

</td></tr><tr><td id="d457955e184">

**Configurations for Platform setup, employee, and fulfiller experiences in the left navigation pane**

</td><td>

For each module in the left navigation pane, view the default configurations \(if available\) and modify if necessary. -   Platform setup and integrations. See [Platform module configuration in Setup Hub](https://www.servicenow.com/docs/access?context=ia-config-platform-il&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Employee experience. See [Configuring the employee experience in AI-native IT Service Management](../concept/configuring-employee-experience-ai-native-itsm.md).
-   Fulfiller experience. See [Configuring the fulfiller experience in AI-native IT Service Management](../concept/configuring-fulfiller-experience-ai-native-itsm.md).
For information about configuration page options, see [Understand the Configuration page flow in Setup Hub](https://www.servicenow.com/docs/access?context=ia-configure-il&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

**Important:** For each configuration, use the guided configuration experience or the conversation AI agent \(if available\). You can use the conversation AI agent by selecting **Configure with Now Assist** on that configuration UI page. For information about AI agents for configurations, see [AI agents and agentic workflows in AI-native IT Service Management](../reference/agents-ai-native-it-service-desk.md).

</td></tr><tr><td id="d457955e252">

**Package and download**

</td><td>

Packages all configuration changes into an update set \(XML file\) and downloads it. You can upload this file for simplified migration to another instance.

</td></tr></tbody>
</table>    ![Applying default configurations for AI-native IT Service Management](../image/ai-native-itsm-config-ui-page.png "Service Level Management admin UI page with guided configuration experience and a conversation AI agent")


