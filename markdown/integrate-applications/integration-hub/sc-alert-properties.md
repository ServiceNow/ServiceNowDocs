---
title: Stream Connect Alerting properties
description: Specify alert properties and how alerts are managed in Stream Connect.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Alerting, Using Stream Connect for Apache Kafka, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Stream Connect Alerting properties

Specify alert properties and how alerts are managed in Stream Connect.

## Alerts

To view Stream Connect Alerting properties, navigate to **Integration Hub** &gt; **Stream Connect** &gt; **Alert Properties**. You must have the stream\_connect\_viewer role to view alerting properties and stream\_commect\_admin role to modify alerting properties.

The Stream Connect Alerting UI has the following alerts.

-   Producer Failed Alert. Triggered when a producer fails to produce messages to a topic.
-   Queue Depth Processing Time Alert. Triggered when the estimated message processing time exceeds the specified value.
-   Consumer Poll Failed Alert. Triggered when a consumer is unable to connect to a topic or read the messages in a topic. For example, if a topic is deleted from Hermes while the associated subscription is still active.
-   Consumer Processing Alert. Triggered when a consumer fails to process messages from a topic.
-   Topic Replication Failed Age Alert. Triggered when the topic replication status remains FAILED for longer than the specified value.
-   Topic Replication Inactivity Alert. Triggered when topic replication is inactive for longer than the specified value.
-   Undelivered Messages Age Alert. Triggered when no messages are delivered to a topic for longer than the specified value. For example, if a producer is running but unable to send data due to network issues or misconfiguration, and the delivery gap exceeds the threshold.
-   Unprocessed Messages Age Alert. Triggered when messages remain unprocessed in a topic for longer than the specified value. For example, if a consumer is assigned to a topic but fails to process messages due to a crash, lag, or misconfiguration, and the message backlog exceeds the threshold.

<table id="table_jqk_y2t_tdc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Alert level

</td><td>

Severity level for the alert.

 The options are:

-   IGNORED
-   INFO
-   WARNING
-   CRITICAL

 Default: CRITICAL

</td></tr><tr><td>

Time interval, in seconds, required between two detections to have them count as separate events.

</td><td>

The minimum number of seconds to wait before sending another notification for the same alert. Detections within this time interval count as a single alert and are linked to the same alert record.

 Default: 3600 seconds

</td></tr><tr><td>

Specifies the number of separate notifications to send when there's a Producer Failed Alert for multiple topics. Select **Global** to receive a single notification, or **Per Topic** to receive a notification for each topic.

</td><td>

Select **Per Topic** to create an alert for each topic, or **Global** to create one alert for all topics.

 Default: Global

</td></tr></tbody>
</table><table id="table_gkg_bft_tdc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Threshold, in seconds, for the queue depth processing time estimate to be considered info.

</td><td>

If the estimated queue processing time is greater than this value, generate an alert with a severity of INFO.

 Default: 0 seconds

 A value of 0 disables the alert at the specified severity level. To completely disable the alert, set the value to 0 for all three severity levels \(INFO, WARNING, and CRITICAL\).

</td></tr><tr><td>

Threshold, in seconds, for the queue depth processing time estimate to be considered a warning.

</td><td>

If the estimated queue processing time is greater than this value, generate an alert with a severity of WARNING.

 Default: 14400 seconds

</td></tr><tr><td>

Threshold, in seconds, for the queue depth processing time estimate to be considered critical.

</td><td>

If the estimated queue processing time is greater than this value, generate an alert with a severity of CRITICAL.

 Default: 86400 seconds

</td></tr><tr><td>

Time interval, in seconds, required between two detections to have them count as separate events.

</td><td>

The minimum number of seconds to wait before sending another notification for the same alert. Detections within this time interval count as a single alert and are linked to the same alert record.

 Default: 3600 seconds

</td></tr><tr><td>

Specifies the number of separate notifications to send when there's a Queue Depth Alert for multiple consumers. Select **Global** to receive a single notification, or **Per Consumer** to receive a notification for each consumer.

</td><td>

Select **Per Consumer** to create an alert for each consumer, or **Global** to create one alert for all consumers.

 Default: Global

</td></tr></tbody>
</table><table id="table_nrz_cft_tdc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Alert level

</td><td>

Severity level for the alert.

 The options are:

-   IGNORED
-   INFO
-   WARNING
-   CRITICAL

 Default: CRITICAL

</td></tr><tr><td>

Time interval, in seconds, required between two detections to have them count as separate events.

</td><td>

The minimum number of seconds to wait before sending another notification for the same alert. Detections within this time interval count as a single alert and are linked to the same alert record.

 Default: 3600 seconds

</td></tr><tr><td>

Specifies the number of separate notifications to send when there's a Consumer Poll Failed Alert for multiple consumers. Select **Global** to receive a single notification, or **Per Consumer** to receive a notification for each consumer.

</td><td>

Select **Per Consumer** to create an alert for each consumer, or **Global** to create one alert for all consumers.

 Default: Global

</td></tr></tbody>
</table><table id="table_wsw_2ft_tdc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Alert level

</td><td>

Severity level for the alert.

 The options are:

-   IGNORED
-   INFO
-   WARNING
-   CRITICAL

 Default: WARNING

</td></tr><tr><td>

Time interval, in seconds, required between two detections to have them count as separate events.

</td><td>

The minimum number of seconds to wait before sending another notification for the same alert. Detections within this time interval count as a single alert and are linked to the same alert record.

 Default: 3600 seconds

</td></tr><tr><td>

Specifies the number of separate notifications to send when there's a Consumer Processing Alert for multiple consumers. Select **Global** to receive a single notification, or **Per Consumer** to receive a notification for each consumer.

</td><td>

Select **Per Consumer** to create an alert for each consumer, or **Global** to create one alert for all consumers.

 Default: Per Consumer

</td></tr></tbody>
</table><table id="table_qvg_gft_tdc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Threshold, in seconds, for the topic replication failed age estimate to be considered info.

</td><td>

Triggered when the topic replication status remains FAILED for longer than the specified value. With a MID Server cluster, this alert is triggered if any of the MID Servers in the cluster has a topic replication status that remains FAILED for longer than the specified value.

 Default: 0 seconds

 A value of 0 disables the alert at the specified severity level. To completely disable the alert, set the value to 0 for all three severity levels \(INFO, WARNING, and CRITICAL\).

</td></tr><tr><td>

Threshold, in seconds, for the topic replication failed age estimate to be considered a warning.

</td><td>

If the topic replication status remains FAILED for longer than this value, generate an alert with a severity of WARNING.

 Default: 1800 seconds

</td></tr><tr><td>

Threshold, in seconds, for the topic replication failed age estimate to be considered critical.

</td><td>

If the topic replication status remains FAILED for longer than this value, generate an alert with a severity of CRITICAL.

 Default: 3600 seconds

</td></tr><tr><td>

Time interval, in seconds, required between two detections to have them count as separate events.

</td><td>

The minimum number of seconds to wait before sending another notification for the same alert. Detections within this time interval count as a single alert and are linked to the same alert record.

 Default: 3600 seconds

</td></tr><tr><td>

Specifies the number of separate notifications to send when there's a Topic Replication Failed Alert for multiple topic replications. Select **Global** to receive a single notification, or **Per Topic Replication** to receive a notification for each topic replication.

</td><td>

Select **Per Topic Replication** to create an alert for each topic replication, or **Global** to create one alert for all topic replications.

 Default: Global

</td></tr></tbody>
</table><table id="table_ihw_gft_tdc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Threshold, in seconds, for the topic replication inactivity estimate to be considered info.

</td><td>

If there are no messages replicated between the source and destination topic by any server for longer than this value, generate an alert with a severity of INFO.

Default: 14400 seconds

</td></tr><tr><td>

Threshold, in seconds, for the topic replication inactivity estimate to be considered a warning.

</td><td>

If topic replication is inactive for longer than this value, generate an alert with a severity of WARNING.

</td></tr><tr><td>

Threshold, in seconds, for the topic replication inactivity estimate to be considered critical.

</td><td>

If topic replication is inactive for longer than this value, generate an alert with a severity of CRITICAL.

</td></tr><tr><td>

Time interval, in seconds, required between two detections to have them count as separate events.

</td><td>

The minimum number of seconds to wait before sending another notification for the same alert. Detections within this time interval count as a single alert and are linked to the same alert record.

 Default: 3600 seconds

</td></tr><tr><td>

Specifies the number of separate notifications to send when there's a Topic Replication Inactivity Alert for multiple replications. Select **Global** to receive a single notification, or **Per Topic Replication** to receive a notification for each topic replication.

</td><td>

Select **Per Topic Replication** to create an alert for each topic replication, or **Global** to create one alert for all topic replications.

 Default: Per Topic Replication

</td></tr></tbody>
</table><table id="table_qch_nmh_nhc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Threshold in seconds for undelivered messages age to be considered as an info

</td><td>

If no messages are delivered for longer than this value, generate an alert with a severity of INFO. A value of 0 disables the alert at the INFO level. To completely disable the alert, set the value to 0 for all three severity levels.

 Default: 3600

</td></tr><tr><td>

Threshold in seconds for undelivered messages age to be considered a warning

</td><td>

If no messages are delivered for longer than this value, generate an alert with a severity of WARNING. A value of 0 disables the alert at the WARNING level.

 Default: 14400

</td></tr><tr><td>

Threshold in seconds for undelivered messages age to be considered critical

</td><td>

If no messages are delivered for longer than this value, generate an alert with a severity of CRITICAL. A value of 0 disables the alert at the CRITICAL level.

 Default: 28800

</td></tr><tr><td>

Time interval, in seconds, required between two detections to have them count as separate alerts. The Undelivered Messages Age Alert is configured to run hourly by default. To modify this interval, please consult the documentation for guidance.

</td><td>

The minimum number of seconds to wait before sending another notification for the same alert. Detections within this time interval count as a single alert and are linked to the same alert record. The Undelivered Messages Age Alert is configured to run hourly by default.

 Default: 3600

</td></tr><tr><td>

Specifies the number of separate notifications to send when there's an Undelivered Messages Age Alert.

</td><td>

This setting is always set to **Global**. Only one alert notification is generated, even if multiple topics are affected.

 Default: Global

</td></tr></tbody>
</table><table id="table_glj_qmh_nhc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Threshold in seconds for unprocessed messages age to be considered info

</td><td>

If no messages are processed for longer than this value, generate an alert with a severity of INFO. A value of 0 disables the alert at the INFO level. To completely disable the alert, set the value to 0 for all three severity levels.

 Default: 3600

</td></tr><tr><td>

Threshold in seconds for unprocessed messages age to be considered a warning

</td><td>

If no messages are processed for longer than this value, generate an alert with a severity of WARNING. A value of 0 disables the alert at the WARNING level.

 Default: 14400

</td></tr><tr><td>

Threshold in seconds for unprocessed messages age to be considered critical

</td><td>

If no messages are processed for longer than this value, generate an alert with a severity of CRITICAL. A value of 0 disables the alert at the CRITICAL level.

 Default: 28800

</td></tr><tr><td>

Time interval, in seconds, required between two detections to have them count as separate alerts

</td><td>

The minimum number of seconds to wait before sending another notification for the same alert. Detections within this time interval count as a single alert and are linked to the same alert record.

 Default: 3600

</td></tr><tr><td>

Specifies the number of separate notifications to send when there's an Unprocessed Messages Age Alert.

</td><td>

Determines how many alert notifications are generated. This is always set to **Global**, meaning only one alert notification is created regardless of how many topics are affected.

 Default: Global

</td></tr></tbody>
</table>**Parent Topic:**[Stream Connect alerting](../concept/stream-connect-alert.md)

