---
title: Register a consumer from the Provider Center
description: Register a consumer instance from the Connections tab in the Provider Center to establish a Service Exchange connection between your instance and the consumer instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-exchange/se-provider-center-onboarding.html
release: australia
product: Service Exchange
classification: service-exchange
topic_type: task
last_updated: "2026-06-03"
reading_time_minutes: 1
breadcrumb: [Use for providers, Service Exchange for Providers, Service Exchange]
---

# Register a consumer from the Provider Center

Register a consumer instance from the **Connections** tab in the Provider Center to establish a Service Exchange connection between your instance and the consumer instance.

## Before you begin

-   Role required: admin
-   A provider record must have been created. See [Set up a Service Exchange provider record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-new-provider.md).
-   A company record must exist for the consumer in the provider instance, and a contact must be associated with that company.
-   The consumer instance must be running Service Exchange version 2.3.18 or later.

## About this task

As a provider admin, you initiate the registration process by creating a connection request in the Provider Center. This generates a unique registration URL that the consumer uses to complete their registration.

If email notifications are enabled, the system sends the registration URL to the consumer contact. Otherwise, you share the URL manually after the connection card is created.

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Administration** &gt; **Provider Center**.

2.  Select the **Connections** tab.

3.  Select **New connection**.

4.  In the **Create a new connection** form, enter the following details:

    -   **Company**: Select the company associated with the consumer instance.
    -   **Contact**: Select the contact associated with the company.

        **Note:** The contact must be an admin user in the consumer instance. Registration cannot be completed by any other user.

    -   **URL**: Enter the URL of the consumer instance.
5.  Select **Create connection**.

    A connection card is created for the consumer and a registration URL is generated.

6.  If email notifications are turned off, copy the registration URL from the **Connection Card** and share the URL with the consumer admin.

    The consumer admin must use this URL to complete the registration process.


## Result

A connection request is created and the consumer receives the registration URL. After the consumer completes registration, the connection card state is set to **Onboarded**. Select **View details** on the connection card to review the registration details and configure connection settings.

## What to do next

[Consumer registration from the Consumer Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/se-consumer-center-onboarding.md).

**Parent Topic:**[Using Service Exchange for providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-administer.md)

