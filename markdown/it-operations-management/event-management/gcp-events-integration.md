---
title: Integrate Google Cloud Platform \(GCP\) events
description: Integrate Google Cloud Platform \(GCP\) with Event Management by adding a standard webhook in the GCP console.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Integrate Google Cloud Platform \(GCP\) events

Integrate Google Cloud Platform \(GCP\) with Event Management by adding a standard webhook in the GCP console.

## Before you begin

-   Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.
-   The Event Management plugin must be installed on the ServiceNow AI Platform instance.
-   Verify Configuration Items for the hosts managed by GCP exist in ServiceNow. These CIs can be physical or virtual, and can be either manually created or discovered using IP discovery or Cloud discovery.
-   The Event Management Connector plugin supports GCP alert data in JSON 1.2 format only.
-   Role required: evt\_mgmt\_integration

## About this task

Configure the Event Management environment for the collection of events from GCP. In your GCP console, set your ServiceNow AI Platform instance as the rest endpoint using a standard webhook.

Starting from the Xanadu release, the OOTB \(Out-Of-The-Box\) event rules provided with the connector, which you have not previously used \(i.e., neither activated, deactivated, nor modified\), will now have the **Apply additional matching rules** check box set to true. Previously, this check box was disabled. This change allows you to execute more event rules or automation using the same filter conditions for the events.

**Note:** This feature applies only to active event rules.

## Procedure

1.  In the GCP console, add a webhook.

    1.  Navigate to **Monitoring** &gt; **Alerting**, and click **Edit Notification Channels**.

    2.  In the Webhooks section, click **Add New**.

    3.  Select the **Use HTTP Basic Auth** check box, and enter the user name and password of the relevant ServiceNow user.

        **Note:** Ensure that the selected user is assigned the evt\_mgmt\_integration role. To ensure proper authentication, use the least privileged user with the evt\_mgmt\_integration role, rather than a high privileged user.

    4.  Enter the endpoint URL.

        For example, use`https://<instance-name>.service-now.com/api/sn_em_connector/em/inbound_event?source=googlemonitor`.

2.  In the GCP console, create an alerting policy.

    1.  Navigate to **Monitoring** &gt; **Alerting**, and select **Create Policy**.

    2.  Configure policy conditions that initiate alerts when the conditions are violated.

    3.  Select the webhook on which the problem should be notified.

    **Note:** If you need to directly open an incident in the GCP console from the alert, navigate to **Quick Response \(in Alert\)** &gt; **Show Incident in GCP Console**.


## Result

Alerts start flowing from GCP into the Event Management plugin. The plugin extracts information from the original GCP alert message to populate the required event fields and inserts the event into the database. In your ServiceNow AI Platform instance, navigate to**All Events**to see the events.

GCP does not send values such as the severity level in the payload. The default severity is Minor, which can be changed in the**Push Connector Configuration**section of**Push Connectors** &gt; **Google Monitor Push Connector**. The valid values of severity are**1- Critical**,**2- Major**,**3- Minor**,**4- Warning**, and**5- Info**.

**Note:**

To map the GCP hosts to the**cmdb\_ci\_server** record instead of**cmdb\_ci\_vm\_object**, disable the**Google Monitor - General**event rule created for GCP. For further information about event rules, see [Event rules](../concept/create-event-rules.md).

**Parent Topic:**[Integrate with push connectors](configure-listener-transform-script.md)

