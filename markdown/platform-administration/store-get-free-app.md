---
title: Get a free application
description: Get an app that's available at no additional cost from the ServiceNow Store when the app has custom terms and conditions or requires provider approval.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [get an app, servicenow store, store, app store, application store, app store user documentation, servicenow app store]
breadcrumb: [Getting apps, ServiceNow Store, Administering applications, Get started, Administer]
---

# Get a free application

Get an app that's available at no additional cost from the ServiceNow Store when the app has custom terms and conditions or requires provider approval.

## Before you begin

You must be logged in to the ServiceNow Store with your Now Support account credentials.

Role required: none

## About this task

Applications that are available at no additional cost must be procured from the ServiceNow Store before installation in the following scenarios:

-   If the application has the "Approval Required" state indicator in the Application Manager, it must be requested through the ServiceNow Store.
-   If the application has the "App Terms Not Accepted" state indicator in the Application Manager, it has custom terms and conditions that must be accepted from the ServiceNow Store.
-   If a new application version has the "App Terms Not Accepted" indicator in the Application Manager, that version has custom terms and conditions that must be accepted from the ServiceNow Store before the application can be updated.

For more information about application state indicators, see [Application state indicators in Application Manager](../../application-manager/reference/app-mgr-state-indicators.md).

## Procedure

1.  Log in to the ServiceNow Store using your Now Support account credentials.

    For more information about accessing isolated federal or regional version of the ServiceNow Store, see [Access the ServiceNow Store for a regulated environment](access-regulated-store.md).

2.  Find and select the application in the ServiceNow Store to navigate to the listing details.

3.  Select **Request app** to request procurement approval if required by the provider.

    You receive an email informing you whether the request is approved.

4.  Accept any unacknowledged custom terms and conditions from the ServiceNow Store.

    1.  From the application listing details in the ServiceNow Store, select **Accept Terms**.

    2.  Download and review the custom terms and conditions.

    3.  Select the option to agree to the terms and conditions.

    4.  Select **Accept**.


## Result

If you use the commercial ServiceNow Store, the application is available for installation from the Application Manager within 24 hours. If you use an isolated federal or regional instance of the ServiceNow Store, the application is available within two business days of final approval. For more information about using the Application Manager, see [Application Manager](../../application-manager/concept/application-manager.md).

If the application isn't available to install from the Application Manager within the expected amount of time, try the following actions.

-   Verify that all necessary dependencies have been procured. For more information, see [Evaluating version requirements and dependencies](../concept/versions-dependencies.md).
-   Review application state indicators from application's details in the Application Manager. For more information about what each indicator means, see [Application state indicators in Application Manager](../../application-manager/reference/app-mgr-state-indicators.md).
-   If the previous options don't work, contact Now Support for assistance.

## What to do next

Install the app on compatible production or non-production instances, based on whether you have a hosted or on-premise instance:

-   If your instance is in a hosted regulated environment, install the app using the Application Manager. For more information, see [Install an application or plugin](../../../build/applications/task/installing-applications-in-application-manager.md).
-   If your instance is in an on-premise environment, download the encrypted app file from your federal or regional instance of the ServiceNow Store and upload the file to your instance. For more information, see [Getting apps as an on-premise customer](../concept/getting-apps-on-prem.md)

