---
title: Set up triggers for the Vonage spoke
description: Set up triggers for the Vonage spoke for the required events. The endpoint enables webhooks to connect with your ServiceNow instance.Configure endpoint for webhooks in the Vonage that support the token authentication.Add the endpoint URL that is generated in your ServiceNow instance in the Vonage API Dashboard to enable webhooks to connect with your ServiceNow instance.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Vonage Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up triggers for the Vonage spoke

Set up triggers for the Vonage spoke for the required events. The endpoint enables webhooks to connect with your ServiceNow instance.

## Configure triggers in ServiceNow instance

Configure endpoint for webhooks in the Vonage that support the token authentication.

### Before you begin

Role required: flow\_designer and connection\_admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Toggle and enable the **Inbound** connections.

4.  Locate the **Vonage Spoke** endpoint and click **View Details**.

5.  For the **Vonage External Trigger** end point, click **Configure**.

6.  Select the user who can trigger the endpoint and click **Activate**.

    ![During the Vonage webhook configuration, select user profile, activate the endpoint, then copy the generated URL and paste it in your Vonage account.](../image/vonage-spk-endpoint-activate.png)

7.  Copy the generated endpoint URL.


## Add the endpoint URL in Vonage

Add the endpoint URL that is generated in your ServiceNow instance in the Vonage API Dashboard to enable webhooks to connect with your ServiceNow instance.

### Before you begin

Role required: admin

### Procedure

1.  Log in to your Vonage API Dashboard.

2.  Navigate to **CONTROL** &gt; **API Settings**.

    ![Configuring webhook URLs in Vonage](../image/vonage-spoke-webhooks.png)

3.  Under **Default SMS Setting**, locate the webhook URL fields.

4.  In the webhook URL field, paste the generated endpoint URL.

    |Field|Description|
    |-----|-----------|
    |Delivery receipts \(DLR\) webhooks|Endpoint URL that was generated after you [Configure triggers in ServiceNow instance](set-up-triggers-vonage.md#) to receive delivery status updates.|
    |Inbound SMS webhooksvo|Endpoint URL that was generated after you [Configure triggers in ServiceNow instance](set-up-triggers-vonage.md#) to receive inbound messages.|

5.  Click **Save** to save the changes.

6.  To configure webhooks for call management, navigate to **BUILD** &gt; **Applications** &gt; **Create a new application**.

    ![Creating an application in Vonage](../image/vonage-spoke-applications.png)

7.  While creating an application, toggle the Voice option under Capabilities.

8.  Copy the URL generated in your ServiceNow instance and paste it as the Answer URL and Event URL and click **Save**.

    ![Configuring voice capabilities in Vonage](../image/vonage-spoke-capabilities.png)


