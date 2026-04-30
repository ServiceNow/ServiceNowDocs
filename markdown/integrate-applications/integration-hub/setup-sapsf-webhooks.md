---
title: Set up webhook for the SuccessFactors spoke
description: Configure a webhook to subscribe to your SuccessFactors account with a ServiceNow callback URL.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SuccessFactors Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up webhook for the SuccessFactors spoke

Configure a webhook to subscribe to your SuccessFactors account with a ServiceNow callback URL.

## Before you begin

-   [Set up the SuccessFactors spoke v4.x.x](setup-successfactors.md#)
-   Role required: admin

## Procedure

1.  Configure the default decision table.

    1.  Navigate to **System Definition** &gt; **Decision Tables**.

    2.  Search for the record, `Successfactors Webhook` and open it.

    3.  In the **Decision Inputs** tab, open the **Webhook Event** record.

    4.  In the **Choices** tab, create record for the event for which you want to subscribe. For example, enter `Employee Time Off` in **Label** and **Name** to subscribe to the Employee Time Off events.

    5.  Navigate back to the `Successfactors Webhook` record.

    6.  In the **Decisions** tab, open the **Default Decision** record.

    7.  Select the required webhook event in **Condition** and select the subflow in **Answer**.

        When the specified webhook event occurs, the associated subflow is triggered.

        **Note:** You can customise the default subflow or create a subflow as per your requirement.

2.  Create a webhook registry.

    1.  Navigate to **SuccessFactors Spoke** &gt; **Webhook Registry**.

    2.  Click **New**.

    3.  On the form, enter `SuccessFactors Webhook Authentication` for **Name** and provide **Description**.

        **Note:** The **Name** of the webhook registry must be `SuccessFactors Webhook Authentication`.

    4.  Click **Generate Username and Password**.

        Username and Password are generated and the values are displayed.

    5.  Copy and record the values of the generated values for later use.

3.  Copy and record the value of **Resource path**.

    1.  Navigate to **System Web Services** &gt; **Scripted REST APIs**.

    2.  Search for the record, `SuccessfactorsWebhook` and open it.

    3.  In the **Resources** tab, click the **processWebhook** record.

    4.  Copy and record the value provided in **Resource path**.

4.  Configure events in your SuccessFactors instance.

    1.  Log in to your SuccessFactors instance and navigate to **Admin Center** &gt; **Event Notification Subscription**.

    2.  In the **External Event** tab, provide these values:

        |Field|Description|
        |-----|-----------|
        |Endpoint URL|ServiceNow instance endpoint URL in this format: `https://<servicenow-instance>.com/<resource-path>`|
        |Authentication|Select **Basic**.|
        |User|User name generated when the webhook registry is created.|
        |Password|Password when the webhook registry is created.|

    3.  Configure the subscriber in the **Subscriber** tab as per your requirement.

    4.  Select the required **Service Event Bus Topic** in the **SEB External Event** tab as per your requirement and select the events for which you want to receive notifications. For example, `Employee Time Off`.


