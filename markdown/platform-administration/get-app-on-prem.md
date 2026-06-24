---
title: Get an app or product as an on-premise customer
description: Procure and download encrypted apps, products, and dependencies from the ServiceNow Store for use with your on-premise \(self-hosted\) instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/get-app-on-prem.html
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Getting on-premise apps, ServiceNow Store, Administering applications, Get started, Administer]
---

# Get an appor product as an on-premise customer

Procure and download encrypted apps, products, and dependenciesfrom the ServiceNow Store for use with your on-premise \(self-hosted\) instance.

## Before you begin

You must be logged in to the ServiceNow Store with your Now Support account credentials.

Role required: none

## About this task

If your on-premise instance isn't connected to the internet or to the ServiceNow Store, you can download encrypted applications to use on your instance. Procure and download an application or product and its dependencies using a computer with internet access, then transfer the necessary files to your instance.

If your on-premise instance has been connected to the ServiceNow Store, refer to [Getting apps and trials from the ServiceNow Store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/getting-apps-trials.md) instead.

**Important:** You must repeat this process for each instance you want to upload an app or product to.

## Procedure

1.  From a computer with internet access, log in to the ServiceNow Store and procure the appor product.

    -   For more details about procuring appsand products from the commercial ServiceNow Store, see [Getting apps and trials from the ServiceNow Store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/getting-apps-trials.md).
    -   For more details about procuring apps in a regulated environment, see [Using the ServiceNow Store in a regulated environment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/using-regulated-store.md).
2.  From the app listing details or product page on the ServiceNow Store, select **On-prem download**.

3.  In the pop-up window, use the **Select on-prem instance** drop-down list to select an instance associated with your account.

4.  Select an encryption certificate through the **Use existing**, **Generate new**, or **Upload new** options.

    -   Select **Use existing** if you recently downloaded an application for the same instance you selected in step 3. If no certificate is automatically populated when you select **Use existing**, select **Generate new** or **Upload new** instead.
    -   Select **Generate new** if you don't have an encryption certificate or if your encryption certificate has expired.
    -   Select **Upload new** if you want to use the same encryption certificate you generated to install an application on a different instance.
<table><thead><tr><th align="left" id="d221279e238">

Option

</th><th align="left" id="d221279e241">

Procedure

</th></tr></thead><tbody><tr><td id="d221279e247">

**__Use existing__**

</td><td>

If a certificate is automatically populated, proceed to the next step. If no certificate is automatically populated, select **Generate new** or **Upload new** instead.

</td></tr><tr><td id="d221279e263">

**__Generate new__**

</td><td>

1.  In the **Password** field, enter the password you want to use with the new certificate.
2.  Select **Generate**.
 A new encryption certificate is available for download.

</td></tr><tr><td id="d221279e292">

**__Upload new__**

</td><td>

1.  In the **Password** field, enter the password that was used to generate the certificate you want to use.
2.  In the **Upload file** field, add the encryption certificate.
3.  Select **Upload**.


</td></tr></tbody>
</table>    For more information about generating encryption certificates and uploading them to your ServiceNow AI Platform instances, see [How to generate and upload a certificate for on-prem store app \| Troubleshooting common issues or errors \[KB1080332\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1080332).

5.  Select a compatible application version to download from the **Version** drop-down list next to the application name.

    Only versions compatible with the instance selected in step 3 are displayed.

    On-prem product downloads display multiple applications with **Version** drop-down lists. Applications that you don't specify a version for are excluded from download.

6.  Select **Download Application** to download an encrypted `.store` filewith the selected apps and their dependencies.

    **Note:** The `.store` file has an expiration date two weeks from the date of download. If more than two weeks pass before you upload it to your instance, you must download a new `.store` file.


## What to do next

Transfer the `.store` file to your on-premise instance to upload the app. For more information, see [Upload an app to an on-premise instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/upload-app-on-prem-instance.md).

