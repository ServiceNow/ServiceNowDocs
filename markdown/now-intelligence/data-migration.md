---
title: Platform Analytics Migration Center
description: When you migrate your Core UI data, your existing dashboards, reports, interactive filters, and Performance Analytics widgets are moved to Platform Analytics. When you activate the migration, the result is a single set of visualizations and unified filters for all data sources.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Migrate a dashboard, migrate a Core UI dashboard, migrate a responsive dashboard]
breadcrumb: [Platform Analytics experience, Platform Analytics]
---

# Platform Analytics Migration Center

When you migrate your Core UI data, your existing dashboards, reports, interactive filters, and Performance Analytics widgets are moved to Platform Analytics. When you activate the migration, the result is a single set of visualizations and unified filters for all data sources.

**Note:**

To learn more about Platform Analytics and the Migration Center, see the [Platform Analytics enablement toolkit](https://sn.works/analytics/pae) on the ServiceNow Community.

From the Zurich release, however both Core UI and Platform Analytics experience dashboards and visualizations sit side by side in the Platform Analytics library.

Once migration is complete, you won't be able to add Core UI reports, PA widgets and filters to Platform Analytics experience dashboards. It is possible to add only migrated content and content created within Platform Analytics experience to these dashboards.

It is not possible to migrate dashboards using an update set.

## What is migrated

The migration process takes your dashboard content and migrates it from Core UI \(Dashboards and visualizations in the classic environment\) to the Platform Analytics library. You then access all of your analytics through a unified navigation menu. If you use indicators, you get tools to alert you of significant changes.

**Note:** When you upgrade releases, the Migration Center automatically migrates any previously incompatible content that is now compatible.

## What isn't migrated

The short answer is that almost everything is migrated. Most Core UI dashboard content is supported in Platform Analytics experience. Some content doesn’t have an analogous Platform Analytics feature. Any dashboard with content that isn't migrated and is migrated into a container, also called an iframe. This is called Compatibility mode. For detailed information about content that isn't migrated, see [Content not migrated or migrated in compatibility mode](../reference/data-mig-unmigrated-content.md).

## What is the migration process

The migration process has the following steps.

-   **Remove unused dashboards**

    Remove any unused dashboards and reports to promote a streamlined process.

    -   Navigate to pa\_dashboards.list, select the dashboards you want to delete, and then select **Actions on selected rows** &gt; **Delete**.
    -   Navigate to **All** &gt; **Reports** &gt; **Administration** &gt; **All**, select the reports you want to delete, and then select **Actions on selected rows** &gt; **Delete**.
-   **Run the migration procedure**

    The procedure identifies what can be migrated directly into Platform Analytics and what is migrated in Compatibility Mode.

-   **Review the migration results**

    You may identify dashboards or other content that you don't want to migrate, for example, unused dashboards, out-of-date visualizations, or filters that don't work as expected.

-   **Activate the migration**

    Activation might be time-consuming, depending on how much content you are migrating.


## Create custom content

You can use tools such as UI Builder to create custom content that meets the needs of content that doesn't migrate.

## What happens to my menus

Before migration, users navigated to **Self Service** &gt; **Dashboards** to view the dashboard overview and to **Reports** &gt; **View / Run** to view the list of reports. After you activate the migration, all analytics content, including dashboards, data visualizations, filters, and KPIs are under **Platform Analytics** &gt; **Library**.

## Block Migration Options

You can disable the **Start Moving** and **Activate** Platform Analytics experience options. Create the system property `com.glide.par.coreui.migration.enabled` and set it to `False`. If you set the property to `False` before you migrate any content, both options are disabled. If you set the property to false after you migrate your content, only the **Activate** button is disabled.

If you want to start the migration and view what artifacts are in compatibility mode, and resolve any issues, set the property to `False` after you run the migration to prevent activation of Platform Analytics experience. If you want to prevent the migration process, set the property to `False` first.

For more information, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

