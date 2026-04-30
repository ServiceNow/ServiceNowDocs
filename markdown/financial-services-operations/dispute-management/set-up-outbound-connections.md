---
title: Set up connections to the tokenizer service
description: Follow these steps to set up connectivity between your ServiceNow instance, the FSO tokenizer service, and the Third-Party System.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Set up connections to the tokenizer service

Follow these steps to set up connectivity between your ServiceNow instance, the FSO tokenizer service, and the Third-Party System.

## Before you begin

Complete the onboarding procedure for our tokenizer service. For more information, see [Initial steps to setup schema and connections for Card data security \(KB2238661\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2238661).

Role required: admin

## About this task

To establish communication between your ServiceNow instance, our tokenizer service, and the Third-Party System, you need to set up the connections and service accounts in our tokenizer service administration site.

The onboarding process includes a script that sets up connections and routes for Visa and Mastercard as part of the application. For more information, see [Initial steps to setup schema and connections for Card data security \(KB2238661\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2238661).

For more detailed information on the procedures described in this topic, refer to the [tokenizer service documentation](https://docs.skyflow.com/).

## Procedure

1.  Navigate to our tokenizer service URL and login to your account with the credentials provided in the onboarding procedure.

2.  Select **Connections** in the side navigation menu.

    You will see connections for Visa and Mastercard that were set up as part of the onboarding procedure.

3.  Select **Edit** for the connection you want to set up.

4.  Enter the outbound URL for the third-party service in **Outbound Base URL**.

5.  Select **Service Account** in the connection navigation menu.

6.  Select **Add service account**.

    Refer to the [tokenizer service documentation](https://docs.skyflow.com/) for steps on setting up a service account.

    During service account setup, you must define your authentication type \(JWT or API key\) and at least one role assignment.

7.  Select **Advanced Configuration** in the connection navigation menu.

8.  Fill in the advanced configuration fields.

    |Field|Value|
    |-----|-----|
    |**Outbound Base URL**|The URL of the Third-Party System.|
    |**Outbound Authentication**|Select the authentication method and enter the required information as provided by the third-party.|


## Result

An endpoint is created for the Third-Party System.

If you selected JWT authentication, a private key file is downloaded. Store this key file in a secure and accessible place.

![Image showing the modal window in our tokenizer service informing the user that private key file(s) will be downloaded and to store these in a safe place.](../image/jwt-key-credentials.png)

If you selected API key authentication, you will be presented with a prompt containing your API key. Save the API key in a secure and accessible place.

![Image showing the modal window in our tokenizer service prompting the user to save the API key.](../image/tokenizer-service-save-api-key.png)

## What to do next

Use this endpoint to complete connectivity setup for Card Data Security in your ServiceNow instance.

Use the provided authentication key in your ServiceNow instance when creating a credential alias. See [Set up tokenized HTTP connection and credentials](create-a-new-tokenizer-route.md).

You may set up additional routes in the connection. For more information, refer to the [tokenizer service documentation](https://docs.skyflow.com/).

