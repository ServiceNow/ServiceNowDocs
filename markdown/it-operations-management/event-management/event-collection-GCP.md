---
title: Event collection from Google Cloud Platform \(GCP\)
description: The MID WebService Event Collector enables you to collect JSON formatted event messages sent from Google Cloud Platform \(GCP\).
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Event collection from Google Cloud Platform \(GCP\)

The MID WebService Event Collector enables you to collect JSON formatted event messages sent from Google Cloud Platform \(GCP\).

## Before you begin

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

Ensure that you:

-   Deploy and start the MID Server. See MID Server configuration .
-   Configure and start the MID Web Server. See [Configure the MID Web Server extension](configure-mid-web-server-extension.md).
-   Configure and start the MID WebService Event Collector. See [Configure the MID WebService Event Collector Context](configure-em-context-extension.md).

Role required: evt\_mgmt\_admin

## About this task

JSON formatted event messages are sent from Google Cloud Platform. The MID Server transforms the collected event messages by parsing them using the TransformEvents\_MidGoogleMonitor script include, located here: **Event Management** &gt; **Integrations** &gt; **PushConnectors**. In the Push Connectors page, click **Google Monitor Mid Push Connector**.

The default format of the URL to push event messages from the GCP to the MID Server is `http://<MID_Server_IP>:<MID_Web_Server_Port>/api/mid/em/inbound_event?Transform=TransformEvents_MidGoogleMonitor`.

|Variable|Description|
|--------|-----------|
|MID\_Server\_IP|IP address of the MID Web Server Extension.|
|MID\_Web\_Server\_Port|Listening port of the MID Web Server Extension.|
|MID\_Web\_Server\_User|Username for the MID Web Server Extension.|
|MID\_Web\_Server\_Password|Password of the user of the MID Web Server.|

The following procedure describes the collection of JSON formatted event messages using basic authentication.

## Procedure

1.  In the Google Cloud Platform \(GCP\) console, make sure the MID Server IP is accessible from the GCP console and MID rest point is accessible from GCP or install the MID Server on a GCP VM and provide the GCP VM external IP address in the URL.

    In the GCP console, create a firewall rule.

    1.  Navigate to **VPC Network** &gt; **Firewall** &gt; **Create Firewall**.

    2.  Set the direction to **ingress** to allow the mid\_web\_server\_port to connect.

    3.  Add the GCP VM that the MID Server is installed on to the **Applicable to instances** list.

2.  In the GCP console, add a webhook.

    1.  Navigate to **Monitoring** &gt; **Alerting** and click **Edit Notification Channels**.

    2.  In the Webhooks section, click **Add New**.

    3.  Select the **Use HTTP Basic Auth** check box, and enter the username and password of the MID Webserver User.

        **Note:** Ensure that the selected user is assigned the evt\_mgmt\_integration role. To ensure proper authentication, use the least privileged user with the evt\_mgmt\_integration role, rather than a high privileged user.

    4.  Enter the endpoint URL.

        For example, use `http://<MID_Server_IP>:<MID_Web_Server_Port>/api/mid/em/inbound_event?Transform=TransformEvents_MidGoogleMonitor`

3.  In the GCP console, create an alerting policy.

    1.  Navigate to **Monitoring** &gt; **Alerting** and click **Create Policy**.

    2.  Configure the policy conditions that initiate alerts when the conditions are violated.

    3.  Select the webhook notification channel on which the problem should be notified.

    4.  Select the **Notify on incident closure** check box to send the closure events to the MID Server and save the alert policy.

        **Note:** If you need to directly open an incident in the GCP Console from the alert, navigate to **Quick Response \(in Alert\)** &gt; **Show Incident in GCP Console**. For more information about creating an alert policy, see [Managing alerting policies](https://cloud.google.com/monitoring/alerts/using-alerting-ui) on the Google Cloud documentation site.


## Result

GCP does not send values such as the severity level into the payload. The default severity is Minor, which can be changed in the **Push Connector Configuration** section of **Push Connectors** &gt; **Google Monitor MID Push Connector**. The valid values of severity are **1- Critical**, **2- Major**, **3- Minor**, **4- Warning**, and **5- Info**.

**Parent Topic:**[Integrate with push connectors](configure-listener-transform-script.md)

