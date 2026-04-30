---
title: Customizations tracked by update sets
description: Update sets can track customizations to application tables, fields, and records.
locale: en-US
release: zurich
product: System Update Sets
classification: system-update-sets
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Explore, System update sets, Deploying applications, Building applications]
---

# Customizations tracked by update sets

Update sets can track customizations to application tables, fields, and records.

Update sets track customizations under these conditions:

-   Where the table has an update\_synch dictionary attribute.
-   Where there is a special handler to track changes to multiple tables.
-   Where the administrator has not excluded a field from updates.

In general, update sets capture configuration information but not task or process data. For example, update sets track service catalog item definitions and related configuration data like variables and variable choices. However, if you test the service catalog by placing orders, update sets do not track order requests, items, and catalog tasks.

Update sets have a limited capacity to transfer data as application files. For larger data transfers, export data and import it with an import set or web service.

Do not combine the usage of both Update Sets and the Application Repository for scoped app development. This will result in numerous issues, including skipped changes, commit errors, and more. Once you have installed an application from the Application Repository, you must continue to develop and publish to the Application Repository for all future development. If you decide to develop an application using update sets, you must continue to use that method exclusively.

## update\_synch attribute

To see the list of tables where customizations are tracked, navigate to **System Definition** &gt; **Dictionary** and filter on attributes CONTAINS update\_synch.

**Warning:** Do not add the `update_synch` attribute to a dictionary record. When improperly used, this attribute can cause major performance issues or cause the instance to become unavailable. Because of this, the `update_synch` attribute is not accessible to customers.

A default rule blocks the use of the `update_synch` attribute on a table for which it is not predefined to avoid the following issues:

-   Some core tables require special update handling because they represent information on multiple tables. When the `update_synch` attribute is added to these tables, duplicate update records are created, causing major conflicts that are difficult to troubleshoot and repair.
-   Using the update\_synch attribute to migrate data records between instances can cause performance issues, because it is not intended for this purpose. To migrate data, use an instance-to-instance import.

    See [Import sets](https://www.servicenow.com/docs/access?context=c_ImportSetsKeyConcepts&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).


## Special handlers

Some changes require special handlers because they represent information on multiple tables. These changes are packaged into one update set entry so that all records are properly updated when the customization is committed. The following changes are tracked with special handlers:

-   Workflows
-   Form sections
-   Lists
-   Related lists
-   Choice lists
-   System dictionary entries
-   Field labels

**Warning:** The form sections, lists, related lists, choice lists, and field labels special handlers delete and reinsert records. This might cause unexpected results and data loss if there are fields referencing the tables.

## Choice lists

Update sets store both new and updated choice options as separate records in the Update Version `[sys_update_version]` and Customer Update `[sys_update_xml]` tables. For example, you create a new Activity `[u_activity]` table that extends the Task table. You then add a new choice option to the Task state field that is only visible for your extended table \(for example, My State\).

When you publish these changes as an update set, the update only contains update and version records for the choice you added to the u\_activity table. The choice options in the task table are unaffected.

**Warning:** Do not use large choice lists in update sets. Doing so leads to excessively long update set commits.

## Dictionary changes

Usually, using update sets prevent you from applying dictionary changes that result in data loss. Blocked dictionary changes include:

-   Removing tables
-   Changing a column data type

Update sets do not track the removal of tables from the system dictionary. Instead, customers must manually remove tables from the target instance. While update sets track data type changes, the target instance skips any change that results in data loss and instead adds a log message about the action. Customers can use the log to manually make data type changes on the target instance.

**Note:** Update set previews do not check for type mismatch problems since the target instance skips changes resulting in data loss. Also, using update sets to delete a column from a table can cause data loss in certain circumstances. If there is data in the column on the target instance, that data is deleted, as well as the column itself, when the update set is committed. A warning message appears if you attempt to commit an update set that deletes a column. The message states that there are one or more delete updates that cause the data to be deleted, and it specifies what delete updates there are.

## Homepages and content pages

Homepages and content pages are not added to update sets by default. Add pages to the current update set by unloading them.

**Important:**

The functionality found in homepages, arranging information from your instance to tell a story about your data, is found in dashboards on new instances. On upgraded instances with Next Experience enabled, users can view existing homepages if they have a direct URL, but they can't create or edit them. Responsive dashboards and Analytics Center dashboards take over homepage functionality.

Use the [Homepage deprecation help tool](https://www.servicenow.com/docs/access?context=homepage-deprecation-help-tool&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) to convert the homepages on your instance to responsive dashboards.

For more information, see:

-   [Dashboards in the Analytics Center](https://www.servicenow.com/docs/access?context=analytics-center-dashboards&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).
-   [Working with responsive dashboards](https://www.servicenow.com/docs/access?context=c_ResponsiveDashboards&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

## Application changes

The system creates a separate update set for each application that only contains changes associated with the application. This ensures that access settings for each application are properly evaluated and applied when committing update set changes.

