---
title: Customizations tracked by update sets
description: Update sets track customizations to application tables, fields, and records.
locale: en-US
release: australia
product: System Update Sets
classification: system-update-sets
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, System update sets, Deploying applications, Building applications]
---

# Customizations tracked by update sets

Update sets track customizations to application tables, fields, and records.

Update sets capture configuration details but exclude task or process data. For example, they record catalog item definitions, variables, and variable choices, but not submitted orders or catalog tasks.

## update\_synch attribute

To see the list of tables where customizations are tracked, navigate to **System Definition** &gt; **Dictionary** and filter on attributes contains update\_synch.

**Warning:** Don’t add the update\_synch attribute to a dictionary record. When improperly used, this attribute can cause major performance issues or cause the instance to become unavailable. The update\_synch attribute isn’t accessible to customers.

A default rule blocks the use of the update\_synch attribute on a table for which it isn’t predefined to avoid the following issues:

-   Some core tables require special update handling because they represent information on multiple tables. When the update\_synch attribute is added to these tables, duplicate update records are created, causing major conflicts that are difficult to troubleshoot and repair.
-   Using the update\_synch attribute to migrate data records between instances can cause performance issues. To migrate data see Import sets key concepts to use an instance-to-instance import.

## Special handlers

Special handlers represent information on multiple tables. These changes are packaged into one update set entry so that all records are properly updated when the customization is committed.

-   Workflows
-   Form sections
-   Lists
-   Related lists
-   Choice lists
-   System dictionary entries
-   Field labels

**Warning:** Form sections, lists, related lists, choice lists, and field label handlers can delete and reinsert records, which may lead to unexpected results or data loss if fields reference those tables.

## Choice lists

Update sets store both new and updated choice options as separate records in the sys\_update\_version and sys\_update\_xml tables. For example, if you extend the Task table with a u\_activity table, add a state field choice visible only in your extended table.

When you publish these changes as an update set, the update only contains update and version records for the choice you added to the u\_activity table. The choice options in the task table are unaffected.

**Warning:** Don’t use large choice lists in update sets. Doing so leads to excessively long update set commits.

## Dictionary changes

Using update sets help to prevent you from applying dictionary changes that result in data loss. For example, blocked dictionary changes include removing tables or changing a column data type.

Update sets don’t track the removal of tables from the system dictionary. You must manually remove tables from the target instance. While update sets track data type changes, the target instance skips any change that results in data loss and instead adds a log message about the action. You can use the log to make data type changes on the target instance.

**Note:** Update set previews don't detect type mismatches when changes could cause data loss. If you delete a table column via update sets, any existing data in that column is lost when the update is committed. A warning appears noting which deletions result in data loss.

## Home pages and content pages

Home pages and content pages aren’t added to update sets by default. Add pages to the current update set by unloading them.

**Important:**

The functionality found in homepages, arranging information from your instance to tell a story about your data, is found in dashboards on new instances. On upgraded instances with Next Experience enabled, users can view existing homepages if they have a direct URL, but they can't create or edit them. Responsive dashboards and Analytics Overview dashboards take over homepage functionality.

Use the Homepage deprecation help tool to convert the homepages on your instance to responsive dashboards.

For more information, see:

-   Dashboards in the Analytics Center.
-   Working with responsive dashboards.

## Application changes

The system creates a separate update set for each application that only contains changes associated with the application. This separation verifies that access settings for each application are properly evaluated and applied when committing update set changes.

**Parent Topic:**[Update sets reference](update-sets-reference.md)

