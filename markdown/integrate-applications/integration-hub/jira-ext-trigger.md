---
title: Set up triggers for the Jira spoke
description: Set up triggers for the Jira spoke for the required events. The endpoint enables webhooks to connect with your ServiceNow instance.Configure endpoint for webhooks in the Jira that support the token authentication.Add the endpoint URL that is generated in your ServiceNow instance in the Jira Atlassian account to enable webhooks to connect with your ServiceNow instance.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-09-04"
reading_time_minutes: 1
breadcrumb: [Jira Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up triggers for the Jira spoke

Set up triggers for the Jira spoke for the required events. The endpoint enables webhooks to connect with your ServiceNow instance.

Demonstrates setting up triggers for the Jira spoke. 

## Before you begin

Role required: admin

## Configure triggers in ServiceNow instance

Configure endpoint for webhooks in the Jira that support the token authentication.

### Before you begin

Role required: flow\_designer and connection\_admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Toggle and enable the **Inbound** connections.

4.  Locate the **Jira Spoke** endpoint and click **View Details**.

    ![Locate the Jira Spoke endpoint.](../image/jira-spk-endpoint.png)

5.  For the **Jira External Trigger** end point, click **Configure**.

    ![Configure the endpoint.](../image/jira-spk-endpoint-conf.png)

6.  Select the user who can trigger the endpoint and click **Activate**.

    ![Activate the endpoint.](../image/jira-spk-endpoint-activate.png)

7.  Copy the generated endpoint URL.

    ![Copy the generated endpoint URL.](../image/jira-spk-endpoint-generated.png)


## Add the endpoint URL in Jira

Add the endpoint URL that is generated in your ServiceNow instance in the Jira Atlassian account to enable webhooks to connect with your ServiceNow instance.

### Before you begin

Role required: admin

### Procedure

1.  Log in to your Jira Atlassian account.

2.  Navigate to **JIRA SETTINGS** &gt; **System**.

    ![Jira system settings.](../image/jira-spk-webhook.png)

3.  Under **Advanced**, click **WebHooks**.

4.  Click **+Create a WebHook**.

5.  On the form, fill in the values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the webhook.|
    |URL|Paste the generated endpoint URL that was generated after you [configured triggers in the ServiceNow instance](jira-ext-trigger.md#).|

    ![Add the endpoint URL.](../image/jira-spk-add-endpt-url.png)

6.  Select the supported events as per your requirement.

    For the list of the supported events, see the [Spoke triggers](../concept/jira-spoke-v3-0-2.md#section_cpg_rpm_ccc) section.

    ![Select the required events.](../image/jira-spk-events.png)

7.  Click **Create**.


