---
title: Set up triggers for the GitHub spoke
description: Set up the trigger to generate the secret and callback URL on your ServiceNow instance.Activate the trigger definition to generate the secret and callback URL on your ServiceNow instance for the GitHub spoke.Set the secret and callback URL to enable GitHub to securely send webhooks to your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-10-14"
reading_time_minutes: 2
breadcrumb: [GitHub Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up triggers for the GitHub spoke

Set up the trigger to generate the secret and callback URL on your ServiceNow instance.

Demonstrates setting up triggers for the GitHub spoke. 

## Before you begin

-   Request an Integration Hub subscription.
-   Activate and set up the GitHub spoke.
-   Role required: admin.

## Activate the trigger definition on ServiceNow instance for the GitHub spoke

Activate the trigger definition to generate the secret and callback URL on your ServiceNow instance for the GitHub spoke.

### Before you begin

Role required: flow\_designer and connection\_admin.

### About this task

GitHub uses the secret and callback URL to securely send the payload to the ServiceNow instance. The ServiceNow instance verifies the secret that GitHub sends and accepts the payload.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select the **Integrations** tab.

3.  Toggle and enable the **Inbound** tab.

4.  Locate the GitHub Spoke card and select **View Details**.

5.  Select **Configure**.

6.  In the User field, select the user name on whose behalf the inbound session or flow is triggered.

7.  Select **Generate secret** to generate the secret.

    The secret is used to sign the payload of the webhook. You must configure the secret on GitHub.

    The secret is generated on the Secret field.

8.  Select **Activate**.

    The callback URL is generated in the URL field.

    ![Callback URL generated.](../image/github-callback-url.png)

9.  Copy the values of **Secret** and **URL** for later use.

10. Close the window.


### What to do next

[Configure secret and callback URL on GitHub](set-up-triggers-github-spoke.md#)

## Configure secret and callback URL on GitHub

Set the secret and callback URL to enable GitHub to securely send webhooks to your ServiceNow instance.

### Before you begin

Role required: Admin

### Procedure

1.  Log in to the GitHub account.

2.  Navigate to the required repository.

3.  Select **Settings**.

4.  On the left panel, select, **Webhooks**.

5.  Select **Add Webhook**.

6.  Fill the form.

<table id="table_glq_5vm_1cc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Payload URL \*

</td><td>

Option to provide GitHub the payload URL that GitHub uses to send the payload via the webhook.Enter the URL that you have generated while activating the trigger. See [Activate the trigger definition on ServiceNow instance for the GitHub spoke](set-up-triggers-github-spoke.md#).

</td></tr><tr><td>

Content type \*

</td><td>

Option to select the payload content format.Select **application/json**.

</td></tr><tr><td>

Secret

</td><td>

Option to provide the secret that the ServiceNow verifies when it receives the webhook from GitHub.Enter the secret that you have generated while activating the trigger. See [Activate the trigger definition on ServiceNow instance for the GitHub spoke](set-up-triggers-github-spoke.md#).

</td></tr><tr><td>

Which events would you like to trigger this webhook?

</td><td>

Option to specify the event that triggers the webhook. Choose from the following options.-   Just the push event: Triggers the webhook when there’s a push event on GitHub.
-   Send me everything: Triggers webhooks whenever an event occurs.
-   Let me select individual events: Triggers the webhook when you specify an event.


</td></tr></tbody>
</table>7.  Select **Add Webhook**.


