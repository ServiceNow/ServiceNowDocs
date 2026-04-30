---
title: Activate Intelligent Task Recommendation
description: Activate the Intelligent Task Recommendation plugin \(com.snc\_task\_recommendations\)\) for Field Service Management if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up Intelligent Task Recommendations, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Activate Intelligent Task Recommendation

Activate the Intelligent Task Recommendation plugin \(com.snc\_task\_recommendations\)\) for Field Service Management if you have the admin role.

## Before you begin

Field Service Intelligent Task Recommendation feature requires the following plugins:

-   Intelligent Task Recommendation \(com.snc\_task\_recommendations\): Provides basic task recommendation framework scripts, configurations, and default extension points.
-   Field Service Management Intelligent Task Recommendations \(com.snc.fsm\_task\_recommendations\): Provides specific implementation and configuration for Field Service Management, which includes default filter constraints, ranking criteria, and Field Service Management extension points.

Ensure the Field Service Management plugin is activated before you install Field Service Intelligent Task Recommendation. See [Activate Field Service Management](../../planning-and-policy/task/t_ActivateFieldServiceManagement.md) for more information.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Intelligent Task Recommendation plugin \(com.snc\_task\_recommendations\)\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  If demo data is available and you want to install it, click **Load demo data**.

    Demo data comprises sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

4.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


