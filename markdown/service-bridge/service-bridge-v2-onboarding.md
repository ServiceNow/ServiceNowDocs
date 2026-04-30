---
title: Register a Service Exchange consumer
description: Registering a new consumer in Service Exchange establishes an instance-to-instance integration between a provider and a consumer.
locale: en-US
release: yokohama
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use Service Exchange for providers, Service Exchange for Providers, Service Exchange]
---

# Register a Service Exchange consumer

Registering a new consumer in Service Exchange establishes an instance-to-instance integration between a provider and a consumer.

## Before you begin

-   Role required: admin
-   A provider record must have been created. See [Set up a Service Exchange provider record](service-bridge-v2-new-provider.md).
-   A company or account must exist for the consumer in the provider’s instance, and a user or contact with the sn\_sb\_pro.consumer role must be associated with the company. If this is a production instance, the user must have a valid email address to receive the registration email.
-   Run the **Key Management** &gt; **Health \(Diagnostics\)** to ensure that the Key Management Framework health check has passed. Your administrator must have the sn\_kmf.admin and sn\_kmf.cryptographic\_manager roles to access the health diagnostics. If your administrator does not have access, follow the instructions in [Assign Key Management Framework roles](https://www.servicenow.com/docs/access?context=assign-kmf-roles&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) to grant the required roles.

## About this task

Register a new consumer by creating a registration task for the company and instance you want them to connect with. The company contact will receive an email when this registration task is created in a production instance or any other instance where email sending is enabled. If email sending is not enabled, the provider admin can copy the link from the registration task comments and send it to the consumer admin. The email contains instructions and a link that allows the consumer to complete the registration process.

The following diagram shows the onboarding flow and the exchange of data between the Service Exchange provider and consumer instances.

![Service Exchange Key Exchange Onboarding flow](../image/service-bridge-v2-oauth-flow.jpg)

**Note:** When setting up two instances for demonstration purposes, it is vital to ensure that the consumer contact matches the user who is currently logged into the provider instance when attempting to complete the registration from the consumer instance. In the consumer instance, selecting the **Connect to Provider** option will open an OAUTH page in the provider instance, where the consumer admin must authenticate the OAUTH token. If the contact listed on the registration task does not match the logged-in user, this process will fail.

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Consumer Registrations** and click **New**.

2.  Enter the following details:

    -   Select the Company associated with the consumer instance being registered.
    -   Select the contact details associated with the Company you have selected.

        **Note:** This contact must be an admin user in the consumer instance, otherwise the registration process cannot be completed. On the provider instance, only a Service Exchange Consumer role is required.

    -   Click the **Lock** icon on the URL field and enter the URL of the consumer ServiceNow instance.
3.  Click **Save**.

    An email is generated and sent to the Consumer Contact specified during registration if email sending is enabled. If not, the admin must either copy the link from the work notes and manually send it to the consumer admin. The Consumer Contact must follow the steps listed in the [Registering with a provider](service-bridge-v2-register.md) to complete the registration process on the consumer instance.


