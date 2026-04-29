---
title: Connections and Credentials
description: The Connections and Credentials page is where you create, configure, and manage all connections between ServiceNow and external systems. This is where you store authentication credentials and establish the actual communication links.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Connect, Workflow Data Fabric Home, Workflow Data Fabric]
---

# Connections and Credentials

The **Connections and Credentials** page is where you create, configure, and manage all connections between ServiceNow and external systems. This is where you store authentication credentials and establish the actual communication links.

## Outbound connections

Outbound connections are integrations where ServiceNow initiates communication to an external system. ServiceNow calls the external system to read data, write data, or trigger actions.

When you create an outbound connection, you:

-   Select the external system
-   Choose a connector type
-   Configure authentication credentials
-   Set up endpoints for different environments
-   Save the connection for use in workflows

See [Set up outbound connections](../task/connecthub-set-up-outbound-connections.md) for detailed steps.

## Inbound connections

Inbound connections are integrations where an external system initiates communication to ServiceNow. The external system sends data, events, or triggers actions in ServiceNow.

When you create an inbound connection, you:

-   Select the external system
-   Choose a spoke to handle the incoming data
-   Configure authentication credentials
-   Activate the connection to generate an endpoint URL
-   Share the endpoint URL with the external system

See [Set up inbound connections](../task/connecthub-set-up-inbound-connections.md) for detailed steps.

## Credentials and security

All credentials stored in Connections and Credentials are encrypted and securely managed by ServiceNow. Credentials include:

-   Usernames and passwords
-   API keys and tokens
-   OAuth credentials

You can update credentials anytime without affecting the connection configuration. Changes apply immediately to new requests.

## Connection status

Each connection displays a status indicating its health and readiness. Status values include:

-   Configured - Connection is configured
-   Connected - Connection is working and ready to use
-   Expired - Authentication credentials have expired
-   Not Configured - Connection is not configured yet
-   Deactivated - Connection exists but is not active

## Managing multiple connections

You can create multiple connections to the same external system for different environments or purposes. Each connection is independent with its own credentials and configuration.

For example, you might have:

-   Jira Production connection
-   Jira Staging connection
-   Jira Development connection

Each connection can use different credentials and settings while using the same connector type.

