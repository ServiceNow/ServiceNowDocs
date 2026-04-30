---
title: Integrate Grafana events
description: Integrate Grafana with Event Management by adding a standard webhook in the Grafana console.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Integrate Grafana events

Integrate Grafana with Event Management by adding a standard webhook in the Grafana console.

## Before you begin

-   Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.
-   The Event Management plugin must be installed on the ServiceNow AI Platform instance.
-   The CI binding happens through the IP, instances should be discovered as servers to initiate the binding. CIs discovered through cloud or CIs in **cmdb\_ci\_vm\_object** don’t get bounded as Grafana doesn't provide any information for object IDs.
-   Role required: evt\_mgmt\_integration

## About this task

Configure the Event Management environment for the collection of events from Grafana. In your Grafana console, set your ServiceNow AI Platform instance as the rest endpoint using a standard webhook.

**Note:** Perform steps 1 and 2 for Grafana v7.4.3. For Grafana v9.3.2. skip to step 3.

## Procedure

1.  **Grafana v7.4.3**
2.  In the Grafana console, create a notification channel.

    1.  Navigate to **Alerting** &gt; **Notification Channels**.

    2.  Click **New Channel** and select the type as **Webhook**.

    3.  Enter a URL.

        For example, use `https://<instance-name>.service-now.com/api/sn_em_connector/em/inbound_event?source=grafana`.

    4.  Under the **Optional WebHook** settings, select the HTTP Method, **POST**, and enter the user name and password of the relevant ServiceNow user.

        **Note:** Ensure that the selected user is assigned the evt\_mgmt\_integration role. To ensure proper authentication, use the least privileged user with the evt\_mgmt\_integration role, rather than a high privileged user.

    5.  Click **Test** to verify the connection.

3.  In the Grafana console, create alerting rules.

    1.  Click **Edit** on the required panel and then **Create Alert**.

    2.  In the **Alert** tab, add the following tags:

        |Tags|Description|
        |----|-----------|
        |Severity|\(This tag is optional and has to be lower cased.\) Severity with which the alert has to be created.|
        |Count|\(This tag is required, otherwise the alerts don’t close automatically in ServiceNow.\) The number of devices, hosts, or servers monitored by this alert rule.|

    3.  Add the notification channel under **Notifications** in the alert rule.

    4.  Click **Save**.

    5.  Navigate to **Alerting** &gt; **Alert Rules** to access the created rule.

4.  **Grafana v9.3.2.**
5.  In the Grafana console, create a contact point.

    1.  Navigate to **Alerting** &gt; **Contact Points**.

    2.  Click **New Contact Point**, enter a name, and select the type as **Webhook**.

    3.  Enter a URL.

        For example, use `https://<instance-name>.service-now.com/api/sn_em_connector/em/inbound_event?source=grafana`.

    4.  Under the **Optional WebHook** settings, select the HTTP Method, **POST**, and enter the user name and password of the relevant ServiceNow user.

        **Note:** Ensure that the selected user is assigned the evt\_mgmt\_integration role. To ensure proper authentication, use the least privileged user with the evt\_mgmt\_integration role, rather than a high privileged user.

    5.  Click **Save** and **Test** to verify the connection.

6.  In the Grafana console, create a notification policy.

    1.  Navigate to **Alerting** &gt; **Notification Policies**.

    2.  Select **New Policy**, add matchers.

        Matchers are labels that direct alert rules to the contact point.

    3.  Select your contact point.

    4.  Select **Save Policy**.

7.  In the Grafana console, create alert rules.

    1.  Navigate to **Alerting** &gt; **Alert Rule**.

    2.  Select **New Rule**.

    3.  Set the Query and Alert Condition.

    4.  Set the data source, metrics, and the necessary filters.

    5.  Set the alert evaluation behavior.

    6.  Enter the rule name.

    7.  In the summary and annotations section, add a summary or a description.

    8.  From the scroll down, select **+Add New**.

    9.  Enter the node, resource, and metric information.

        This information is required for the node, resource, and metric\_name fields for the event.

        **Note:** Use the value string to pass these values. For example, a node can be \{\{ $values.C0.Labels.instance \}\}.

    10. Under custom labels, provide the required labels to direct your notifications to the appropriate contact point.

        **Note:** You can also pass the severity under custom labels. The same is used for events. The available severity options are: critical, major, minor, warning.

    11. Click **Save**.


## Result

Alerts start flowing from Grafana into the Event Management plugin. The plugin extracts information from the original Grafana alert message to populate the required event fields and inserts the event into the database. In your ServiceNow AI Platform instance, navigate to **All Events** to see the events.

**Note:**

-   For Grafana v7.4.3, you may see extra clear events coming into ServiceNow which aren’t bound to an alert. Ignore them as they’re created to overcome the issue of Grafana not sending information in the clear notification.
-   A severity parameter is added which is used only for Grafana 8 and above. The provided value is used as a severity for an event if the severity isn’t passed in custom labels.

-   **[Integrate Grafana with REST API key token](integrate-grafana-api-key.md)**  
Integrate using an API key to establish secure communication and automate data exchange via REST API. This simplifies integration, enabling seamless access to services and enhancing operational efficiency.

**Parent Topic:**[Integrate with push connectors](configure-listener-transform-script.md)

