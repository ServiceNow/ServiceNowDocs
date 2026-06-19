---
title: Exploring Reverse Tunnel
description: Reverse Tunnel enables Zero Copy Connectors to reach private or on-premises data sources through encrypted outbound connections without having to open inbound firewall ports.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/exploring-reverse-tunnel.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: concept
last_updated: "2026-05-31"
reading_time_minutes: 2
keywords: [Reverse Tunnel, private connectivity, Zero Copy Connectors, Workflow Data Fabric]
breadcrumb: [Reverse Tunnel, Workflow Data Fabric]
---

# Exploring Reverse Tunnel

Reverse Tunnel enables Zero Copy Connectors to reach private or on-premises data sources through encrypted outbound connections without having to open inbound firewall ports.

## Reverse Tunnel overview

Reverse Tunnel extends Zero Copy Connectors access to data sources hosted in private cloud networks or on-premises networks. Because it accepts outbound connections from private relays deployed in the customer network and routes encrypted traffic to the correct data source without decrypting it, Zero Copy Connectors can reach data sources that aren't publicly accessible.

## Key components

-   **Gateway**

    The central infrastructure component hosted on the ServiceNow platform that accepts authenticated connections from private relays, enforces registration and hostname authorization, and routes encrypted traffic to customer-side data sources.

-   **Private relay**

    A component deployed in the customer network that connects outbound to the gateway and proxies traffic between the gateway and the customer's private cloud data source. The relay is deployed in the customer network and operates like a MID Server in placement and connectivity.


**Note:** Private relays authenticate with the gateway automatically using certificates issued by the ServiceNow instance. Certificate configuration and management are handled automatically.

-   **Gateway Controller**

    Manages gateway instances on the ServiceNow platform. Handles gateway creation and assignment to private relays.


## Reverse Tunnel users

|User|Description|
|----|-----------|
|Relay manager|Registers and manages private relays and monitors relay connection and registration health. Requires the sn\_zc\_tunnel.relay\_manager role.|
|Relay user|A service account that the private relay uses to authenticate with the instance and fetch its configuration.|

## Reverse Tunnel workflow

The setup workflow involves the following primary activities:

1.  Install the `sn_zc_tunnel` \(Zero Copy Reverse Tunnel\), which provides the interface to manage relays and services.
2.  Service account creation: The relay manager creates a service account in User Administration with the sn\_zc\_tunnel.relay\_user role and notes the password for relay configuration.
3.  Relay setup: The relay manager downloads the relay artifact `Reverse Tunnel Relay` from the store app, extracts the files, and configures and starts the relay.
4.  Relay record configuration: After the relay starts, the relay registers with the instance and a new record is created in the `sn_zc_tunnel_relay` table. The relay manager requests a gateway instance.

    Two gateway records are automatically attached to the Gateways field, tied to the instance name.

5.  Backend services registration: The relay manager adds a service endpoint to the relay record for each data source to be accessed through the tunnel. For details, see [Manage relay service endpoints through Reverse Tunnel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/manage-relay-services.md).
6.  Zero Copy Connectors connection setup: The relay manager configures the connector in Zero Copy Connectors with the required credentials and tests the connection.

## Reverse Tunnel benefits

|Benefit|Feature|
|-------|-------|
|Connect to private cloud or on-premises data sources without having to open inbound firewall ports.|Reverse Tunnel|
|Establish encrypted connections between your private network and Workflow Data Fabric without exposing data source credentials or IP addresses.|Reverse Tunnel|
|Manage and monitor private relay registrations and connection health from your ServiceNow instance.|[Monitoring relay connectivity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/using-reverse-tunnel.md)|

## What to explore next

To learn more about configuring and using Reverse Tunnel, see:

-   [Configuring Reverse Tunnel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/configuring-reverse-tunnel.md)
-   [Monitoring relay connectivity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/using-reverse-tunnel.md)

