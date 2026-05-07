---
title: Global call list
description: Use the global call list capability enabled via OpenFrame integration. Access call controls to manage voice calls using the phone icon available in any workspace within your ServiceNow instance to ensure efficient call management without losing access to call controls.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [ICC for voice calls, Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# Global call list

Use the global call list capability enabled via OpenFrame integration. Access call controls to manage voice calls using the phone icon available in any workspace within your ServiceNow instance to ensure efficient call management without losing access to call controls.

## Global call list overview

Enterprises can integrate with any third-party Contact Center as a Service \(CCaaS\) voice call capability within their ServiceNow instance. Using the global call list call controls, agents can initiate new phone calls by using the dial pad or phone directory and manage existing calls. This capability enables agents to access their contact details, queues, and other relevant information via integrated contact center.

Every call creates an interaction record with the call details, which can be accessed by selecting the **Open interaction** link in the call window. The interaction opens in a supported or unsupported workspace based on your integration settings. The feature allows agents to access and manage call controls from a phone icon, regardless of the workspace or tab they are in. Agents can move freely between tabs or other workspaces that don't support the call control capability.

The following screenshot gives you the context for the global call list view.

![Global call list view in the ServiceNow instance](../image/ccaas-global-call-list.png "Global call list view")

The global call list provides the following functionality:

-   **Switching workspaces during active calls**

    Agents can switch between different workspaces while on an active phone call, ensuring continued access to necessary information and tools without losing call controls.

-   **Accepting calls outside ICC supported workspaces**

    Agents can accept phone calls from workspaces even if they aren't integrated with the Interaction Controls Component \(ICC\) voice controls.

-   **Navigating to supported workspaces**

    If the current workspace is supported, agents can select the **Open interaction** link from the voice control screen to open the interaction and display the details.

-   **Improved call management**

    The badge on the phone icon keeps agents informed and helps them track the number of active phone calls. The feature is particularly useful in workspaces that do not support call controls, ensuring the agent can manage calls effectively regardless of the tab or workspace they are in.


## Global call list scenarios

Before going over some typical scenarios, let's review certain terms for insight on the global call list feature:

<table id="table_cgy_zb3_yfc"><thead><tr><th>

Workspace terms

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Current Workspace

</td><td>

Workspace the agent is currently on.

</td></tr><tr><td>

Supported Workspace

</td><td>

Workspace integrated with ICC call controls.

</td></tr><tr><td>

Unsupported Workspace

</td><td>

Workspace not integrated with ICC call controls.

</td></tr><tr><td>

Default Workspace

</td><td>

Workspace configured via OpenFrame enables agents to navigate to an ICC integrated workspace if they are in an unsupported workspace. See: [Set default workspace for CCaaS](../task/ccaas-set-default-workspace.md).

</td></tr></tbody>
</table>Let’s go over some scenarios to understand how an agent can switch between supported and unsupported workspaces while managing inbound and outbound calls:

-   **Scenario 1**

    The global call list is available from an unsupported workspace, which allows the agent to accept and manage calls. The agent can accept a call and select the **Open interaction** link to open the interaction record in the default workspace.

-   **Scenario 2**

    The agent is in an active call in a supported workspace, and during the call moves to an unsupported workspace. The call control is available to the agent via the phone icon in the global call list window.

-   **Scenario 3**

    The agent selects the phone icon to open the phone dial pad to make an outbound call from an unsupported workspace. The related interaction record opens in the agent’s current unsupported workspace. However, the agent must have default workspace configured to see the current call in the Interaction screen.

    **Note:** See: [Set default workspace for CCaaS](../task/ccaas-set-default-workspace.md).

-   **Scenario 4**

    The agent can access and display the global call list from anywhere within the ServiceNow instance by selecting the phone icon. Selecting the Open interaction link displays the call details with the global call controls in their default workspace.

    **Note:** The default workspace must be set by the contact center admin.

-   **Scenario 5**

    The agent ends a call from an unsupported workspace. Selecting the interaction record links from the call that just ended or for other previous calls, displays in the same unsupported workspace the agent is in.


## Global call list features

The feature streamlines the call handling experience for contact center agents. Agents can access call controls and manage calls while viewing other resources in supported or unsupported tabs in their ServiceNow instance.

From the global call list view, Agents can do the following:

-   Initiate new calls using either the keypad or the phone directory and view a list of queues, other agent names, and external contacts in the phone directory.
-   Use Search in the phone directory to display a maximum list of 25 results at a time. The limit can be set by configuring the system property setting called`icc_search_limit` using an integer value. The default minimum value is 10, and a limit can be set to return a maximum of 25 results according to list of queues, agents, or external data.
-   Use the phone icon next to the search input field to make outbound calls to an external number that doesn't display in the Queues, Agent, or External tab results.
-   View and access call controls even when navigating to other tabs and screens. The global call list icon is available from supported and unsupported workspaces.
-   View a badge count on the phone icon indicating the number of ongoing calls.
-   Select the **Open interaction** link to open the interaction record details in their supported workspace in call resiliency mode. See: [Call resiliency](ccaas-call-resiliency.md).

**Note:** The Transfer function isn't supported in the global call list feature.

