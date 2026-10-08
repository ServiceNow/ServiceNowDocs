---
title: Consumer registration from the Consumer Center
description: Complete the registration process from the Service Exchange Connection Wizard to establish a secure connection to your provider instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-exchange/se-consumer-center-onboarding.html
release: brazil
product: Service Exchange
classification: service-exchange
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configure for consumers, Service Exchange for Consumers, Service Exchange]
---

# Consumer registration from the Consumer Center

Complete the registration process from the Service Exchange Connection Wizard to establish a secure connection to your provider instance.

## Before you begin

-   Role required: admin
-   The consumer instance must be running Service Exchange version 2.3.18 or later.
-   The provider must have created a connection request and shared the registration URL with you. See [Register a consumer from the Provider Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-provider-center-onboarding.md).

## About this task

The provider initiates registration and shares a registration URL with you either by email or directly.

**Note:** The provider should have requested the contact details of an admin to set as the main point of contact on their registration record. This designated contact person will receive an email either from the provider's instance or directly from the provider's admin, containing a registration link.

When you open the URL, the Service Exchange Connection Wizard opens and guides you through the pre-onboarding checks and registration steps.

The registration process runs system checks to verify that your instance is ready before starting the connection. The process may take a few minutes to complete.

If your instance is running an older version of Service Exchange, clicking the link in the email redirects you to the older registration experience instead of this wizard.

## Procedure

1.  Open the registration URL sent to you by the provider.

    The **Create your connection** page opens.

2.  In the **Select Provider** field, select the provider company and then select **Get Started**.

    The system automatically runs the pre-onboarding scan suite and displays the provider connection details. The page shows the message "Running pre-onboarding checks to ensure you are ready." When checks complete:

    -   If all checks pass, the message "System checks passed. Your system is healthy and ready for registration." appears and **Start Registration** becomes active.
    -   If any check fails, the issues are listed with a **Resolution steps** link next to each one. Select **Resolution steps** to open the resolution details and a **Validate &amp; resolve** button. Resolved issues show a green check. **Start Registration** remains disabled until all issues are resolved.
    -   If the scan itself fails, the message "Failed running the pre-onboarding checks. Please check again later." appears and **Start Registration** remains disabled.
3.  Select **Start Registration**.

    The registration process starts. All phases are listed from the start. As each phase completes, it shows a green check. Expand a phase to see its detailed steps. If a step fails, a red error icon appears on that step.

    If a step takes longer than 5 minutes, a delay message is displayed. The process may take a few minutes overall.

4.  When registration completes successfully, select **Configure settings**.

    The **Settings** page opens. Configure the settings for this connection. See the settings reference for the available options.

5.  Save your settings by selecting **Done**.


## Result

When registration completes, the success message `Congrats! You're now connected with <provider name>!` appears with a link to the **Health** tab to monitor connection health. The connection state is set to **Onboarded**. After saving your settings, the **View details** page opens showing the connection details.

## What to do next

[Execute a scan suite as a consumer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/se-con-execute-scan-check.md).

