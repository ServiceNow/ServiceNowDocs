---
title: Register a Service Exchange consumer
description: Registering a new consumer in Service Exchange establishes an instance-to-instance integration between a provider and a consumer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/service-exchange/service-bridge-v2-onboarding.html
release: zurich
product: Service Exchange
classification: service-exchange
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use for providers, Service Exchange for Providers, Service Exchange]
---

# Register a Service Exchange consumer

Registering a new consumer in Service Exchange establishes an instance-to-instance integration between a provider and a consumer.

## Before you begin

-   Role required: admin
-   A provider record must have been created. See [Set up a Service Exchange provider record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/service-exchange/service-bridge-v2-new-provider.md).
-   A company or account must exist for the consumer in the provider’s instance, and a user or contact with the sn\_sb\_pro.consumer role must be associated with the company. If this is a production instance, the user must have a valid email address to receive the registration email.

## About this task

Register a new consumer by creating a registration task for the company and instance you want them to connect with. The company contact will receive an email when this registration task is created in a production instance or any other instance where email sending is enabled. If email sending is not enabled, the provider admin can copy the link from the registration task comments and send it to the consumer admin. The email contains instructions and a link that allows the consumer to complete the registration process.

**Note:** When setting up two instances for demonstration purposes, it is vital to ensure that the consumer contact matches the user who is currently logged into the provider instance when attempting to complete the registration from the consumer instance. In the consumer instance, selecting the **Connect to Provider** option will open an OAUTH page in the provider instance, where the consumer admin must authenticate the OAUTH token. If the contact listed on the registration task does not match the logged-in user, this process will fail.

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Consumer Registrations** and click **New**.

2.  Enter the following details:

    -   Select the Company associated with the consumer instance being registered.
    -   Select the contact details associated with the Company you have selected.

        **Note:** This contact must be an admin user in the consumer instance, otherwise the registration process cannot be completed. On the provider instance, only a Service Exchange Consumer role is required.

    -   Click the **Lock** icon on the URL field and enter the URL of the consumer ServiceNow instance.
3.  Click **Save**.

    An email is generated and sent to the Consumer Contact specified during registration if email sending is enabled. If not, the admin must either copy the link from the work notes and manually send it to the consumer admin. The Consumer Contact must follow the steps listed in the [Connect to a provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/service-exchange/service-bridge-v2-register.md) to complete the registration process on the consumer instance.


