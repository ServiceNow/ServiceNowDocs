---
title: Install the app collaboration application
description: Install the app collaboration application so that you can view the collaboration feature in the UI.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Application collaboration, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Install the app collaboration application

Install the app collaboration application so that you can view the collaboration feature in the UI.

## Before you begin

Download the app collaboration application so that you can view the collaboration feature.

You must have an App Engine license.

Role required: admin

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Click the search icon \(![Search](../../../common/image/List_SearchIcon.png)\) in the middle of the screen to search for the application collaboration application.

3.  Click **Install**.

    **Note:** If app collaboration is already installed, the **Install** button is inactive.

4.  Click **Activate**.


## Result

The app collaboration feature is active.

After you install and activate the app collaboration plugin, all delegated developers will receive custom collaboration descriptors based on their current permissions and applications. The base system table provides standard Owner and Editor collaboration descriptors which are used in the collaboration feature.

If you install this plugin without App Engine Studio \(AES\) for an application, you should manage the delegated development permissions with this plugin or use the old Manage Developers screen to manage the permissions. Do not use both the plugin and the Manage Developers screen to manage the delegated development permissions.

To use the old Manage Developers screen, select your application and select Manage Developers in the related links on the form.

