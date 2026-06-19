---
title: Connect a private relay to the Reverse Tunnel gateway
description: Configure and register a private relay to establish an encrypted connection to the Reverse Tunnel gateway.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/connect-customer-relay.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-06-18"
reading_time_minutes: 2
keywords: [private relay, relay registration, Reverse Tunnel, config.yaml]
breadcrumb: [Configure, Reverse Tunnel, Workflow Data Fabric]
---

# Connect a private relay to the Reverse Tunnel gateway

Configure and register a private relay to establish an encrypted connection to the Reverse Tunnel gateway.

## Before you begin

-   The Reverse Tunnel store app must be available in the ServiceNow Store.
-   The host machine must be running Linux x86-64 or Windows x86-64.
-   The host machine must have outbound network access to the ServiceNow instance on port 443 and to the gateway on ports 8090 and 8081.
-   A user account must be available to create a service account for the relay.

Role required: sn\_zc\_tunnel.relay\_manager

## Procedure

1.  Download the relay artifact Reverse Tunnel Relay from the ServiceNow Store.

2.  Extract the artifact files.

3.  Configure and start the relay following the README instructions included in the extracted artifact.

4.  Navigate to **All** &gt; **Private Relay** &gt; **Relays** and verify a relay record was created.

    **Note:** After successful registration, a record ID is stored in the `config.yaml` file. Do not modify or remove this value.

5.  In the relay record, select **Create gateway** to create a gateway instance.

    **Note:** Selecting this action more than once is safe — only the first selection creates the gateway. Two gateway records are automatically attached to the Gateways field, tied to the instance name.

6.  Register backend services to the relay.

    1.  Note the fully qualified domain name \(FQDN\) and port number of the data source you want to access through the tunnel.

        For example: `acme.snowflakecomputing.com:443`.

    2.  In the relay record, select **Unlock Services**.

    3.  Select the Lookup using list icon \[Omitted image "lookup-using-list-icon.png"\] Alt text: to open the Service Endpoints list.

    4.  Select **New**.

    5.  Enter a name for the service endpoint and the FQDN and port number.

    6.  Select **Submit**.

    7.  Save the record.

    Assigned services are reported to the gateway, which routes incoming traffic to the correct relay. To add or update service endpoints after initial setup, see [Manage relay service endpoints through Reverse Tunnel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/manage-relay-services.md).

7.  Set up the zero copy connection.

    1.  Navigate to **All** &gt; **Zero Copy Connectors** \(Workflow Data Fabric\).

    2.  Select the connector you want to configure with the relay.

    3.  Enter the credentials for the connector.

        **Note:** The connection URL hostname must exactly match the FQDN registered as a service endpoint. If the backend data source has an IP allowlist restriction, verify the relay is running on the same machine that is on the allowlist.

    4.  Select **Test Connection**.

        If the connection test succeeds, the private tunnel setup is complete.


