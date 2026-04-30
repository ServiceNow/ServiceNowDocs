---
title: Implement the Interaction Controls Component \(ICC\) for contact center integration
description: Implement prebuilt, certified integrations with Contact Center as a Service \(CCaaS\) providers using the ServiceNow voice reference architecture.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-03-24"
reading_time_minutes: 1
keywords: [ICC for contact center integration, ICC for CCaaS, NVC for CCaaS integration]
breadcrumb: [Enable communication channels, Configuring Customer Service Management, Customer Service Management]
---

# Implement the Interaction Controls Component \(ICC\) for contact center integration

Implement prebuilt, certified integrations with Contact Center as a Service \(CCaaS\) providers using the ServiceNow® voice reference architecture.

## About this task

The Interaction Controls Component \(ICC\) feature enables CCaaS providers to display native voice integrations so agents can manage customer calls directly from their configurable workspace.

For more information, see [Integrating contact centers with Interaction Controls Component \(ICC\) for voice calls](../concept/contact-center-integration-with-icc.md).

The voice controls display under the following conditions:

-   The interaction is a phone call.
-   The **Enable interaction controls** field is enabled on the OpenFrame Configuration record that allows the admin to configure the Agent Workspace to display voice interaction components.
-   The agent is a member of the user group specified on the OpenFrame Configuration record. If no user group is specified, all agents can access the CSM voice interaction record page.
-   Ensure the certified third-party App Store plugin is installed. For Example:
    -   [Unified Experience from Genesys](https://store.servicenow.com/store/app/cdff6b621ba46a50a85b16db234bcba3#linksAndDocuments)
    -   [Unified Experience from Genesys - Core](https://store.servicenow.com/store/app/6ebe67ea1b646a50a85b16db234bcb54)

## Before you begin

Ensure the Interaction Controls Component \(ICC\) plugin \(com.app\_interaction\_control\) is installed to use the ICC voice features for CCaaS.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **OpenFrame** &gt; **Configurations**.

2.  Create a new configuration record for the specific CCaaS provider.

    Some CCaaS providers can include OpenFrame configurations for their plugin.

3.  Turn on the interaction controls for OpenFrame by selecting the **Enable interaction controls** check box.

4.  From the **User Group** column, select a group and move it to the selected column.

    This is the group of users to whom the OpenFrame configuration applies.

5.  Unlock the URL field.

6.  In the URL field, enter a third-party URL.

    CaaS providers have specific configuration requirements for their plugins. Refer to the relevant contact center documentation for setup instructions.

7.  Select **Update**.


