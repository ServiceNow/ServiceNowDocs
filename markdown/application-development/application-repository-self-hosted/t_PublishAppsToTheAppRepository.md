---
title: Publish an application to the application repository
description: Publish a custom application to the application repository so that it can be installed on other instances in your organization.
locale: en-US
release: yokohama
product: Application Repository \(Self-Hosted\)
classification: application-repository-self-hosted
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage applications, ServiceNow application repository, Application sharing, Administer your apps, Deploying applications, Building applications]
---

# Publish an application to the application repository

Publish a custom application to the application repository so that it can be installed on other instances in your organization.

## Before you begin

To enable a developer to publish an application to the application repository, delegate the Publish to App Repo permission to the developer. For more information, see [Delegate development and deployment permissions to personnel](t_AddADeveloper.md).

Role required: admin or delegated\_developer with Publish To App Repo permission enabled

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **My Company Applications**.

2.  Open the In Development tab.

3.  Open the application record that you want to publish to the application repository.

4.  Select the **Publish to My Application Repository** related link.

5.  Select **Submit**.


## What to do next

Install the application on company instances so that your organization can start using it. For more information, see [Install an application from the application repository](install-app-from-repo.md).

By default, after you publish an application to the application repository, all your company instances are entitled to the application automatically. To limit which company instances are entitled to the application, access the application repository by going to [https://apprepo.service-now.com/sn\_appstore\_store.do](https://apprepo.service-now.com/sn_appstore_store.do), and then change the entitlement type for the application.

**Note:**

The **Can Edit Application in Studio** property defaults to true for new applications, but you can set it false before publishing.

In Studio, when an application customization has the **Can Edit Application in Studio** property set to false, the user sees this warning:![Can Edit Application in Studio warning](../image/can-edit-app-studio-warning.png)

For more information, see [Manage application entitlements from the application repository](manage-app-entitlements.md) and [Legacy - Access ServiceNow Studio](t_AccessStudio.md).

