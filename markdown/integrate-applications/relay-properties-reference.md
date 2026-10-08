---
title: Relay properties
description: Relay properties control connection, polling, certificate, and logging behavior for a private relay. Set these properties in the Relay Property \[sn\_zc\_tunnel\_relay\_prop\] table on your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/relay-properties-reference.html
release: zurich
topic_type: reference
last_updated: "2026-10-06"
reading_time_minutes: 1
keywords: [relay properties, Reverse Tunnel, private relay]
breadcrumb: [Reference, Reverse Tunnel, Workflow Data Fabric]
---

# Relay properties

Relay properties control connection, polling, certificate, and logging behavior for a private relay. Set these properties in the Relay Property \[sn\_zc\_tunnel\_relay\_prop\] table on your instance.

|Property|Default|Description|
|--------|-------|-----------|
|**reconnect-multiplier**|2|Multiplier applied to the reconnect interval when the relay retries a connection to the gateway.|
|**reconnect-jitter**|0.3|Random variation applied to the reconnect interval to prevent multiple relays from attempting to reconnect at the same time.|
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

