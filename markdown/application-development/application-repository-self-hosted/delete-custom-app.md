---
title: Delete an application from the application repository
description: Delete an application from the application repository so that it's no longer available to your company instances.
locale: en-US
release: yokohama
product: Application Repository \(Self-Hosted\)
classification: application-repository-self-hosted
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage applications, ServiceNow application repository, Application sharing, Administer your apps, Deploying applications, Building applications]
---

# Delete an application from the application repository

Delete an application from the application repository so that it's no longer available to your company instances.

## Before you begin

-   [Publish an application to the application repository](t_PublishAppsToTheAppRepository.md)
-   You can delete an application only if the application is not installed on any of your company instances. Uninstall the application on all your instances before deleting it from the application repository.

Role required: Primary customer admin of the account

## Procedure

1.  Go to [https://apprepo.service-now.com/sn\_appstore\_store.do](https://apprepo.service-now.com/sn_appstore_store.do).

2.  Log in using your Now Support credentials.

3.  **Note:** Customers using the Federal Store must log in to HIWave and then select the Federal Store option at the bottom of the page. Then, under your company name, select My Repository to proceed.

4.  Select the expand arrow next to your name and select **My app repos**.

    ![Expanded user menu with my app repos option highlighted.](../image/app-manager-open-app-repo.png)

5.  Next to the application listing, click **Select Action** and then click **Flag for Deletion**.

6.  On the confirmation window, click **Yes**.

    After you flag an application for deletion, the application is deleted automatically after 90 days.

7.  To delete the application immediately:

    1.  Open the Flagged Apps tab.

    2.  Next to the application listing, click **Select Action** and then click **Delete Immediately**.


