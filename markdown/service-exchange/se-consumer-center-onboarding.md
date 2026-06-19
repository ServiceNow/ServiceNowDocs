---
title: Consumer registration from the Consumer Center
description: Complete the registration process from the Service Exchange Connection Wizard to establish a secure connection to your provider instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-exchange/se-consumer-center-onboarding.html
release: australia
product: Service Exchange
classification: service-exchange
topic_type: task
last_updated: "2026-06-03"
reading_time_minutes: 1
breadcrumb: [Configure for consumers, Service Exchange for Consumers, Service Exchange]
---

# Consumer registration from the Consumer Center

Complete the registration process from the Service Exchange Connection Wizard to establish a secure connection to your provider instance.

## Before you begin

-   Role required: admin
-   The consumer instance must be running Service Exchange version 2.3.18 or later.
-   The provider must have created a connection request and shared the registration URL with you. See [Register a consumer from the Provider Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/se-provider-center-onboarding.md).

## About this task

The provider initiates registration and shares a registration URL with you either by email or directly.

**Note:** The provider should have requested the contact details of an admin to set as the main point of contact on their registration record. This designated contact person will receive an email either from the provider's instance or directly from the provider's admin, containing a registration link.

When you open the URL, the Service Exchange Connection Wizard opens and guides you through the pre-onboarding checks and registration steps.

The registration process runs system checks to verify that your instance is ready before starting the connection. The process may take a few minutes to complete.

## Procedure

1.  Open the registration URL sent to you by the provider.

    The **Create your connection** page opens.

2.  In the **Select Provider** field, select the provider company and then select **Get Started**.

    The system runs pre-onboarding checks and the page state is set to **Validated** when all checks pass.

    **Note:** If any check fails, the system displays a validation error and the **Start Registration** button does not appear. Resolve the issues indicated and select **Get Started** again.

3.  Select **Start Registration**.

    The registration process starts. The wizard displays the progress of each step as it completes. The process may take a few minutes.

4.  Select **Configure settings**.

    Use the **Settings** tab to configure the connection settings, including **Remote record producer settings**, **Remote task definitions**, and **Auto-activation** options.

5.  Save your settings by selecting **Done**.


## Result

After the registration is successful, you see a success message and the state of the connection changes to Onboarded. ALONG with the state, you also see the provider details, connection status, and the date the connection was established.

## What to do next

[Execute a scan suite as a consumer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/se-con-execute-scan-check.md).

