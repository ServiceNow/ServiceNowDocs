---
title: Reverse Tunnel release notes
description: The ServiceNow Reverse Tunnel application enables Zero Copy Connectors to reach private cloud or on-premises data sources through encrypted outbound connections, without opening inbound firewall ports. Reverse Tunnel is available in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-06-08"
reading_time_minutes: 1
keywords: [Reverse Tunnel, private connectivity, private relay, Zero Copy Connectors, Workflow Data Fabric]
---

# Reverse Tunnel release notes

The ServiceNow® Reverse Tunnel application enables Zero Copy Connectors to reach private cloud or on-premises data sources through encrypted outbound connections, without opening inbound firewall ports. Reverse Tunnel is available in the Australia release.

## Reverse Tunnel highlights for the Australia release

-   Connect Zero Copy Connectors to private cloud or on-premises data sources without opening inbound firewall ports.
-   Establish encrypted outbound connections to private cloud or on-premises data sources by deploying a private relay in your network.
-   Monitor relay heartbeat data directly from your ServiceNow instance.

See [Reverse Tunnel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/reverse-tunnel.md).

**Note:** Reverse Tunnel is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Reverse Tunnel features

-   **[Private connectivity for Zero Copy Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/exploring-reverse-tunnel.md)**

    Connect Zero Copy Connectors to data sources hosted in private cloud or on-premises networks without exposing data source credentials or IP addresses. The Reverse Tunnel gateway routes encrypted traffic between Workflow Data Fabric and private relays deployed in your private network, without decrypting that traffic.

-   **[Private relay deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/connect-customer-relay.md)**

    Deploy a private relay in your private network to establish an outbound encrypted connection to the Reverse Tunnel gateway. The relay uses the same placement and connectivity model as a MID Server. Authentication is handled automatically.

-   **[Relay heartbeat monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/monitor-relay-health.md)**

    Monitor relay heartbeat data directly from the relay record on your ServiceNow instance.

-   **[Service endpoint management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/manage-relay-services.md)**

    Register the fully qualified domain name \(FQDN\) and port number of each data source to the relay. The gateway uses registered service endpoints to route incoming traffic to the correct relay.


## Activation information

Reverse Tunnel is available in the ServiceNow Store. Install the following:

Install the Zero Copy Reverse Tunnel store app \(`sn_zc_tunnel`\) from the ServiceNow Store.

For details, see [Connect a private relay to the Reverse Tunnel gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/connect-customer-relay.md).

## Plugin information

-   **New plugins**

    The following plugin was added in the Australia release:

    Zero Copy Reverse Tunnel \(`sn_zc_tunnel`\): Provides the interface to manage private relays, service endpoints, and relay properties for private connectivity through the Reverse Tunnel gateway.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/build-automate-rn-landing.md)

