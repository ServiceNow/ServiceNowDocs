---
title: Stream Connect alerting
description: Receive alerts and alert notifications for Stream Connect integrations.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2024-11-15"
reading_time_minutes: 6
breadcrumb: [Using Stream Connect for Apache Kafka, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Stream Connect alerting

Receive alerts and alert notifications for Stream Connect integrations.

Stream Connect uses both active and scheduled monitoring to detect events across multiple Stream Connect components. If an issue is detected, the system creates an alert, logs a message to the Stream Connect Log, and sends out an alert notification.

## Alerts

Stream Connect uses both event-type alerts and threshold alerts. Each type of alert has a set of alerting properties that specify how to handle the alert.

-   Event-type alerts \(or real-time alerts\) are created when there's an error in a Stream Connect component. For example, when a producer is unable to write to a topic, or a consumer is unable to read from a topic. These alerts are built into to the code and use the alerting properties to determine the severity level and when to send a notification. Event-type alerts are detected through active monitoring which uses various mechanisms to detect events across multiple Stream Connect components. The system caches the configuration and detects the events when they occur.

-   Threshold alerts are created when a value transitions from below the threshold to at or above the threshold. For example, when the lag on a topic goes beyond a certain number of messages, or the processing time of the messages in a topic is above a specified value. When a threshold alert decreases from at or above a threshold to below it, the active flag on the alert is set to false. Threshold alerts are detected through scheduled monitoring, where a scheduled job runs scripted checks on Stream Connect integrations. An alert is generated for thresholds that meet the alert configuration specified by the alerting properties.


For a list and description of the alerts, or to configure alerting properties, see [Stream Connect Alerting properties](../reference/sc-alert-properties.md). You must have the Kafka Admin role to view or modify alerting properties.

## Alert table

When an alert is triggered for the first time, an Alert \[sys\_sc\_alert\] record is added to the Stream Connect Alerts \[sys\_sc\_alerts\] table. If the same alert is triggered again, and the original alert record is still active, the record’s **Last Detections \[last\_detection\]** field is updated. If the original alert record is not active, a new record is added to the alerts table. An alert record is deactivated when the alert has not been triggered for a specified amount of time. This time interval varies depending on the type of alert and can be modified in the [Stream Connect Alerting properties](../reference/sc-alert-properties.md) UI.

The Stream Connect alerts table shows if an alert is active and the alert's severity level, type, and updated date. It also displays:

-   An alert's **Number**, which references the alert record. Each alert record contains detailed information about the alert, including the name of the affected component, the severity level, and the timestamp.
-   An alert's **Affected Entity**, which references the target for an alert, for example, a Kafka Stream or a Kafka Flow Trigger.

You can view the Stream Connect Alerts table by navigating to **Integration Hub** &gt; **Stream Connect** &gt; **Alerts**.

Alerts are available for 30 days. A table cleaner job handles the retention period for the Stream Connect alerts table. Active alerts are deactivated if they don’t reoccur within a specified duration. The duration is configured per alert type in the Stream Connect Alerting properties.

## Alert logs

Log messages for Stream Connect alerts are written to the Stream Connect Log \[sys\_consumer\_log\]. This log has an Alert \[sc\_alert\] field that references the associated Stream Connect Alert record.

Logs are available for 30 days. The log retention period is determined by the table rotation schedule for the Stream Connect Log.

## Notifications

Receive alert notifications via email, SMS, or the ServiceNow® mobile app. Notifications contain detailed alert information, including the alert number, level, and a description.

When an alert is triggered, a notification is also triggered, unless a notification for that same alert was recently triggered. Each alert has a time interval property that specifies the amount of time, in seconds, required between alert detections to have the detections count as two separate alerts. A notification is only triggered if the time since the last notification is greater than that time interval or, in the case of threshold-based alerts, if the severity for the alert has increased since the last detection. This helps ensure that you don't receive multiple rapid notifications for the same alert. The time interval property for each alert can be modified from the Stream Connect Alerting properties UI.

Administrators can configure notification settings based on alert types, user preferences, and alert severity levels. There are three alert severity levels in the Notifications \[sysevent\_email\_action\] table.

-   Stream Connect Alert - INFO
-   Stream Connect Alert - WARNING
-   Stream Connect Alert - CRITICAL

You can opt in to different levels using the standard system notification capabilities on the platform. Administrators can also configure notification debounce settings, including the time interval and criteria for consolidating alerts. For notification details, see [Notifications](https://www.servicenow.com/docs/access?context=notifications&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

Notifications are sent to users who are members of the Stream Connect Alert Notifications group. The Stream Connect Alert Notifications group members inherit the Stream Connect Alert Viewer role so that everyone who receives notifications can use the link in the notification to see the alert record.

## Roles

To view Stream Connect Alerts, you must have the Kafka Admin role or the Stream Connect Alert Viewer role.

-   The Kafka Admin \[kafka\_admin\] role can view Stream Connect alert records and logs, configure Stream Connect Alerting properties, and configure alert notification settings.
-   The Stream Connect Alert Viewer \[stream\_connect\_alert\_viewer\] role has read-only access to Stream Connect alert records and logs.

## ACLs and domain separation

ACLs on the Stream Connect Alerts table enable a user with the Stream Connect Alert Viewer role to view the alerts table and the reports on that table. Users without that role can’t read or report on that table. Only users with the Kafka Admin role can insert and update records on that table. ACLs make the Stream Connect Alerting properties page available only to Kafka Admins.

On a domain-separated instance, the properties that govern alerts can be overridden on a per-domain basis. See [Domain separation application properties](https://www.servicenow.com/docs/access?context=ds-application-properties&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) for details.

The domain used to look up properties is the domain of the topic or consumer. The Stream Connect Alerting properties UI for setting properties sets the global properties, not domain-specific overrides. There's no UI for setting domain-specific overrides. The sys\_domain of the Stream Connect Alerts table should be the same as the domain of the consumer that triggered it, for consumer alerts, or the domain for the sys\_kafka\_topic record for producer alerts. For alerts where a consumer or topic isn't known, the sys\_sc\_alert domain is set to global.

## Plugin

Stream Connect alerting requires the ServiceNow Stream Connect Alerting \[com.glide.hub.stream\_connect.alerting\] plugin. This plugin is automatically activated when the ServiceNow Stream Connect Installer\[com.glide.hub.stream\_connect.installer\] plugin is activated.

-   **[Stream Connect Alerting properties](../reference/sc-alert-properties.md)**  
Specify alert properties and how alerts are managed in Stream Connect.

**Parent Topic:**[Using Stream Connect for Apache Kafka](stream-connect-apache-kafka.md)

