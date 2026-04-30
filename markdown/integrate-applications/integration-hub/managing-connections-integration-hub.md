---
title: Managing connections in Integration Hub
description: Create several connections to a single integration provider. View and configure connections in a simplified interface with the Connections dashboard.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integration Hub, Creating integrations with applications]
---

# Managing connections in Integration Hub

Create several connections to a single integration provider. View and configure connections in a simplified interface with the Connections dashboard.

Integration Hub uses aliases to manage connection information and credentials when integrating with external systems. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. Integration Hub only requires an alias, which then resolves to use the correct credentials and connection information during runtime. Learn more about [credentials, connections, and aliases](https://www.servicenow.com/docs/access?context=credentials-connections-alias&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## Support for multiple connections

Integration Hub supports multiple connections to a single integration provider. For example, you can have connections to several different Jira environments.

You can select which connection you want to use in a flow, and override preset connections for flows, subflows, and actions directly through Workflow Studio. When a flow is promoted to production, you can reestablish a connection to each account without needing to modify the flow.

## Connections dashboard

You can view and configure your connection and credential aliases with the Connections dashboard. The Connections dashboard enables you to manage multiple connections through a single interface, and provides simplified processes for adding, editing, and configuring connections. With the Connections dashboard, you can view details about an alias and all associated child connections in a single location.

-   **[Using the Personal Authentication dashboard](personal-auth-dashboard.md)**  
Use your personal credentials to connect to third-party integrations. View, authenticate, revoke, and renew your personal authentications through a simplified, consolidated interface.
-   **[Using the mTLS protocol with a MID Server](mtls-mid-server.md#)**  
Make outbound REST and SOAP calls through a MID Server using mTLS. Store mTLS credential and certificate information on the instance, in a configuration file, or in an external vault. The MID Server retrieves the credential and certificate information and makes outbound REST and SOAP calls using the mTLS protocol.
-   **[Supporting multiple connections](support-multiple-connections.md)**  
Support several connections to a single integration provider. Select connections for flows, subflows, and actions directly from a flow.
-   **[Override a connection in a flow](../tasks/override-connection-flow.md)**  
Override a connection for a flow, subflow, or action.
-   **[Using the Connections dashboard](connections-dashboard.md)**  
View and configure your connection and credential aliases through a simplified interface. Add new connections, edit existing connections, and view connection details.
-   **[Add a connection in the Connections dashboard](../tasks/dashboard-add-connection.md)**  
Add a connection through the Connections dashboard.
-   **[Configure a connection in the Connections dashboard](../tasks/dashboard-configure-connection.md)**  
Configure a connection through the Connections dashboard.

**Parent Topic:**[Integration Hub](integrationhub.md)

