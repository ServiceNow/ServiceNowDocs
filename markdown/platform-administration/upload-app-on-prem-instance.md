---
title: Upload an app to an on-premise instance
description: Upload an application's encrypted file to your on-premise instance to make it available for installation.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Getting on-premise apps, ServiceNow Store, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Upload an app to an on-premise instance

Upload an application's encrypted file to your on-premise instance to make it available for installation.

## Before you begin

Role required: admin

-   The same certificate used when downloading the app must be installed to the instance.
-   For instances that aren't connected to the internet, the system property `sn_appclient.app.install.offline` must be set to `true`. If the value is set to `false`, contact [Customer Service and Support](https://support.servicenow.com/now) and request it be changed to `true`.

## Procedure

1.  From your ServiceNow AI Platform instance, access the Application Manager by navigating to **Admin** &gt; **Application Manager**

2.  Select **Upload Offline Application**.

3.  Upload the `.store` file you received when you downloaded the application from the ServiceNow Store.

4.  Locate and select the app from the list on the **Available for you** page.

    If you can't find the app, refresh the Application Manager and try again.


## What to do next

Install the uploaded application through the Application Manager. For more information, see [Install an application or plugin](../../../build/applications/task/installing-applications-in-application-manager.md).

