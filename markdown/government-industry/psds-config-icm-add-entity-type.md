---
title: Configure entity types in the Investigative Case Management Entity Management workspace
description: Configure the entity type tabs that are displayed in the Entity Management workspace. After you create or modify an entity type, investigators and supervisors can select and add the required entity type through the case form.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Entity Management, Investigative Case Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure entity types in the Investigative Case Management Entity Management workspace

Configure the entity type tabs that are displayed in the Entity Management workspace. After you create or modify an entity type, investigators and supervisors can select and add the required entity type through the case form.

## About this task

By default, Investigative Case Management contains the following entity types:

-   Persons
-   Locations
-   Events
-   Vehicles
-   Properties
-   Firearms
-   Organizations

As an admin, you can add and configure entity types that are displayed in the Entity Management workspace of an investigative case, to create additional labels that more closely align with the types of entities your team regularly handles for investigative cases.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

    UI Builder will open in a separate tab.

2.  In UI Builder, select **Page collections**.

3.  Select and open the **Investigative Record Page Collection**.

    Make sure the list is configured to display the Pages and Variants name column.![](../image/psds-icm-entity-tab-config-name-column.png)

4.  If prompted, select **Edit in original scope**.

5.  Select the name of the entity you wish to configure.

    To add a new one, select the add \(![](../image/plus-icon-2.png)\) icon.

6.  In the content panel, select **Body** &gt; **Generic List – ICM**.

7.  In the Configure panel for the `Generic List – ICM`, select the dropdown for **Card Configuration Section**.

8.  Select **Entity Page Header**, and enter the desired name for the Entity page.

9.  If necessary, update the core table that this entity record maps to by selecting **\[Entity Type\] Core Table**, and entering the desired table in the field.

10. Select **Save**.


## Result

A new entity type table has now been created and is displayed in the Entity Management case workspace alongside existing types. You can add new entities under this table configuration, and link them to existing entities of other categories.

## What to do next

Add an entity to the case using this configuration. For more information on adding an entity to a case, see [Add entities to an investigative case using Investigative Case Management Entity Management](psds-using-icm-add-entities.md#).

