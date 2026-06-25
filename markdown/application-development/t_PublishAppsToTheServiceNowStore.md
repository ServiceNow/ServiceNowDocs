---
title: Publish an application to the ServiceNow Store
description: Publishing an application to the ServiceNow Store makes it available to everyone.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/t\_PublishAppsToTheServiceNowStore.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Application sharing, Administer your apps, Deploying applications, Building applications]
---

# Publish an application to the ServiceNow Store

Publishing an application to the ServiceNow Store makes it available to everyone.

## Before you begin

To publish an application to the ServiceNow Store:

-   Create an application within a private application scope.
-   Join the [Technology Partner Program](https://tpp.servicenow.com/$appstore.do#!/tpp/program).
-   Have the application certified.

**Note:** Applications in the global scope cannot be published to the ServiceNow Store.

Role required: admin, or delegated\_developer with Publish To App Store permission enabled

## About this task

After you have met the prerequisites, you can publish the application to the ServiceNow Store

**Note:**

The **Can Edit Application in Studio** property defaults to true for new applications, but you can set it false before publishing.

In Studio, when an application customization has the **Can Edit Application in Studio** property set to false, the user sees this warning:

\[Omitted image "can-edit-app-studio-warning.png"\] Alt text: Can Edit Application in Studio warning

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **Applications**.

2.  Click the **In Development** tab.

3.  Open the application record you want to publish to the ServiceNow Store.

4.  Click the **Publish to Store** related link.

5.  Fill in the fields, as appropriate \([see table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/application-repository-self-hosted/t_PublishAppsToTheAppRepository.md)\).

    \[Omitted image "PublishToMarketplace.png"\] Alt text: Publish an application to the marketplace

6.  Enter your HI credentials.

7.  Click **Submit**.

    The system uploads the current version of the application to the ServiceNow Store allowing other users to download it.


**Parent Topic:**[Application sharing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_SharingApplications.md)

**Related topics**  


[Delegate development and deployment permissions to personnel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/delegated-development-and-deployment/t_AddADeveloper.md)

