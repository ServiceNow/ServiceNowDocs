---
title: Accessing unpurchased recommended apps on ServiceNow Store
description: Administrators can access the list of unpurchased ServiceNow Store apps, view recommended apps, and view details of the required app without navigating to the ServiceNow Store.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Legacy Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Accessing unpurchased recommended apps on ServiceNow Store

Administrators can access the list of unpurchased ServiceNow Store apps, view recommended apps, and view details of the required app without navigating to the ServiceNow Store.

**Note:**

Legacy Application Manager is being deprecated. Starting with Australia patch 1, Legacy Application Manager is no longer available and bookmarks will redirect to the new Application Manager experience.

A known issue affects the use of bookmarks to access the Legacy Application Manager before Australia patch 1. For details about possible issues with accessing the Legacy Application Manager, see the [Deprecated Classic App Manager URL usage causes issues on instances running ZP5 / YP10 and above \[KB2804238\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2804238) article in the Now Support knowledge base.

A new Application Manager experience is available. The new experience simplifies the process of managing your licensed applications by consolidating them in one convenient location, displaying all applications, plugins, installed applications, and available updates. For more information, see [Application Manager](../../../administer/application-manager/concept/application-manager.md).

To access the list of unpurchased ServiceNow Store apps, navigate to **System Applications** &gt; **All Available Applications** &gt; **Available To Obtain From Store**. The recommended apps, have the **Recommended** indicator on the application tile. You can also use the filter options available under **Additional Filters** to populate the required apps. The filter options include:

|Filter option|Description|
|-------------|-----------|
|Free Trial|App is available for a free trial.|
|Service Graph Connector|App type is Service Graph Connector.|
|Purchase In Process|Request to purchase the app is in process and the app has not been purchased on ServiceNow Store yet.|
|Rejected Request|Request for app trial or purchase is rejected.|
|Request in Progress|Request for app trial or purchase has been initiated and response from the vendor is awaited.|

-   To view the app details that are available on ServiceNow Store, click **View Details**.
-   To purchase or try the required app, on the app details page, click:

    -   **Get** for free apps.
    -   **Buy** for paid apps.
    -   **Request App** for free or paid apps that require approval from vendor to purchase the app.
    -   **Request Trial** for free or paid apps that require approval from vendor to try the app.
    -   **Try** before procuring the application directly from the application manager.
    You will be redirected to the ServiceNow Store from where you can purchase the app.


**Parent Topic:**[Using Legacy Application Manager](using-legacy-application-manager.md)

