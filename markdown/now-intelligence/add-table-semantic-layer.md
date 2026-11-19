---
title: Add a table to the semantic data layer
description: Add more tables to the Query Generation semantic layer so that users can use ServiceNow Otto for Platform Analytics applications to ask questions about the data in those tables.Instead of adding individual tables or database views to the semantic layer, you can select multiple ones from a list and enable Query Generation for them together.Several extra requirements have to be kept in mind when you add a Workflow Data Fabric table to the semantic layer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/now-intelligence/add-table-semantic-layer.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [semantic table configuration, query generation, AI data explorer, workflow data fabric, WDF, batch add tables semantic table config, bulk add tables semantic table config]
breadcrumb: [Configure, Query Generation, ServiceNow Otto for Platform Analytics, Platform Analytics]
---

# Add a table to the semantic data layer

Add more tables to the Query Generation semantic layer so that users can use ServiceNow Otto for Platform Analytics applications to ask questions about the data in those tables.

## Before you begin

\[Omitted video\] Description: Adding a table to the semantic data layer

Role required: sn\_query\_gen.admin or higher

## About this task

Semantic table configuration supports regular tables, database views, and Workflow Data Fabric tables \(df\_\*, table\_type = REMOTE\).

**Warning:**

-   Adding a table to the semantic data layer and enabling semantic generation on that table can negatively impact both initial load time and runtime performance of Query Generation.
-   All tables that are addressed by a query must be listed in the semantic table configuration, including tables in any multi-table relationship.

## Procedure

1.  Navigate to **All** &gt; **Query Generation** &gt; **Administration** &gt; **Semantic table config**.

    If you do not have this navigation path despite having the correct roles, you may be missing a required entitlement.

    **Note:** As an alternative to this procedure, you can select one or more tables in a list and apply the Enable for Query Generation list action.

    \[Omitted image "enable-qg-from-list-of-tables.png"\] Alt text: The Enable for query generation action for tables in a list of tables.

2.  In the Semantic Tables Configurations list, select **New**.

3.  Set your session application scope to be the same as the scope you want for the table.

    **Important:** To add a database view, you must select the same scope as that database view.

4.  Select a table from the **Table Name** list.

    Workflow Data Fabric \(WDF\) table names begin `df_*` and are listed under Remote Tables.

5.  Select whether to enable semantic generation for the table.

    By default, semantic generation is enabled. It must be enabled for WDF tables. For more information, see [Enable semantic generation for tables in the semantic layer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/enable-semantics-generation.md).

6.  Select whether to include the hierarchy of child tables.

    By default, child hierarchies are included. However, they are not relevant for WDF tables.

7.  Select **Submit**.


## Result

Your table is added to the list. If you enabled semantic generation, records for the table and its child tables, if included, are generated in the Entities \[sn\_query\_gen\_entities\] table. Records for the table columns are generated in the Dimensions \[sn\_query\_gen\_dimensions\] table.

## Adding the Contract table hierarchy to the semantic layer

If you have users who need to explore and discuss data relating to asset contracts, add the Contract \[ast\_contract\] table to the semantic layer. This table hierarchy is not supported by default.

1.  First, you open the Semantic Table Configuration list \[sn\_query\_gen\_table\_config\_list\] and press the **New** button.

    \[Omitted image "qgen-stg-list.png"\] Alt text: Semantic Table Generation list showing where to open it in Navigator and the New button.

2.  Now you are in the form for creating a new Semantic Table Configuration record. You search for the Contract \[ast\_contract\] table and select it.

    \[Omitted image "qgen-stc-new-table.png"\] Alt text: Selecting the Contract table in a new Semantic Table Configuration record.

3.  You want to enable semantic generation on the entire Contract table hierarchy, so you leave the **Enable Semantic Generation** and **Include Child Hierarchy** checkboxes selected and press **Submit**.

    \[Omitted image "qgen-new-form-filled.png"\] Alt text: The completed new record form for adding the Contract table to Semantic Table Configuration, ready to be submitted.

4.  You see that the Contract \[ast\_contract\] table has been added to the Semantic Table Configurations table, and that semantic generation is enabled on its hierarchy.

    \[Omitted image "qgen-ast-contract-added-stc.png"\] Alt text: The Semantic Table Configurations list showing the newly added ast\_contract table.

5.  When you open the Entities list \[sn\_query\_gen\_entity\_list\], you see that the Contract table and all its children are represented by Entity records, and all the records are active.

    \[Omitted image "qgen-contract-entities.png"\] Alt text: Entities added for the Contract table hierarchy.

6.  Looking in the Dimensions list \[sn\_query\_gen\_dimension\_list\], you see that many columns of the Contract table are represented, and you are confident that you have successfully added the table hierarchy to the semantic layer.

    \[Omitted image "qgen-contract-dimensions.png"\] Alt text: Dimensions added for the Contract table.


**Parent Topic:**[Configuring Query Generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/configuring-query-generation.md)

## Add a batch of tables to the semantic layer

Instead of adding individual tables or database views to the semantic layer, you can select multiple ones from a list and enable Query Generation for them together.

### Before you begin

Role required: admin, now\_assist\_explorer\_admin, sn\_query\_gen.admin

### Procedure

1.  Navigate to the Tables list \[sys\_db\_object\_list\], the Database Views list \[sys\_db\_view\_list\], or a subset of one of those lists, such as Remote Tables.

2.  Set your session application scope, which will be reflected in the scopes of the Semantic Table Configuration records you create.

    **Important:** To add a database view, you must select the same application scope as that database view.

3.  Select the checkboxes for the desired tables or database views.

    \[Omitted image "selected-tables.png"\] Alt text: Selected tables from a list.

4.  Expand **Actions on selected rows...**

5.  Select **Enable for Query Generation**.

    \[Omitted image "querygen-enable-action-tables.png"\] Alt text: The Enable Query Generation action on a list of tables.

    When successful, a banner says `Selected tables have been successfully added to Query Generation semantic layer. View`.

6.  Select **View** to see a list of the tables or database views you just added to Semantic Table Configurations.

    You can disable semantic generation for any of the tables/database views or add support for their child hierarchies. You can also remove the tables/database views from Semantic Table Configurations.


## Additional points for Workflow Data Fabric tables

Several extra requirements have to be kept in mind when you add a Workflow Data Fabric table to the semantic layer.

The semantic layer supports Workflow Data Fabric \(WDF\) tables.

-   The tables are listed in the Table \[sys\_db\_object\] table, with names beginning `df_*` and the table type REMOTE.
-   Child Hierarchies do not apply to WDF tables.
-   Semantic generation must be enabled on the Semantic Table Config record.
-   Every WDF table has a generated read role. Find this role in the Roles \[x\_snc\_plugin\_reque\_plugin\_role\] table and grant it to the appropriate users. Users without this role see "No Access" in AI Data Explorer, or Query Generation silently answers from an unrelated table.
-   To enable extended analysis for WDF tables, the system property **sn\_query\_gen.hidden.insights.wdf.enabled** must be created and set to `true`.
-   In the response metadata for WDF answers, `additionalMetadata.entitySourceType / entitySourceLabel / entityType = remote_table`. The **View Source** label relies on this metadata.

### Limitations of Workflow Data Fabric tables in the semantic layer

-   There can be routing ambiguity when a Glide table exists with a similar name to the WDF table.
-   Some query shapes are not supported for remote tables.

