---
title: Install a ServiceNow Store application
description: Install an application that you purchased from the ServiceNow Store to make it available on your instance.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use, Legacy Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Install a ServiceNow Store application

Install an application that you purchased from the ServiceNow Store to make it available on your instance.

## Before you begin

-   Purchase an application from the ServiceNow Store.
-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Role required: admin, sn\_appclient.app\_client\_company\_installer \(can only install applications that match the instance company\), or sn\_appclient.app\_client\_user

## About this task

Applications that you purchase from the ServiceNow Store are added to the Application Manager automatically. You must install the application from the Application Manager to activate it in an instance.

To install an application that you published to the ServiceNow application repository, follow the steps in [Install an application from the application repository](https://www.servicenow.com/docs/access?context=install-app-from-repo&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US) instead.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find an application, you may have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data comprises the sample records that describe application features for the common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.

7.  Click **Go to Subscription Management** to map the installed application to a subscription.


**Parent Topic:**[Using Legacy Application Manager](using-legacy-application-manager.md)

**Related topics**  


[Install customizations from an application repository](https://www.servicenow.com/docs/access?context=install-customizations-from-app-repo&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)

[System-managed developer and deployment roles](https://www.servicenow.com/docs/access?context=delegated_deployment_user_roles&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)

