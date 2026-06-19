---
title: Monitor relay connection health
description: View the heartbeat status of a private relay to verify connectivity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/monitor-relay-health.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-06-01"
reading_time_minutes: 1
keywords: [relay health, tunnel status, relay monitoring, Reverse Tunnel]
breadcrumb: [Use, Reverse Tunnel, Workflow Data Fabric]
---

# Monitor relay connection health

View the heartbeat status of a private relay to verify connectivity.

## Before you begin

The private relay must be deployed and registered. The registration status in the Relay \[sn\_zc\_tunnel\_relay\] table must be Successful.

Role required: sn\_zc\_tunnel.relay\_manager

## Procedure

1.  Navigate to **All** &gt; **Private Relay** &gt; **Relays**.

2.  Open the relay record to monitor.

3.  Review the health monitoring table on the relay record.

    |Field|Description|
    |-----|-----------|
    |Last Seen|Date and time of the last successful heartbeat from the relay, shown with relative age. Updated in real time.|


