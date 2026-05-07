---
title: Activate Smart Assessment for Field Service questionnaire
description: You can activate the Smart Assessment for Field Service Questionnaire plugin \(sn\_fsm\_smart\_asmt\) for Field Service Management if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: australia
product: Mobile Experience for Field Service Management \(Glide Family\)
classification: mobile-experience-for-field-service-management-glide-family
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up Smart Assessment questionnaires, Setting up Field Service Mobile Agent, Configure, Field Service Management]
---

# Activate Smart Assessment for Field Service questionnaire

You can activate the Smart Assessment for Field Service Questionnaire plugin \(sn\_fsm\_smart\_asmt\) for Field Service Management if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

Smart Assessment for Field Service Questionnaire requires a separate subscription from the rest of the ServiceNow AI Platform.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

To purchase a subscription, contact your ServiceNow account manager. When you purchase a subscription, certain plugins are activated automatically. If a paid plugin isn't activated automatically, you can manually activate it from the All Applications list in your instance.

**Note:**

Before purchasing a subscription, you can evaluate the feature on a non-production instance without charge by requesting it from the Now Support Service Catalog.

Role required: admin, questionnaire\_admin

Ensure the following plugins are activated before you install Smart Assessment for Field Service Questionnaire.

-   Field Service Management \(field\_service\_management\)
-   Field Service Questionnaire
-   Field Service Mobile
-   Smart Assessment for Mobile
-   Smart Assessment Dependencies
-   Smart Assessment Core
-   Smart Assessment Designer
-   Smart Assessment Connected
-   Smart Assessment Migration Tools

## About this task

The following items are installed with Smart Assessment for Field Service Questionnaire:

-   Plugins
-   Tables
-   Business rules
-   Script includes
-   Scheduled job

For more information, see [Smart Assessment components](../reference/smart-assessment-components.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


**Related topics**  


[Enable Smart Assessment Questionnaire](enable-smart-assessment-questionnaire.md)

[Migrating to Smart Assessment from survey-based questionnaire](../concept/configuring-sa-by-migrating.md)

