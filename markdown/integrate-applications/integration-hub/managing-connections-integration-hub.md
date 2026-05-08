---
title: Managing connections in Integration Hub
description: Create several connections to a single integration provider. View and configure connections in a simplified interface with the Connections dashboard.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration Hub, Workflow Data Fabric]
---

# Managing connections in Integration Hub

Create several connections to a single integration provider. View and configure connections in a simplified interface with the Connections dashboard.

## Connections and credentials in Integration Hub

Integration Hub uses aliases to manage connection information and credentials when integrating with external systems. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. Integration Hub only requires an alias, which then resolves to use the correct credentials and connection information during runtime. Learn more about credentials, connections, and aliases.

## Support for multiple connections

Integration Hub [supports multiple connections](support-multiple-connections.md) to a single integration provider. For example, you can have connections to several different Jira environments.

You can select which connection you want to use in a flow, and override preset connections for flows, subflows, and actions directly through Workflow Studio. When a flow is promoted to production, you can reestablish a connection to each account without needing to modify the flow.

You can also view, edit, and create connections for integration actions directly in Workflow Studio. Integration actions have one or more connection fields in the Action Properties section, simplifying connection management at the action-level.

## Personal Authentication dashboard

Use your personal credentials to connect to third-party integrations with the [Personal Authentication dashboard](personal-auth-dashboard.md). View, authenticate, revoke, and renew your personal authentications through a simplified, consolidated interface.

The Personal Authentication dashboard provides a streamlined way to manage your personal authentication integrations. With personal authentication, multiple users can use Integration Hub without needing to share superuser credentials. It also enhances security by removing the need to manage ACLs for third-party systems.

## Connections dashboard

You can view and configure your connection and credential aliases with the [Connections dashboard](connections-dashboard.md). The Connections dashboard enables you to manage multiple connections through a single interface, and provides simplified processes for adding, editing, and configuring connections. With the Connections dashboard, you can view details about an alias and all associated child connections in a single location.

## Use the mTLS protocol with a MID Server

Make outbound REST and SOAP calls through a MID Server [using mTLS](mtls-mid-server.md#). Store mTLS credential and certificate information on the instance, in a configuration file, or in an external vault. The MID Server retrieves the credential and certificate information and makes outbound REST and SOAP calls using the mTLS protocol.

