---
title: Supporting multiple connections
description: Support several connections to a single integration provider. Select connections for flows, subflows, and actions directly from a flow.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Managing connections in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Supporting multiple connections

Support several connections to a single integration provider. Select connections for flows, subflows, and actions directly from a flow.

## Benefits

Multiple connections support offers these benefits.

-   Have more than one connection to the same integration provider. For example, you can establish connections to several different Jira environments.
-   Select which connection you want to use in a flow. Override preset connections for flows, subflows, and actions directly through Workflow Studio.
-   When a flow is promoted to production, reestablish a connection to each account without needing to modify the flow.

To learn more about connections, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## Create connections

There are two ways to add a child connection to a parent alias.

-   **Through the Connections dashboard**

    The Connections dashboard provides a simplified way to add a connection to an alias. For more information about the Connections dashboard, including how to add a connection, see [Using the Connections dashboard](connections-dashboard.md).

-   **Through the platform user interface**

    Manually create a child connection by setting up connection and credential records. To create a connection with this method, see [Create a Connection and Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).


## Flow-level connection selection

You can choose a connection for a flow or subflow directly from the flow's main page. When you select a new connection, it overrides any preconfigured connection for that flow. To choose a connection, click the More Actions menu icon \(![More Actions icon](../images/more-actions-menu-icon.png)\), and select the **Configure connections** option. This option opens the Configure Connections window, where you can select the connections for your flow. The Configure Connections window displays:

-   All the aliases used in the flow.
-   The icon and name for each alias.
-   A list of the configured connections for each alias. The default connection is listed first. Other connections are listed alphabetically.
-   An information icon for each alias. Clicking the icon opens the Connection &amp; Credential Aliases record for the default connection shown in the list.
-   A **Manage Connections** option that opens the connections dashboard.
-   Options to **Cancel** connection selection or **Update** your connection choice.

Each alias has one entry in the Configure Connections window, regardless of how many actions or subflows may use that alias. When you select a connection at the flow level, the new connection applies to all the actions and subflows using that alias. For example, if a flow has several actions that use a Slack service, changing the connection for the Slack service changes the connection for all the Slack service actions within the flow.

You can see which parts of a flow a connection change affects by matching the alias icons in the flow to the ones in the Configure Connections window. An action that impacts a Slack service has a Slack icon next to the action in the flow. The Slack icon also appears next to the alias name in the Configure Connections window.

The Configure Connections window is automatically updated whenever you add or delete a flow component that has connections. When you add an action or subflow to a flow, the Configure Connections window displays the connections for the action or subflow that you just added. If you remove an action or subflow, the connection information is removed from the Configure Connections window.

You can choose whether to display the **Configure connections** option with the **sn\_flow\_designer.connections\_override\_enabled** system property. Setting the property to **true** displays the **Configure connections** option, while setting it to **false** hides it. If you delete the system property or it doesn't exist, the **Configure connections** option is displayed by default.

View which connection your flow ran with by examining the Step Configuration section of the flow's execution details. The connection alias listed in the CONFIGURATION column is the alias that the flow was originally designed to run with. The alias listed in the RUNTIME VALUE column is the one that the flow actually ran with.

![Execution details page that displays the connection alias for the flow's default configuration and the flow's runtime value.](../images/mc-execution-details.png "Execution details page")

## Action-level connection selection

You can select connections for individual actions within a flow. This functionality is useful if a flow must interact with multiple configurations of the same provider. For example, downloading a file from one configuration of a file storage provider then uploading the file to a different configuration of the same file storage provider.

To select a connection for an individual action in a flow or subflow, click **Advanced Options**. This option shows the name of the alias that the action uses and a list of all the alias's associated connections. The first connection on the list is the default connection. Other connections are listed alphabetically. Selecting a connection from the list overrides the connection for that action and for any dynamic inputs inside the action.

You can enable or disable action-level overrides by clicking the More actions icon \(![More actions icon](../images/more-actions-menu-icon.png)\) and selecting **Flow Preferences**. The Configurations window has a **Show advanced connection options** option. This option is disabled by default, so actions don't show the **Advanced Options** button. When enabled, the option is available if the action has a connection alias that can be overridden.

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

-   If the alias has a template, configure the connection through the Connections dashboard. See [Configure a connection in the Connections dashboard](../tasks/dashboard-configure-connection.md) for instructions.
-   If an alias doesn't have a template, configure it through the platform user interface. For more information about configuring a connection without a template, see [Getting started with connections](https://www.servicenow.com/docs/access?context=connection-information&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## Additional considerations

To add a connection through the Connections dashboard, the parent alias must have a configuration template. Templates first became available in the Orlando release, so aliases from previous releases may not have templates yet. For more information about configuration templates, see [Connection and Credential configuration templates](https://www.servicenow.com/docs/access?context=spoke-configuration-template&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

**Parent Topic:**[Managing connections in Integration Hub](managing-connections-integration-hub.md)

