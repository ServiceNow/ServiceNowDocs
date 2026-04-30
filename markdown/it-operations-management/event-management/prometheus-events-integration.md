---
title: Integrate Prometheus events
description: Integrate Prometheus with Event Management by adding a standard webhook in Prometheus's Alert Manager.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Integrate Prometheus events

Integrate Prometheus with Event Management by adding a standard webhook in Prometheus's Alert Manager.

## Before you begin

-   Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.
-   Verify Configuration Items for the hosts managed by Prometheus exist in ServiceNow. These CIs can be physical or virtual, and can be either manually created or discovered using IP discovery or Cloud discovery.
-   Role required: evt\_mgmt\_integration

## About this task

Configure the Event Management environment for the collection of events from Prometheus.

Starting from the Xanadu release, the OOTB \(Out-Of-The-Box\) event rules provided with the connector, which you have not previously used \(i.e., neither activated, deactivated, nor modified\), will now have the **Apply additional matching rules** check box set to true. Previously, this check box was disabled. This change allows you to execute more event rules or automation using the same filter conditions for the events.

**Note:** This feature applies only to active event rules.

## Procedure

1.  In the Prometheus instance, add a webhook.

    1.  Navigate to Alertmanager.yml and add a webhook entry under the recievers.
    2.  Enter the endpoint uRL. For example, use `https://<instance-name>/service-now.com/api/sn_em_connector/em/inbound_event?source=prometheus`.
    3.  Type `basic_auth` underneath **http\_config**.
    4.  Add a username and password under **basic\_auth**, then add the created webhook name in the receiver under **route**.
2.  In the Prometheus instance, create an alert rule.

    1.  Create a file for the alert rule and add its' path inside prometheus.yml under **rules\_files**.
    2.  Create the alert rule as per the prometheus format using PromQL.
    3.  Restart AlertManager and Prometheus to reflect the changes.

## Result

Alerts start flowing from Prometheus into the Event Management plugin. The plugin extracts information from the original Prometheus alert message to populate the required event fields and inserts the event into the database. In your ServiceNow AI Platform instance, navigate to **All Events** to see the events.

If severity isn't received in the payload, the default severity is Major, which can be changed in the **Push Connector Configuration** section of **Push Connectors** &gt; **Prometheus Push Connector**. The valid values of severity are **1- Critical**, **2- Major**, **3- Minor**, **4- Warning**, and **5- Info**.

**Note:**

To map hosts to the **cmdb\_ci\_vm\_object** record instead of **cmdb\_ci\_hardware**, enable the **Prometheus VM Binding** event rule created for Prometheus. For further information about event rules, see [Event rules](../concept/create-event-rules.md).

**Parent Topic:**[Integrate with push connectors](configure-listener-transform-script.md)

