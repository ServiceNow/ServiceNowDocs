---
title: Set up triggers for the Aha! spoke
description: Set up triggers for the Aha! spoke for the required events. The endpoint enables webhooks to connect with your ServiceNow instance.Configure endpoint for webhooks in the Aha! that support the token authentication.Add the endpoint URL that is generated in your ServiceNow instance in the Aha! account to enable webhooks to connect with your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-29"
reading_time_minutes: 1
breadcrumb: [Aha! Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up triggers for the Aha! spoke

Set up triggers for the Aha! spoke for the required events. The endpoint enables webhooks to connect with your ServiceNow instance.

## Before you begin

Role required: admin

## Configure triggers in ServiceNow instance

Configure endpoint for webhooks in the Aha! that support the token authentication.

### Before you begin

Role required: flow\_designer and connection\_admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Toggle and enable the **Inbound** connections.

4.  Locate the **Aha! Spoke** endpoint and click **View Details**.

    ![image.aha-ext-triggers1]

5.  For the **Aha! External Trigger** end point, click **Configure**.

    ![image.aha-ext-triggers2]

6.  Select the user who can trigger the endpoint and click **Activate**.

    ![image.aha-ext-triggers3]

7.  Copy the generated endpoint URL.

    ![image.aha-ext-triggers4]


## Add the endpoint URL in Aha!

Add the endpoint URL that is generated in your ServiceNow instance in the Aha! account to enable webhooks to connect with your ServiceNow instance.

### Before you begin

Role required: admin

### Procedure

1.  Log in to Aha! Workspace as an admin.

2.  Click user profile and navigate to **SETTINGS** &gt; **Workspace**.

3.  Under **Integrations**, click **+** to add an integration.

4.  Under **API**, click **+ Activity webhook**.

5.  On the form, for **Hook URL** paste the generated endpoint URL that was generated after you configured triggers in the ServiceNow instance.

    For more information, see [Configure triggers in ServiceNow instance](aha-ext-triggers.md#).

6.  Select the activities and users as per your requirement.

    For the list supported events, see the [Spoke triggers](../concept/aha-spoke.md#section_wjk_vm2_t3c) section.

7.  Select the **Valid certificate**, **Reduce webhook delay**, and **Enable** check boxes.

8.  Click **Add activity**.


