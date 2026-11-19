---
title: Monitoring established connections
description: Maintain the health of established connections by monitoring connection status in Zero Copy Connector Hub.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/monitoring-connection-status-zcc.html
release: brazil
topic_type: concept
last_updated: "2026-11-17"
reading_time_minutes: 1
breadcrumb: [Manage zero copy connections, Zero Copy Connectors, Workflow Data Fabric]
---

# Monitoring established connections

Maintain the health of established connections by monitoring connection status in Zero Copy Connector Hub.

Determine whether a connection requires an update by checking the status on the **Established connections** tab.

|Status|Description|
|------|-----------|
|Connected|The connection to the data source has been tested and established.|
|Deactivated|The connection to the data source has been deactivated by the connection admin.|
|Needs configuration|The connection attributes or authentication information are missing from the connection details.|
|Needs mapping|The connection has been tested and established, but the data isn't mapped to a data fabric table.|
|Not connected|The connection details have been added, but the connection to the data source isn't working.|

Each connection on the **Established connections** tab appears as a card. The following table describes what each card shows.

|Item|Description|
|----|-----------|
|Source|The data source type and connection label.|
|Mapped tables|The number of data fabric tables mapped to this connection.|
|Status|The current connection status. See the preceding table for status descriptions.|

Use the following controls on the **Established connections** tab to find connections that need attention.

|Control|Description|
|-------|-----------|
|Search|Search for a connection by label or name.|
|Sources|Filter the list by data source type.|
|Status|Filter the list by connection status.|
|Created by|Filter the list by the user who created the connection.|
|Sort order|Sort connections by creation date or connection label.|

**Parent Topic:**[Managing zero copy connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/managing-connections-zcc.md)

