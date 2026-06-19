---
title: Manage relay service endpoints through Reverse Tunnel
description: Add or update the service endpoints assigned to a private relay to control which data sources are accessible through Reverse Tunnel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/manage-relay-services.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-06-01"
reading_time_minutes: 1
keywords: [relay service endpoints, FQDN, Reverse Tunnel, relay management]
breadcrumb: [Use, Reverse Tunnel, Workflow Data Fabric]
---

# Manage relay service endpoints through Reverse Tunnel

Add or update the service endpoints assigned to a private relay to control which data sources are accessible through Reverse Tunnel.

## Before you begin

The private relay must be deployed, registered, and connected. The registration status in the relay \[sn\_zc\_tunnel\_relay\] table must be Successful.

Role required: sn\_zc\_tunnel.relay\_manager

## About this task

Service endpoints specify the hostname and port of each data source routed through the relay.

## Procedure

1.  Navigate to **All** &gt; **Private Relay** &gt; **Relays**.

2.  Open the relay record.

3.  In the relay record, select **Unlock Services** to unlock the Services field.

4.  Select **Lookup using list** to open the Service Endpoints list.

5.  Select **New**.

6.  Enter a name for the service endpoint and the FQDN and port number of the data source.

    For example: `acme.snowflakecomputing.com:443`.

    When creating a Zero Copy Connectors connection, the connection URL hostname must exactly match the fully qualified domain name \(FQDN\) registered as a service endpoint.

7.  Select **Submit**.

8.  Save the relay record.


## Result

The new service endpoint is reported to the gateway, which routes incoming traffic from Zero Copy Connectors to the correct relay.

## What to do next

If the backend data source has an IP allowlist restriction, verify that the relay is running on a machine whose IP address is on the allowlist.

