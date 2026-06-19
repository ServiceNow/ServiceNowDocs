---
title: Publish an application to the application repository
description: Publish a custom application to the application repository so that it can be installed on other instances in your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/application-repository-self-hosted/t\_PublishAppsToTheAppRepository.html
release: zurich
product: Application Repository \(Self-Hosted\)
classification: application-repository-self-hosted
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage applications, ServiceNow application repository, Application sharing, Administer your apps, Deploying applications, Building applications]
---

# Publish an application to the application repository

Publish a custom application to the application repository so that it can be installed on other instances in your organization.

## Before you begin

To enable a developer to publish an application to the application repository, delegate the Publish to App Repo permission to the developer. For more information, see [Delegating development permissions to personnel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/delegated-development-and-deployment/t_AddADeveloper.md).

Role required: admin or delegated\_developer with Publish To App Repo permission enabled

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **My Company Applications**.

2.  Open the In Development tab.

3.  Open the application record that you want to publish to the application repository.

4.  Select the **Publish to My Application Repository** related link.

5.  Select **Submit**.


## What to do next

Install the application on company instances so that your organization can start using it. For more information, see [Install an application from the application repository](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/application-repository-self-hosted/install-app-from-repo.md).

By default, after you publish an application to the application repository, all your company instances are entitled to the application automatically. To limit which company instances are entitled to the application, access the application repository by going to [https://apprepo.service-now.com/sn\_appstore\_store.do](https://apprepo.service-now.com/sn_appstore_store.do), and then change the entitlement type for the application.

**Note:**

The **Can Edit Application in Studio** property defaults to true for new applications, but you can set it false before publishing.

For more information, see [Manage application entitlements from the application repository](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/application-repository-self-hosted/manage-app-entitlements.md).

