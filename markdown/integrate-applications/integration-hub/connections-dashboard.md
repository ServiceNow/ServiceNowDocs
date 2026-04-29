---
title: Using the Connections dashboard
description: View and configure your connection and credential aliases through a simplified interface. Add new connections, edit existing connections, and view connection details.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage connections, Integration Hub, Workflow Data Fabric]
---

# Using the Connections dashboard

View and configure your connection and credential aliases through a simplified interface. Add new connections, edit existing connections, and view connection details.

## Benefits

The Connections dashboard provides these benefits:

-   Enables connection admins to manage multiple connections through a single interface.
-   Provides simplified processes for adding, editing, and configuring connections.
-   Displays details about an alias and all associated child connections in a single location.

## Landing page

The dashboard landing page displays all the connection and credential aliases available on your instance. You can search for an alias by name, sort aliases by date created, or sort them alphabetically in ascending or descending order.

Each alias is displayed in a card format. Cards display the following:

-   The application's icon.
-   The name and scope of the parent alias.
-   A short description of the application associated with the alias. This option only appears when there are no connections.
-   The total number of connections.
-   A list of all the connections associated with the alias. The first connection is the default parent connection.
-   A **View Details** option that displays specific information about the alias and any child connections.
-   An **Advanced Setup** option. This option only appears when an alias doesn't have a configuration template.
-   An **Add Connection** option. This option is only available when an alias has a configuration template.

Each page of the Connections dashboard displays a maximum of 12 aliases. Page through to see additional aliases.

## Detailed view

View details about an alias and any child connections by clicking the **View Details** option on the alias card. The details page has two columns. The first column displays:

-   The application's icon.
-   The name and scope of the parent alias.
-   An option to **View connection alias**, which opens the associated Connection &amp; Credential Aliases record.

The second column of the detailed view displays:

-   An **Add Connection** or **Advanced Setup** option, depending on whether the alias has a configuration template.
-   The number of connections associated with the alias.
-   A list of connections associated with the alias. The default connection is marked.

Connections that are not configured have a **Configure** option. Connections that are configured have an **Edit** option. Each configured connection displays the connection name, endpoint, credential name, and credential type.

If an alias uses an OAuth credential, the OAuth access or refresh token status is displayed with each connection. For connections that require a new token, you can request one by clicking **Get OAuth Token**.

## Configuration templates

Configuration templates enable you to set up complex integrations using a single form. For example, an OAuth integration requires registering an OAuth provider, generating a token, and creating several connection and credential records. But if you use a configuration template to set up an OAuth integration, you only need to fill in one form. The system creates the associated records. To learn more about templates, see [Connection and Credential configuration templates](https://www.servicenow.com/docs/access?context=spoke-configuration-template&version=australia&pubname=australia-platform-security&ft:locale=en-US).

To add, edit, or configure connections directly through the dashboard, an alias must have a configuration template. Not all aliases have templates. Templates were first introduced in the Orlando release, so aliases from previous versions may not have them yet. An alias without a template displays an **Advanced Setup** option on both its dashboard and detailed view. Clicking **Advanced Setup** opens the alias's connection and credential record, where you can set up the alias. For more information about working with aliases that don't have templates, see [Create a Connection and Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Unconfigured connections

When you transfer an alias or promote it to production, its underlying connection information doesn't get transferred with it. In this situation, the connection is in an unconfigured state and must be reconfigured before you can use it. You can reestablish the underlying connections either through the dashboard or through the platform user interface.

-   If the alias has a template, you can configure the connection through the dashboard.
-   If it doesn't have a template, configure it through the platform user interface. For more information about configuring a connection without a template, see [Getting started with connections](https://www.servicenow.com/docs/access?context=connection-information&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Roles

To access the Connections dashboard, you must have the connection\_admin or admin role.

