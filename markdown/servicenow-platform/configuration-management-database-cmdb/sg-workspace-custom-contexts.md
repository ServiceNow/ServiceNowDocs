---
title: Customize data exploration contexts in Service Graph Workspace
description: Customize the default navigation contexts that are used for exploring CMDB data in the Explore and Search view in Service Graph Workspace, by adding contexts that are relevant in your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/sg-workspace-custom-contexts.html
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-05-29"
reading_time_minutes: 5
breadcrumb: [Configure, Service Graph Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Customize data exploration contexts in Service Graph Workspace

Customize the default navigation contexts that are used for exploring CMDB data in the Explore and Search view in Service Graph Workspace, by adding contexts that are relevant in your organization.

## About this task

A context-based hierarchy provides the navigation for exploring CMDB data in the Explore and Search view in Service Graph Workspace. The contexts and their associated classes in that navigation, are based on default definitions. You can add contexts to customize the exploration experience, to reflect on specific data in the CMDB in your organization. Typically, there is a parent context that is the entry item in the navigation, which expands a child context entry that further expands to a list of tables to explore. For more information about exploring CMDB data, see [Explore and Search view in Service Graph Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-search-explore-view.md).

The contexts hierarchy can be two or more levels deep. The child context which doesn't expand further to any context is the leaf-context. When selecting the leaf-context, the tables associated with that context, appear.

You can associate customizations of the contexts navigation hierarchy with the configuration identifiers framework to make those customizations available for use with other workspaces. For more information, see [Configuration identifiers framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cnfg-identifiers-framework-sg.md).

## Before you begin

The Service Graph Workspace - Content store app and its dependent app, Data Model Navigator, must be installed to enable the **Explore by contexts** option. To add or modify contexts, you must use the following tables:

-   Model Context \[sn\_data\_model\_nav\_model\_context\]
-   Model Context to Model Contexts \[sn\_data\_model\_nav\_model\_context\_to\_context\]
-   Model Tables \[sn\_data\_model\_nav\_model\_table\]
-   Model Table To Model Contexts \[sn\_data\_model\_nav\_model\_table\_to\_context\]
-   Workspace Configuration to Model Context Mapping \[sn\_cmdb\_ws\_config\_model\_context\_m2m\]
-   Model Table Field Mapping \[sn\_cmdb\_ws\_model\_table\_field\_mapping\]

The Data Model Navigator store app tables \(\[sn\_data\_model\_nav\*\]\) define the hierarchical structure of contexts and tables, and the CMDB Workspace tables \(\[sn\_cmdb\_ws\*\]\) control visibility, filtering, and appearance behavior within the Explore tab. For more information about the Data Model Navigator store app, see [Data Model Navigator app features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/data-model-navigator-app-ref.md).

Role required: sn\_data\_model\_nav.data\_model\_navigator\_write \(write access to the Data Model Navigator store app tables\), and sn\_cmdb\_ws.config\_editor or sn\_cmdb\_admin \(write access to the CMDB Workspace tables\)

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Graph Workspace**, in the navigation panel select the Explore and Search icon and then select **Explore by contexts** in the Explore tab.

    Examine the navigation panel that is based on the default definitions of the contexts hierarchy \(unless it's already modified\) before updating.

2.  Select **All** and then, in the navigation filter, enter `sn_data_model_nav_model_context.list` to open the Model Context table and create a record for each context that you want to add.

    For example, create a parent context named `Software Service` and a child context named `Saas`.

    1.  On the Model Context table form, select **New**.

    2.  Set **Name** to the name of the context, such as `Software Service` or `SaaS`, and enter a **Description**.

    3.  Select **Submit**.

3.  Select **All** and then, in the navigation filter, enter `sn_data_model_nav_model_context_to_context.list` to open the Model Context to Model Contexts table and define the parent-to-child relationships between the contexts.

    1.  On the Model Context to Model Contexts table form, select **New**.

    2.  On the new record form, set **Parent Context** to a context that will be the parent in the relationship, such as `Software Service`.

    3.  Set **Child Context** to a context that will be the child in the relationship, such as `SaaS`.

    4.  Select **Submit**.

4.  Select **All** and then, in the navigation filter, enter `sn_data_model_nav_model_table.list` to open the Model Tables table to create records for each table that you want to use in the contexts hierarchy.

    1.  Select **New**.

    2.  On the new record form, set **Table** to a table that you want to associate with a context.

    3.  Select **Submit**.

5.  Select **All** and then, in the navigation filter, enter `sn_data_model_nav_model_table_to_context.list` to open the Model Table To Model Contexts table to associate tables to a leaf-context.

    1.  Select **New**.

    2.  On the new record form, set **Context** to a leaf-context such as `SaaS`, and set **Table** to a table record such as `cmdb_ci_business_capability`.

    3.  Select **Submit**.

    Alternatively, you can associate multiple tables to the leaf-context:

    1.  Open the Model Context to Model Contexts \[sn\_data\_model\_nav\_model\_context\_to\_context\] table.

    2.  In the table list view, locate the record for the parent context and then, select the link in the Child Context column of that record.
    3.  Select the Tables tab in the related items section on the child record form.
    4.  Select **Edit**.
    5.  Add one or more tables to Tables List.
    6.  Select **Save**.
6.  Select **All** and then, in the navigation filter, enter `sn_cmdb_ws_config_model_context_m2m.list` to open the Workspace Configuration to Model Context Mapping table form to make the top-level context visible and to associate the new context with the CMDB Workspace config identifier framework.

    1.  Select **New**.

    2.  On the new record form, set **CMDB Model Context** to the new parent context \(such as `Software Service`\).

    3.  Set **Config Identifier** to `Default`.

    4.  Select **Submit**.

7.  Select **All** and then, in the navigation filter, enter `sn_cmdb_ws_model_table_field_mapping.list` to open the Model Table Field Mapping table to configure filter fields and conditions for each table that is associated with a leaf-context.

    1.  Select **New**.

    2.  Set **Model table** to the table that is associated with the context, such as `cmdb_ci_business_app`.

    3.  Set **Filter fields** to the list of fields to show when exploring this context.

    4.  Configure **Conditions** to filter the table by when exploring this context.

    5.  Select **Submit**.


## Result

When exploring CMDB data in the Explore and Search view in Service Graph Workspace, the new context structure appears in the navigation panel, and when selecting the leaf-context, records from associated tables appear, filtered as specified.

