---
title: Configuring Reverse Tunnel
description: Configure Reverse Tunnel to establish secure, private connectivity between your private cloud data sources and Workflow Data Fabric.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/configuring-reverse-tunnel.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: concept
last_updated: "2026-05-31"
reading_time_minutes: 1
keywords: [Reverse Tunnel configuration, private relay setup]
breadcrumb: [Reverse Tunnel, Workflow Data Fabric]
---

# Configuring Reverse Tunnel

Configure Reverse Tunnel to establish secure, private connectivity between your private cloud data sources and Workflow Data Fabric.

## Configuration overview

Private relays authenticate with the gateway automatically using certificates issued by the ServiceNow instance. No certificate configuration is required.

1.  [Connect a private relay to the Reverse Tunnel gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/connect-customer-relay.md) — Configure and register a private relay to establish an encrypted connection to the Reverse Tunnel Gateway.
2.  [Configure relay behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/configure-relay-properties.md) — Set relay behavior using the relay properties table or the `config.yaml` file.

