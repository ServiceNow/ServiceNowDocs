---
title: Configure relay behavior
description: Configure relay behavior by setting properties in the Relay Property \[sn\_zc\_tunnel\_relay\_prop\] table on your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/configure-relay-properties.html
release: brazil
topic_type: task
last_updated: "2026-10-06"
reading_time_minutes: 1
keywords: [relay properties, Reverse Tunnel, private relay]
breadcrumb: [Configure, Reverse Tunnel, Workflow Data Fabric]
---

# Configure relay behavior

Configure relay behavior by setting properties in the Relay Property \[sn\_zc\_tunnel\_relay\_prop\] table on your instance.

## Before you begin

-   The Reverse Tunnel store app must be installed.
-   The private relay must be deployed and registered. For more information, see [Connect a private relay to the Reverse Tunnel gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/connect-customer-relay.md).

Role required: sn\_zc\_tunnel.relay\_manager

## About this task

Properties set in the Relay Property \[sn\_zc\_tunnel\_relay\_prop\] table are retrieved dynamically during the relay configuration polling cycle and applied without restarting the relay. Use the instance table for most configuration changes.

The relay also supports a `config.yaml` file shipped with the relay artifact. Properties set in `config.yaml` take precedence over instance properties. Modify `config.yaml` only when instance-level configuration is not sufficient. For example, to set properties before the relay registers with the instance for the first time.

## Procedure

1.  Navigate to **All** &gt; **Private Relay** &gt; **Relays**.

2.  Open the relay record.

3.  In the Relay Properties related list, select **New**.

4.  Enter the property name and value.

    For example, to enable debug logging, set the property name to `debug` and the value to `true`.

    For a list of available properties and their defaults, see Relay properties.

    Invalid property values fall back to defaults, and a warning is logged. Configuration polling is not affected.

5.  Select **Submit**.


## Result

The new property value is applied during the next configuration polling cycle without requiring a restart.

