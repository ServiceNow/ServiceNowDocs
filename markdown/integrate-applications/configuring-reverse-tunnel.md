---
title: Configuring Reverse Tunnel
description: Configure Reverse Tunnel to establish secure, private connectivity between your private cloud data sources and Workflow Data Fabric.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/configuring-reverse-tunnel.html
release: zurich
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Reverse Tunnel configuration, private relay setup]
breadcrumb: [Reverse Tunnel, Workflow Data Fabric]
---

# Configuring Reverse Tunnel

Configure Reverse Tunnel to establish secure, private connectivity between your private cloud data sources and Workflow Data Fabric.

## Configuration overview

Private relays authenticate with the gateway automatically by using certificates. ServiceNow issues and renews the certificates, so you don't need to configure or manage them.

1.  [Connect a private relay to the Reverse Tunnel gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/connect-customer-relay.md) — Configure and register a private relay to establish an encrypted connection to the Reverse Tunnel Gateway.
2.  [Configure relay behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/configure-relay-properties.md) — Set relay behavior using the `Relay Property [sn_zc_tunnel_relay_prop]` table or the `config.yaml` file.

