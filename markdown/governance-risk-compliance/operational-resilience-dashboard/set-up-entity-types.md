---
title: Configure entity types and entity filters
description: Configure the entity type and entity filter using the Core UI \(UI16\) view in the Operational Resilience application. IT enables you to define the relevant data for your business entity.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Set up pillars, entity types, and generate entities, Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Configure entity types and entity filters

Configure the entity type and entity filter using the Core UI \(UI16\) view in the Operational Resilience application. IT enables you to define the relevant data for your business entity.

## Before you begin

Role required: sn\_oper\_res.admin

## About this task

**Note:** If you have set up the entity types and pillars from the Workspace view in the earlier step \([Set up pillars, entity types, and generate entities](manage-entity-types-pillars-from-ws.md)\), you can ignore this step and proceed to [Main node configurations: A component of the Data Relationships Framework](../concept/main-node-relationship-fw.md).

An entity in Governance, Risk, and Compliance can be a person, a process, a department, an application, or an object. An entity type in Governance, Risk, and Compliance is a group of the entities that have similar attributes.

The entity type form in the Operational Resilience application is pre-configured with an entity filter that defines the data for an entity.

You can use the pre-defined entity types that are provided with the base system or you can create an entity type depending on your business requirement. You can operate Operational Resilience by using these entity types as shipped, edit them as needed, or create entity types.

To create an entity from an existing record, select the **Add to OpRes reporting** UI action, which adds the entity record to the entity type.

**Note:** As an Operational Resilience administrator, you must perform the following tasks:

1.  Activate the necessary entity types.
2.  Activate the necessary entity filters.
3.  Create new or update the existing pillars and entity types.
4.  Generate entities based on the setup.

The Operational Resilience managers cannot create the entity types, but they can update the entity types.

## Procedure

1.  Navigate to **All** &gt; **Operational Resilience** &gt; **Admin** &gt; **Entity Types**.

    Beginning with Release 20.1.x, the following entity types have been added in the tables:

    -   Application Service
    -   Service Offering
    -   Business Services
    -   Data
2.  Select the **Name** of an entity type record and view its details.

    In entity types, a combination of entity filters is used for selecting the entities into the entity types. By default, all entity types and entity filters are inactive in the application. You can activate the entity types and entity filters based on your needs.

    **Note:** The default entity types are used to pull data into the pillars of the application.

3.  To update the filter condition, select the Entity Filters related list and select **Build your own conditions**.

    The Entity Filters related list and the **Build your own conditions** option are shown in the example.

    ![related list.](../image/ent-type-ent-filter-rel-list.png)![Condition.](../image/ent-filter-build-condition.png)

    The entity filter is used to define the table from which data is pulled into each entity type for display in the Operational Resilience application. The filter condition requires that the service classification field is set to "business service and operation," and the operational status of the service is "operational." These conditions determine whether an entity type can have any entity records.

4.  To use a predefined query instead of building your own conditions, choose the **Select from predefined queries** option in the **Entity filter type** field and select **Save**.

    ![Predefined query.](../image/ent-filter-predefined-query.png)

5.  Check the Entity filter related list in the form for Business Service and Application Service Entity types.

    You can verify that the selected filters are applied to the entities.

6.  To create an entity type, return to the Entity Types screen, and select **New**.

7.  On the form, fill in the fields.

    For a description of the field values, see [Entity Type New record form](../reference/entity-type-reference.md).

8.  Select **Submit**.

    The newly defined entity type is listed in the Entity Types screen.

9.  To activate entity filters directly from the entity filters page, complete the following steps.

    1.  Select and hold \(or right-click\) on the page header in the Entity Filter record and select **Configure &gt; Form Layout**.

        ![Form layout.](../image/ent-fil-conf-form-layout.png)

        If you see the option to try the Form Builder, you can select **Not now**.

        ![Option.](../image/ent-fil-form-builder.png)

        You can select **Edit this section** in the "Configuring Entity Filter" form so that the picker list is displayed.

        ![Edit.](../image/ent-fil-edit-section.png)

    2.  From the "Available" selection list on the left, select **Active** and use the right arrow to shift it to the "Selected" list.

        ![Selected.](../image/ent-fil-active-field-selected.png)

    3.  Select **Save**.

        On the Entity Filter page, a check box with the Active label is displayed.

    4.  To activate the Entity filter, select the **Active** check box.

        ![Activate the Entity filter.](../image/ent-fil-active-field-on-form.png)

        Once this change is made for one entity filter, all the other records within the Entity filters list have the Active option set to **True** by default.


## What to do next

Set up the main node configurations so that Configuration Management Database \(CMDB\) data can be fetched into Operational Resilience for reporting. For more information, see [Main node configurations: A component of the Data Relationships Framework](../concept/main-node-relationship-fw.md).

