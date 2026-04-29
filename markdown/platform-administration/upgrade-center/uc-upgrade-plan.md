---
title: Upgrade Plan overview
description: Accelerate your upgrades using the Upgrade Plan that automates the installation of applications during upgrades, giving you a seamless upgrade experience. It helps you define applications and target versions to be installed in your instance.
locale: en-US
release: australia
product: Upgrade Center
classification: upgrade-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Exploring Upgrade Center, Upgrade Center, Upgrade, Administer the ServiceNow AI Platform]
---

# Upgrade Plan overview

Accelerate your upgrades using the Upgrade Plan that automates the installation of applications during upgrades, giving you a seamless upgrade experience. It helps you define applications and target versions to be installed in your instance.

Navigate to **All** &gt; **Upgrade Center** &gt; **Upgrade Plan**.

You will need the following instances to use Upgrade Plan.

-   Builder instance: Build your upgrade plan
-   Consumer instance: Implement your created upgrade plan

**Note:** Ensure that you have upgraded your instance to the latest available version to build the upgrade plan. It is recommended to configure your dev instance as your builder instance. You are required to install the upgrade plan before upgrading your consumer instance. See [Upgrade Plan Properties](../reference/uc-properties.md#table_h4b_wq2_5tb) for more details.

When you upgrade an instance, resolutions are skipped, and customizations are often loaded post upgrade. This causes temporary breakdown of features until fully loaded. Tasks like committing update sets, installing new plugins and applications, and multiple update are also time consuming. Use the Upgrade Plan feature to automate these post-upgrade tasks by tracking your actions and replay the steps on all the required instances. You don’t have to manually apply post-upgrade tasks which helps in reducing downtime.

**Note:** After upgrading to the latest version, you will see some skipped records. Some of those records will already be marked as reviewed and some of them will need to be reviewed.

Starting Yokohama release, customizations and skipped records are not a part of the Upgrade Plan, by default. You can choose to include the customizations and skipped records along with the app installations within the Upgrade Plan by enabling the glide.upgrade.plan.include.skips property. This property controls about when skips and customizations are included when you build or refresh an Upgrade Plan.

-   When glide.upgrade.plan.include.skips property is **TRUE**, skips and customizations are included when an Upgrade Plan is built or refreshed
-   When glide.upgrade.plan.include.skips property is **FALSE**, skips and customizations aren't included when an Upgrade Plan is built or refreshed. This property has been set to False by default.

You will see one of the following modal messages depending on the scenario:

-   First time user: When you are building your Upgrade Plan for the first time \(the property is disabled by default\)

    ![Screenshot showing first time user for Upgrade Plan](../image/uc_up_first_time_user.png)

-   Building the upgrade plan with the property enabled

    ![Screenshot showing building of Upgrade Plan with property enabled](../../upgrade-management/image/uc_build_up_property_enabled.png)

-   Refreshing the Upgrade Plan with the property disabled \(default\)

    ![Screenshot showing refreshing of the Upgrade Plan with property disabled](../../upgrade-management/image/uc_refresh_up_property_disabled.png)

-   Refreshing the Upgrade Plan with the property enabled

    ![Screenshot showing refreshing of the Upgrade Plan with property enabled](../../upgrade-management/image/uc_refresh_up_property_enabled.png)


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
-   Existing ServiceNow features like Global Application and App customization are used as application containers that can be installed in all the required instances. See [Legacy - Global application file management](https://www.servicenow.com/docs/access?context=manage_global_application_files&version=australia&pubname=australia-application-development&ft:locale=en-US) and [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=australia&pubname=australia-application-development&ft:locale=en-US) for more information.
-   If you install any applications or plugins, they are also captured in the Upgrade plan. But, since they are application life cycle items, they are never pushed to the App Repository.

During the consumption of the upgrade plan, the following operations are done at the background:

-   At first the upgrade plan is validated and then the source from the app repo is downloaded
-   Once the source is downloaded, the app is moved to the ready state

    **Note:** Only the upgrade plan items with **State=Ready** and **Active=true** are installed on the consumer instances. The rest of the items are skipped.

-   Auto-generation of the preview for the upgrade plan

