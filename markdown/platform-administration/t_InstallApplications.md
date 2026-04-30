---
title: Install a ServiceNow Store application
description: Install an application that you purchased from the ServiceNow Store to make it available on your instance.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Legacy Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Install a ServiceNow Store application

Install an application that you purchased from the ServiceNow Store to make it available on your instance.

## Before you begin

-   Purchase an application from the ServiceNow Store.
-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

**Note:**

Legacy Application Manager is being prepared for deprecation. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

A known issue affects the use of bookmarks to access the Legacy Application Manager. For details about possible issues with accessing the Legacy Application Manager, see the [Deprecated Classic App Manager URL usage causes issues on instances running ZP5 / YP10 and above \[KB2804238\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2804238) article in the Now Support knowledge base.

A new Application Manager experience is available. The new experience simplifies the process of managing your licensed applications by consolidating them in one convenient location, displaying all applications, plugins, installed applications, and available updates. For more information, see [Application Manager](../../../administer/application-manager/concept/application-manager.md).

Role required: admin, sn\_appclient.app\_client\_company\_installer \(can only install applications that match the instance company\), or sn\_appclient.app\_client\_user

## About this task

Applications that you purchase from the ServiceNow Store are added to the Application Manager automatically. You must install the application from the Application Manager to activate it in an instance.

To install an application that you published to the ServiceNow application repository, follow the steps in [Install an application from the application repository](https://www.servicenow.com/docs/access?context=install-app-from-repo&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) instead.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find an application, you may have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.

7.  Click **Go to Subscription Management** to map the installed application to a subscription.


**Parent Topic:**[Using Legacy Application Manager](using-legacy-application-manager.md)

**Related topics**  


[Install customizations from an application repository](https://www.servicenow.com/docs/access?context=install-customizations-from-app-repo&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)

[System-managed developer and deployment roles](https://www.servicenow.com/docs/access?context=delegated_deployment_user_roles&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)

