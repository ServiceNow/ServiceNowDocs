---
title: Upgrade Plan overview
description: Accelerate your upgrades by packaging your skipped records and customizations into the relevant application container \(global apps or app customizations\). Upgrade Plans help you define applications and target versions to be installed in your instance. It automates the installation of these applications during upgrades, giving you a seamless upgrade experience.
locale: en-US
release: xanadu
product: Upgrade Center
classification: upgrade-center
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Exploring Upgrade Center, Upgrade Center, Upgrade, Administer the ServiceNow AI Platform]
---

# Upgrade Plan overview

Accelerate your upgrades by packaging your skipped records and customizations into the relevant application container \(global apps or app customizations\). Upgrade Plans help you define applications and target versions to be installed in your instance. It automates the installation of these applications during upgrades, giving you a seamless upgrade experience.

Navigate to **All** &gt; **Upgrade Center** &gt; **Upgrade Plan**.

You will need the following instances to use Upgrade Plan.

-   Builder instance: Build your upgrade plan
-   Consumer instance: Implement your created upgrade plan

**Note:** Ensure that you have upgraded your instance to the latest available version to build the upgrade plan. It is recommended to configure your dev instance as your builder instance. You are required to install the upgrade plan before upgrading your consumer instance. See [Upgrade Plan Properties](../reference/uc-properties.md#table_h4b_wq2_5tb) for more details.

When you upgrade an instance, resolutions are skipped, and customizations are often loaded post upgrade. This causes temporary breakdown of features until fully loaded. Tasks like committing update sets, installing new plugins and applications, and multiple update are also time consuming. Use the Upgrade Plan feature to automate these post-upgrade tasks by tracking your actions and replay the steps on all the required instances. You don’t have to manually apply post-upgrade tasks which helps in reducing downtime.

**Note:** After upgrading to the latest version, you will see some skipped records. Some of those records will already be marked as reviewed and some of them will need to be reviewed.

## Advantages of Upgrade Plan over Update Sets

You can achieve the following using Upgrade Plans:

-   Along with the skipped record resolution, you can also track app and plugin installation

    **Note:** You won’t be allowed to choose the skipped records that are captured by the upgrade plan. Upgrade plan captures all the skipped records regardless of whether they are reviewed or not and modified or not. If the customizations are coming from different instances, then the skipped records are required to be reviewed.

-   Optimizing the table alters using batch bootstrapping
-   Manage your customizations using the App Repository

**Note:** It is recommended to build an Upgrade Plan for each instance upgrade. When you build an upgrade plan on a builder instance, it gets created to the exactly same as the builder instance version \(including patches and hot fixes\). You can’t use the previously created Upgrade Plan for the new instance upgrade. In case of consumer instances, when you install the upgrade plan, its version should match exactly the consumer instance version.

## Persona

If you are using the app repository for active application development, use Upgrade Plan to accelerate your upgrades.

**Note:** If you are currently using the Update Sets and want to catapult your upgrade process, use the Upgrade Plan feature.

## Design considerations

The following are the important considerations while working with Upgrade Plan:

-   Each new instance upgrade requires its own upgrade plan. It can't be shared across upgrades.
-   Only one builder instance is supported to build the Upgrade Plan
-   Upgrade Plan can’t be uninstalled on a consumer instance. You can rollback the entire upgrade but not partially.
-   The scope of the files moved to **Global Customizations - Upgrade Plan** application by upgrade plan is still global
-   During an upgrade, only the upgrade plan items with **State=Ready** and **Active=true** are installed on the consumer instances. The rest of the items are skipped.
-   Upgrade sets can’t be included in the Upgrade Plan
-   Maint only plugins are not allowed in Upgrade Plan
-   Configure your instance as a builder instance before installing new applications and plugins or during skip resolutions. Otherwise, the actions are not captured by the Upgrade Plan.
-   You can’t view the list of customizations in the Upgrade Plan items view. You can navigate to the respective tables to ensure if the customization has been captured.

See [KB1271313](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1271313) for more information.

## Upgrade Plan background operations

During the building of the upgrade plan, the following operations are done at the background:

-   Skipped records are packaged and uploaded to the App Repository in the form of Global Application and App customization. The following are the 3 types of apps created by Upgrade Plan on your instance and App Repo.

    **Note:** After the packaging is done, you can choose the items from the Upgrade Plan. An Upgrade Plan works at the scope level, so it captures everything and publishes it to the repository.

    -   The global records are packaged into the global customization upgrade plan app and published to the app repo
    -   The scoped skipped records are packaged into the respective app customization packages
    -   When the upgrade plan is published, a global application is created, for example, **Upgrade Plan - release name**
-   Existing ServiceNow features like Global Application and App customization are used as application containers that can be installed in all the required instances. See [Legacy - Global application file management](https://www.servicenow.com/docs/access?context=manage_global_application_files&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US) and [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US) for more information.
-   If you install any applications or plugins, they are also captured in the Upgrade plan. But, since they are application life cycle items, they are never pushed to the App Repository.

During the consumption of the upgrade plan, the following operations are done at the background:

-   At first the upgrade plan is validated and then the source from the app repo is downloaded
-   Once the source is downloaded, the app is moved to the ready state

    **Note:** Only the upgrade plan items with **State=Ready** and **Active=true** are installed on the consumer instances. The rest of the items are skipped.

-   Auto-generation of the preview for the upgrade plan

