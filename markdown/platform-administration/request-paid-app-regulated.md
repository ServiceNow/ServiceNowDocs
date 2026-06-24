---
title: Request a paid app for a regulated environment
description: Request to buy a paid app from a federal or regional ServiceNow Store instance to make that app available on your regulated instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/request-paid-app-regulated.html
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using a regulated environment, ServiceNow Store, Administering applications, Get started, Administer]
---

# Request a paid app for a regulated environment

Request to buy a paid app from a federal or regional ServiceNow Store instance to make that app available on your regulated instance.

## Before you begin

Role required: none

## Procedure

1.  Access the federal or regional ServiceNow Store instance that corresponds to your regulated environment.

    For more information, see [Access the ServiceNow Store for a regulated environment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/access-regulated-store.md).

2.  Find and select a paid app or integration.

3.  Conduct a security review to verify that the app or integration meets the requirements for your regulated instance.

4.  Request to purchase a license for the application or integration.

    -   If the application is provided by ServiceNow, select **Request license**.
    -   If the application is provided by a partner and requires approval, select **Request purchase**.
    If your request is approved, a sales representative or your account executive contacts you by email to process your purchase. Approval is granted at the provider's discretion.

    For questions about an application provided by ServiceNow, contact your account executive. For questions about an application provided by a partner, contact the partner directly.

5.  Follow the emailed instructions to complete the purchase.

    **Note:** It can take up to two business days for the application to become available in the Application Manager after final license confirmation.

6.  If the application displays the "App Terms Not Accepted" state indicator in the Application Manager, accept the custom terms and conditions from the ServiceNow Store.

    For more information about application state indicators, see [Application state indicators in Application Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/application-manager/app-mgr-state-indicators.md).

    1.  From the application listing details in the ServiceNow Store, select **Accept Terms**.

    2.  Download and review the custom terms and conditions.

    3.  Select the option to agree to the terms and conditions.

    4.  Select **Accept**.


## Result

Confirmation emails for the application and any dependencies that were procured are sent to the email address associated with your ServiceNow Store account. For information about configuring which email address receives notifications for this application, see [Configure ServiceNow Store application notification preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/configure-store-notifications.md).

The application is available to install within two business days. If the application still can't be installed after two business days, contact Now Support for assistance.

## What to do next

Install the app on compatible production or non-production instances, based on whether you have a hosted or on-premise instance:

-   If your instance is in a hosted environment, install the app using the Application Manager. For more information, see [Install an application or plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/application-manager/installing-applications-in-application-manager.md).
-   If your instance is in an on-premise environment, download the encrypted app file from your federal or regional instance of the ServiceNow Store and upload the file to your instance. For more information, see [Getting apps as an on-premise customer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/getting-apps-on-prem.md)

