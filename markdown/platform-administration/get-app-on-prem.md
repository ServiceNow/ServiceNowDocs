---
title: Get an app as an on-premise customer
description: Procure and download an encrypted app from the ServiceNow Store for use with your on-premise \(self-hosted\) instance.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Getting on-premise apps, ServiceNow Store, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Get an app as an on-premise customer

Procure and download an encrypted app from the ServiceNow Store for use with your on-premise \(self-hosted\) instance.

## Before you begin

You must be logged in to the ServiceNow Store with your Now Support account credentials.

Role required: none

## About this task

If your on-premise instance isn't connected to the internet or to the ServiceNow Store, you can download encrypted applications to use on your instance. Procure and download the application using a computer with internet access, then transfer the necessary files to your instance.

If your on-premise instance has been connected to the ServiceNow Store, refer to [Getting apps and trials from the ServiceNow Store](../concept/getting-apps-trials.md) instead.

**Important:** You must repeat this process for each instance you want to upload the app to.

## Procedure

1.  From a computer with internet access, log in to the ServiceNow Store and procure the app.

    -   For more details about procuring apps from the commercial ServiceNow Store, see [Getting apps and trials from the ServiceNow Store](../concept/getting-apps-trials.md).
    -   For more details about procuring apps in a regulated environment, see [Using the ServiceNow Store in a regulated environment](../concept/using-regulated-store.md).
2.  From the app listing details on the ServiceNow Store, select **Manage Entitlements** to confirm that all of your instances have been entitled.

3.  Select **On-prem Download**.

4.  In the pop-up window, select which entitled instance you want to install the app to.

5.  Add an encryption certificate.

    -   If you don't have a certificate or if your certificate is expired, select **Generate New Certificate**. For more information about generating certificates, see [How to generate and upload a certificate for on-prem store app \[KB1080332\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1080332).
    -   If you have already generated a certificate to install an app on a different instance, you can use the same certificate. Select **Upload New Certificate** and upload the certificate that was saved previously.
    -   If you have already downloaded an app for the selected instance, you can use the same certificate. The certificate might be automatically populated in this case.
6.  Select **Download Application** to download an encrypted `.store` file.

    **Note:** The `.store` file has an expiration date two weeks from the date of download. If more than two weeks pass before you upload it to your instance, you must download a new `.store` file.


## What to do next

Transfer the `.store` file to your on-premise instance to upload the app. For more information, see [Upload an app to an on-premise instance](upload-app-on-prem-instance.md).

