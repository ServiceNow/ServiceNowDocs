---
title: Configure relay behavior
description: Configure relay behavior by setting properties either in the config.yaml file or in the relay properties table on your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/configure-relay-properties.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-06-18"
reading_time_minutes: 2
keywords: [relay properties, Reverse Tunnel, private relay]
breadcrumb: [Configure, Reverse Tunnel, Workflow Data Fabric]
---

# Configure relay behavior

Configure relay behavior by setting properties either in the `config.yaml` file or in the relay properties table on your instance.

## Before you begin

-   The Reverse Tunnel store app must be installed.
-   The private relay must be deployed and registered.

Role required: sn\_zc\_tunnel.relay\_manager

## About this task

The private relay supports two configuration sources:

-   **`config.yaml`**

    A configuration file shipped with the relay zip file and deployed in your environment. Properties set in `config.yaml` take precedence over properties set on the instance. Modifying this file does not require a relay restart as changes are applied automatically. If issues occur, restarting the relay applies the changes immediately.

    Modify `config.yaml` only when you have a functional or business reason to do so.

-   **Relay properties table \(ServiceNow instance\)**

    Properties configured in the relay properties table on your ServiceNow instance are retrieved dynamically during the relay configuration polling cycle. Changes are applied without restarting the relay. Use the relay properties table for most configuration changes to avoid relay restarts.


|Property|Default|Description|
|--------|-------|-----------|
|**reconnect-multiplier**|2|Multiplier applied to the reconnect interval when the relay retries a connection to the gateway.|
|**reconnect-jitter**|0.3|Jitter applied to the reconnect interval to prevent simultaneous reconnection attempts from multiple relays.|
|**config-poll-interval**|30000 ms|Interval in milliseconds at which the relay polls the instance for configuration updates.|
|**debug**|false|When set to true, enables debug logging on the relay.|
|**reregistration-max-attempts**|5|Number of retry attempts made when registering backend services with the gateway instance. If all attempts are exhausted, the gateway connection is closed.|
|**max-streams**|10000|Maximum number of concurrent streams supported. When the cap is reached, new streams are rejected and traffic is distributed to another relay.|
|**stream-window-kb**|256 KB|Flow control window size in kilobytes for each stream. Controls the amount of data in flight per stream.|
|**cert-reissue-window**|30 days|Number of days before certificate expiry at which the relay initiates certificate renewal. The relay generates a new certificate signing request and re-establishes the connection using the renewed certificate.|
|**http-request-timeout**|30000 ms|Timeout in milliseconds for HTTP requests made by the relay to the instance.|
|**reconnect-initial-delay**|1000 ms|Delay in milliseconds before the relay attempts to reconnect to the gateway.|
|**reconnect-max-delay**|60000 ms|Maximum delay in milliseconds between reconnection attempts.|
|**cert-monitor-interval**|86400000 ms|Interval in milliseconds between certificate expiration checks.|
|**glide.kmf.issuing.reverse\_tunnel\_relay.validity\_ms**|365 days|Validity period of the relay certificate. Minimum: 1 millisecond. Maximum: 20 years.|

## Procedure

1.  Navigate to **All** &gt; **Private Relay** &gt; **Relays**.

2.  Open the relay record.

3.  In the Relay Properties related list, select **New**.

4.  Enter the property name and value.

    For example, to enable debug logging, you would set the property name to `debug` and the value to `true`.

    Invalid property values fall back to defaults, and a warning is logged. Configuration polling is not affected.

5.  Select **Submit**.


## Result

The new property value is applied during the next configuration polling cycle without requiring a restart.

