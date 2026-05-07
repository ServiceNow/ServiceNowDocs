---
title: Implement the Interaction Controls Component \(ICC\) for contact center voice call and callback integrations
description: Implement prebuilt, certified integrations with Contact Center as a Service \(CCaaS\) providers using the ServiceNow voice reference architecture.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [ICC for contact center integration, ICC for CCaaS, NVC for CCaaS integration]
breadcrumb: [Phone channel, Enable communication channels, Configure, Customer Service Management]
---

# Implement the Interaction Controls Component \(ICC\) for contact center voice call and callback integrations

Implement prebuilt, certified integrations with Contact Center as a Service \(CCaaS\) providers using the ServiceNow® voice reference architecture.

## About this task

The Interaction Controls Component \(ICC\) feature enables CCaaS providers to display native voiceand callbackintegrations so agents can manage customer calls directly from their configurable workspace.

For more information, see [Interaction Controls Component \(ICC\) for voice calls](../concept/contact-center-integration-with-icc.md) and [Integrating contact centers with Interaction Controls Component \(ICC\) for callbacks](../concept/interaction-controls-component-icc-callback-integration-features.md).

The voice controls and callback controls display under the following conditions:

-   When the interaction is a phone call, voice controls display.When the interaction is a phone call that is associated with a callback task, the callback controls display.
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


## What to do next

Refer to [Plugin requirements for voice and callback integrations with contact centers](plugin-requirements-for-external-call-routing-integration-for-contact-centers.md) for dependencies and address all prerequisite requirements to access the ICC features.

