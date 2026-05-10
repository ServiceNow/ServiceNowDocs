---
title: Install Health and Safety Core
description: You can install the Health and Safety Core \(sn\_ohs\_im\) if you have an admin role. This data model includes demo data and installs related ServiceNow Store plugins if they are not already installed.
locale: en-US
release: australia
product: Health and Safety Core
classification: health-and-safety-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Health and Safety Core, Health and Safety, Employee Service Management]
---

# Install Health and Safety Core

You can install the Health and Safety Core \(sn\_ohs\_im\) if you have an admin role. This data model includes demo data and installs related ServiceNow® Store plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Health and Safety Core](https://store.servicenow.com/store/app/b32ce76e1b246a50a85b16db234bcb02) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The following items are installed with Health and Safety Incident Management:

-   Plugins
-   Store applications
-   Roles
-   Scheduled jobs
-   Tables

For more information, see [Components installed with Health and Safety Core](../reference/components-installed-hs-core.md).

This table lists the optional applications that can be installed for additional features:

<table id="table_ix1_bff_gxb"><thead><tr><th>

Application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Geo map component

 \[sn\_geo\_map\]

</td><td>

Provides access to enable the map component in the Health and Safety Workspace from the application properties.

 To install, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateAPlugin.md)

</td></tr><tr><td>

Geolocation plugin

 \[com.snc.geolocation\]

</td><td>

Enables geolocation feature on the Now Mobile app and gives access to manual tracking options.

 For more information, see [Enabling and selecting location tracking options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/location-tracking-enable.md)

</td></tr><tr><td>

Learning Core\[sn\_lc\]

</td><td>

Installs Learning Core to enable learning content in Health and Safety actions.For more information, see [Configuring Learning Core](../../human-resources/concept/configuring-learning-core.md).

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Health and Safety Core application \(sn\_ohs\_im\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


**Parent Topic:**[Setting up Health and Safety Core](../concept/setting-up-hs-core.md)

**Related topics**  


[Workplace location data](../../ohs-incident-management/task/configure-hs-workplace-location-data.md)

[Enable a Health and Safety table for configuring report field mapping](../../ohs-incident-management/task/enable-hs-table-report-field-mapping.md)

[Create a safety report field mapping for generating reports](../../ohs-incident-management/task/create-safety-report-field-mapping.md)

[Configure groups for Health and Safety](../../ohs-incident-management/task/configure-groups-health-and-safety.md)

[Configure scheduled job to generate frequency rates](../../ohs-incident-management/task/configure-job-generate-frequency-rates.md)

[Assign Health and Safety profile to a user](../../ohs-incident-management/task/assign-hs-profile-user.md)

[Add a Health and Safety visitor](../../ohs-incident-management/task/hs-add-health-safety-visitor.md)

[Migrate existing safety documents to the Document library](hs-migrate-sync-existing-safety-document-docs-library.md)

