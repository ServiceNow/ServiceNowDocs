---
title: Set default workspace for CCaaS
description: Configure and set a default workspace for contact center agents to let them navigate back to a workspace integrated with Interaction Controls Component \(ICC\), from any other unsupported workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/ccaas-set-default-workspace.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Enable ICC for CCaaS calls and callbacks, Phone channel, Enable communication channels, Configure, Customer Service Management]
---

# Set default workspace for CCaaS

Configure and set a default workspace for contact center agents to let them navigate back to a workspace integrated with Interaction Controls Component \(ICC\), from any other unsupported workspace.

## Before you begin

An interaction can be opened and details displayed in any workspace within the ServiceNow instance. However, if the workspace isn't integrated with ICC, then the global call controls supported by the ICC integration doesn't display in the workspace, rendering the workspace as unsupported.

Promote the Interaction Controls Component \(ICC\) plugin \(com.app\_interaction\_control\) is installed to use the ICC voice features for CCaaS.

Role required: **admin**

Configure the default workspace via OpenFrame within your ServiceNow instance as follows.

**Note:** Prerequisite for CCaaS callbacks: Verify that agents are configured through their contact center integration to receive callbacks and access the ServiceNow Workspace. Agent profiles are synced automatically when agents log in through the contact center connector in OpenFrame. For example, an agent must be able to log in to both the contact center and ServiceNow workspace. The agent presence state must match between both systems, as callbacks only route to available agents. In some cases, the state "available" might be labeled differently in the contact center, such as "on queue." Presence mismatches can prevent agents from receiving callbacks.

## Procedure

1.  Navigate to **All** &gt; **OpenFrame** &gt; **Configurations**.

2.  Create a configuration record for the specific CCaaS provider.

    Some CCaaS providers can include OpenFrame configurations for their plugin.

3.  Turn on the interaction controls for OpenFrame by selecting the **Enable interaction controls** check box.

4.  Checking the **Enable interaction controls** check box displays the **Default Experience** field.

5.  Click the Search icon to search through the list of available supported workspaces and select the workspace you want to set as default.

6.  From the **User Group** column, select a group and move it to the selected column.

    This user group refers to the group of users to whom the OpenFrame configuration applies.

7.  Unlock the URL field.

8.  In the URL field, enter a third-party URL.

    CaaS providers have specific configuration requirements for their plugins. Refer to the relevant contact center documentation for setup instructions.

9.  Select **Update**.


