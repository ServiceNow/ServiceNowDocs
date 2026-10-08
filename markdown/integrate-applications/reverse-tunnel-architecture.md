---
title: Reverse Tunnel architecture
description: A private relay opens outbound connections to your instance and to the gateway. Knowing the ports and their purposes helps you configure firewall rules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/reverse-tunnel-architecture.html
release: brazil
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 3
keywords: [Reverse Tunnel, architecture, private relay, gateway, ports]
breadcrumb: [Explore, Reverse Tunnel, Workflow Data Fabric]
---

# Reverse Tunnel architecture

A private relay opens outbound connections to your instance and to the gateway. Knowing the ports and their purposes helps you configure firewall rules.

Reverse Tunnel requires outbound access on port 443 and on two gateway ports, a data port and an admin port. Use the information in this topic to explain the purpose of each host and port when you request firewall changes.

For descriptions of the gateway, private relay, and Gateway Controller, see [Exploring Reverse Tunnel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/exploring-reverse-tunnel.md).

## How it works

The figure shows the connections between the customer network and the ServiceNow network.\[Omitted image "reverse-tunnel-architecture-diagram.png"\] Alt text: The relay connects outbound to the instance on port 443 and to the gateway on the admin and data ports. The relay forwards requests to the data source.

Reverse Tunnel components communicate in the following sequence:

1.  The private relay connects to your ServiceNow instance on port 443 to register, request its certificate, and retrieve its relay and tunnel configuration.
2.  When the relay registers, the instance attaches gateway records to the relay record, creating them if they don't already exist.
3.  The relay opens outbound connections to each gateway host on the admin port and the data port, and uses its certificate to authenticate with the gateway.
4.  When Zero Copy Connectors sends a request for a data source in your network, the gateway routes the request through the data port connection to the relay.
5.  The relay forwards the request to the data source registered as a service endpoint on the relay record.

For details about how the gateway authenticates the relay, see [Reverse Tunnel mTLS authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/reverse-tunnel-mtls.md).

## Hosts and ports the relay connects to

The relay host machine requires outbound access to the hosts and ports in the following table. For gateway hosts, the **Data Port** and **Admin Port** fields in each gateway record are the source for the port numbers. The table lists the values currently in use.

|Host|Port|Purpose|
|----|----|-------|
|ServiceNow instance|443|Relay registration, certificate signing requests, retrieval of relay and tunnel configuration, and periodic checks for configuration updates|
|Each gateway host|4281 \(**Data Port** field\)|Requests from the instance to data sources in your environment|
|Each gateway host|4290 \(**Admin Port** field\)|Tunnel-related activities, such as health checks|

To find the gateway hostnames for your relay, see [Verify outbound network access for a private relay](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/verify-relay-outbound-access.md).

## Considerations

-   Gateway hostnames aren't available until the relay registers with the instance. Your network administrator must open port 443 to the instance first. After the gateways appear on the relay record, open the data port and admin port to each gateway host.
-   The relay connects to multiple gateway hosts for redundancy and reliability. ServiceNow determines the number of gateway hosts, and the number can change. Each gateway host requires access on both the data port and the admin port.
-   How you configure outbound firewall rules depends on your network environment and is managed by your network administrator.

**Related topics**  


[Verify outbound network access for a private relay](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/verify-relay-outbound-access.md)

[Connect a private relay to the Reverse Tunnel gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/connect-customer-relay.md)

