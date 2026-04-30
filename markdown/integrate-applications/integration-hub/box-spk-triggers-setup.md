---
title: Set up triggers for the Box spoke
description: Set up the trigger to generate the secret and callback URL on your ServiceNow instance.Set the secret and callback URL to enable Box to securely send webhooks to your ServiceNow instance.Activate the trigger definition to generate the secret and callback URL on your ServiceNow instance for the Box spoke.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-12-01"
reading_time_minutes: 2
breadcrumb: [Box Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up triggers for the Box spoke

Set up the trigger to generate the secret and callback URL on your ServiceNow instance.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate and set up the Box spoke.
-   Role required: admin.

## Configure secret and callback URL in Box

Set the secret and callback URL to enable Box to securely send webhooks to your ServiceNow instance.

### Before you begin

Role required: admin

### Procedure

1.  Log in to the Box account.

2.  Create a custom application.

    1.  Click **Dev Console**.

    2.  Under **My Platform Apps**, click **Create Platform App**.

    3.  Click **Custom App**.

    4.  On the Create a Custom App form, provide app details.

        Provide a name for **App Name** and select **Custom Portal** for **Purpose**.

    5.  Click **Next**.

    6.  Select **Server Authentication \(with JWT\)** for **Authentication Method** and click **Create App**.

        The custom application is created and the **Configuration** tab is displayed.

    7.  Copy the value of **Client ID** from the **Configuration** tab.

3.  Authorize the custom application.

    1.  Navigate to the **Admin console** from the Box account homepage.

    2.  Click **Integrations**.

    3.  Under the **Platform Apps Manager**, click **Server Authentication App**.

    4.  Click **Add Platform App**, paste the value of **Client ID**, and click **Next**.

        The custom application details are displayed.

    5.  Click **Authorize**.

4.  Provide the required application scopes to the custom application.

    1.  In the **Configuration** tab, for **Application Scopes** select the **Write all files and folders stored in Box**, **Manage signature requests**, **Manage webhooks**, and **Enable integrations** options.

    2.  Click **Save Changes**.

5.  Generate primary key for the custom application.

    1.  In the **Webhooks** tab, click **Manage Signature Keys**.

    2.  Under **Primary Key**, click **Generate Key**.

    3.  Click **Copy** to copy the value of **Primary Key** and record it for later use.

6.  Create a webhook for the custom application and add ServiceNow endpoint URL.

    1.  In the **Webhooks** tab, click **Create Webhook** and select **V2**.

    2.  For **URL Address** under **Configuration**, enter ServiceNow endpoint URL in this format: `https://<ServiceNow-Instance-Name>.service-now.com/api/sn_box_spoke/box_external_trigger?X-SkipCookieAuthentication=true`.

    3.  For **Content Type**, select either file or folder as per your requirement.

        Flow events differ based on the selected **Content Type**.

    4.  Select the required triggers that are associated with the selected **Content Type**.

    5.  Click **Create Webhook**.


## Activate the trigger definition on ServiceNow instance for the Box spoke

Activate the trigger definition to generate the secret and callback URL on your ServiceNow instance for the Box spoke.

### Before you begin

Role required: flow\_designer and connection\_admin.

### About this task

Box uses the secret and callback URL to securely send the payload to the ServiceNow instance. The ServiceNow instance verifies the secret that Box sends and accepts the payload.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select the **Integrations** tab.

3.  Toggle and enable the **Inbound** tab.

4.  Locate the **Box Spoke** card and select **View Details**.

5.  Select **Configure**.

6.  In the **User** field, select the user name on whose behalf the inbound session or flow is triggered.

7.  In the **Secret** field, paste the value of **Primary Key** that was generated in the Box account.

    The secret is used to sign the payload of the webhook.

8.  Select **Activate**.

    The callback URL is generated in the URL field.

    ![Configure external trigger for the Box spoke.](../image/box-spk-ext-trigger.jpg)

9.  Close the window.


