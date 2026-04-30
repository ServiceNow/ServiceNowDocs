---
title: Publish app changes to the Application Repository from ServiceNow Studio
description: Publish changes that you have made to an app in ServiceNow Studio to the Application Repository \(App Repo\).
locale: en-US
release: zurich
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ServiceNow Studio quick start, Explore, ServiceNow Studio, Developing your application, Building applications]
---

# Publish app changes to the Application Repository from ServiceNow Studio

Publish changes that you have made to an app in ServiceNow Studio to the Application Repository \(App Repo\).

## Before you begin

Role required: admin or delegated developer

## About this task

The App Repo is one option ServiceNow offers for app deployment. You can also [create update sets](qs-create-update-set.md) to publish changes, or if your company has a deployment pipeline set up, you can deploy changes through the pipeline in ServiceNow Studio. For more information about the App Repo, see [ServiceNow application repository](../../applications/concept/app-repo.md).

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Open the **App details** page for the application that you want to update from either the ServiceNow Studio home page or the Navigator panel.

    -   On the ServiceNow Studio home page, select the **Deployment** tab. Then select **Applications** and select your application from the **Name** column.
    -   In the Navigator panel, select the Apps icon \(![Apps icon](../image/sn-studio-app-nav-icon.png)\). Then select your application and select **App details**.
3.  On the App details page, select **Publish**.

4.  In the **New version** field, enter a version number for the changes.

5.  In the **Release notes** field, add notes about the changes that you’re publishing.

6.  Select **Publish**.

    You have submitted your changes for review and approval. Once your changes are approved, your updates are accessible to all instances of your application.


