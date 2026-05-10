---
title: Supporting multiple connections
description: Support several connections to a single integration provider. Select connections for flows, subflows, and actions directly from a flow.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Manage connections, Integration Hub, Workflow Data Fabric]
---

# Supporting multiple connections

Support several connections to a single integration provider. Select connections for flows, subflows, and actions directly from a flow.

## Benefits

Multiple connections support offers these benefits.

-   Have more than one connection to the same integration provider. For example, you can establish connections to several different Jira environments.
-   Select which connection you want to use in a flow. Override preset connections for flows, subflows, and actions directly through Workflow Studio.
-   When a flow is promoted to production, reestablish a connection to each account without needing to modify the flow.

To learn more about connections, see [Connections and Credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r-credentials.md).

## Connection and credential aliases

Integration Hub uses aliases to manage connection information and credentials when integrating with external systems. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. Integration Hub only requires an alias, which then resolves to use the correct credentials and connection information during runtime.

With connection and credential aliases, you can also create additional aliases or connections called child aliases. Child aliases enable you to create multiple connections within the same application integration. For more information, see [Create a Connection and Credential alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/connection-alias.md).

## Flow-level connection selection

You can choose a connection for a flow or subflow directly from the flow's main page. When you select a new connection, it overrides any preconfigured connection for that flow. To choose a connection, select the More Actions menu icon \(![More Actions icon](../images/more-actions-menu-icon.png)\), and select the **Configure connections** option. This option opens the Configure Connections window, where you can select the connections for your flow. The Configure Connections window displays:

-   All the aliases used in the flow.
-   The icon and name for each alias.
-   A list of the configured connections for each alias. The default connection is listed first. Other connections are listed alphabetically.
-   An information icon for each alias. Selecting the icon opens the Connection &amp; Credential Aliases record for the default connection shown in the list.
-   A **Manage Connections** option that opens the connections dashboard.
-   Options to **Cancel** connection selection or **Update** your connection choice.

Each alias has one entry in the Configure Connections window, regardless of how many actions or subflows may use that alias. When you select a connection at the flow level, the new connection applies to all the actions and subflows using that alias. For example, if a flow has several actions that use a Slack service, changing the connection for the Slack service changes the connection for all the Slack service actions within the flow.

You can see which parts of a flow a connection change affects by matching the alias icons in the flow to the ones in the Configure Connections window. An action that impacts a Slack service has a Slack icon next to the action in the flow. The Slack icon also appears next to the alias name in the Configure Connections window.

The Configure Connections window is automatically updated whenever you add or delete a flow component that has connections. When you add an action or subflow to a flow, the Configure Connections window displays the connections for the action or subflow that you just added. If you remove an action or subflow, the connection information is removed from the Configure Connections window.

You can choose whether to display the **Configure connections** option with the **sn\_flow\_designer.connections\_override\_enabled** system property. Setting the property to **true** displays the **Configure connections** option, while setting it to **false** hides it. If you delete the system property or it doesn't exist, the **Configure connections** option is displayed by default.

View which connection your flow ran with by examining the Step Configuration section of the flow's execution details. The connection alias listed in the CONFIGURATION column is the alias that the flow was originally designed to run with. The alias listed in the RUNTIME VALUE column is the one that the flow actually ran with.

![Execution details page that displays the connection alias for the flow's default configuration and the flow's runtime value.](../images/mc-execution-details.png "Execution details page")

## Action-level connection selection

You can select connections for individual integration actions within a flow. This functionality is useful if a flow must interact with multiple configurations of the same provider. For example, downloading a file from one configuration of a file storage provider then uploading the file to a different configuration of the same file storage provider.

Integration actions have one or more connection fields in the Action Properties section where you can edit or configure a connection. If the connection alias is using a configuration template with a test action, you can also test the connection from here. For details, see [Create a test action to test a connection alias from a configuration template](../tasks/test-alias-configuration-template.md).

In the following example, the Create Remote Incident action has a connection field called **ServiceNow Connection**. The default connection hasn’t been configured yet, so a `Connection not configured` message appears below the connection field. This message appears whenever the connection for the selected alias is not configured

![Integration action showing the connection field in the Action Properties section.](../images/integration-action-connection.png "Example of a connection field in an integration action")

Use the gear icon \(![gear icon](../../../build/app-engine-studio/image/gear-icon.png)\) to create or configure an alias.

-   For connections using a [configuration template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/spoke-configuration-template.md), the gear icon opens a window where you can create or configure a connection.
-   For connections without a configuration template, the gear icon opens the platform form for [creating a connection and credential alias.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/connection-alias.md)

Use the plus icon \(![plus icon](../../../reuse/icons/product-icons/plus-outline-24.svg)\) to add a new child connection alias.

The pencil icon \(![pencil icon](../../../reuse/icons/product-icons/pencil-outline-24.svg), not shown in the image\) opens the Edit Connection window where you can edit the selected connection. If the connection is using a configuration template with a test action, you can test the connection by using the **Save and Test** button.

## Dynamic inputs

You can select connections for flows and subflows containing actions with dynamic inputs. When a connection override is specified at the flow level, the dynamic action uses the flow-level override. For example, in a flow with a data-gathering action, the action uses the flow's override connection for the data-gathering step rather than the action's default connection. If an override is specified at the action level, the dynamic action uses the action-level override.

## Multiple overrides within a flow

When there is more than one override in a flow, they're applied according to the following rules:

-   Action-level overrides always apply.
-   Subflow-level overrides always apply to the subflow. The override also applies to actions within the subflow that don't have their own overrides configured.
-   Flow-level overrides apply to subflows and actions that don't have their own overrides configured.

## Flow promotion

When you move a flow to a production instance, the alias information is transferred with it, but the underlying connection information is not. An alias functions as a type of container for connections. The container moves with the flow, but the specific connection information doesn't. Any connections associated with the alias become unconfigured and must be reconfigured before you can use them in the new environment.

You can configure connections without having to modify the flow because you already have the base alias set up. To configure a connection:

-   If the alias has a configuration template, configure the connection through the Connections dashboard. See [Configure a connection in the Connections dashboard](../tasks/dashboard-configure-connection.md) for instructions.
-   If an alias doesn't have a configuration template, configure it through the platform user interface. For more information about configuring a connection without a template, see [Getting started with connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/connection-information.md).

