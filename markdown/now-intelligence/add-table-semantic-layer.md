---
title: Add a table to the semantic data layer
description: Add more tables to the Query Generation semantic layer so that users can use Now Assist in Platform Analytics applications to ask questions about the data in those tables.Instead of adding individual tables or database views to the semantic layer, you can select multiple ones from a list and enable Query Generation for them together.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Add a table to the semantic data layer

Add more tables to the Query Generation semantic layer so that users can use Now Assist in Platform Analytics applications to ask questions about the data in those tables.

## Before you begin

Semantic table configuration supports regular tables, database views, and Workflow Data Fabric tables.

**Warning:** Adding a table to the semantic data layer and enabling semantic generation on that table can negatively impact both initial load time and runtime performance of Query Generation.

Role required: sn\_query\_gen.admin or higher

## Procedure

1.  Navigate to **All** &gt; **Query Generation** &gt; **Administration** &gt; **Semantic table config**.

    If you do not have this navigation path despite having the correct roles, you may be missing a required entitlement.

2.  In the Semantic Tables Configurations list, select **New**.

3.  Set your session application scope to be the same as the scope you want for the table.

    **Important:** To add a database view, you must select the same scope as that database view.

4.  Select a table from the **Table Name** list.

5.  Select whether to enable semantic generation for the table.

    By default, semantic generation is enabled. For more information, see [Enable semantic generation for tables in the semantic layer](enable-semantics-generation.md).

6.  Select whether to include the hierarchy of child tables.

    By default, child hierarchies are included.

7.  Select **Submit**.


## Result

Your table is added to the list. If you enabled semantic generation, records for the table and its child tables, if included, are generated in the Entities \[sn\_query\_gen\_entities\] table. Records for the table columns are generated in the Dimensions \[sn\_query\_gen\_dimensions\] table.

## Adding the Contract table hierarchy to the semantic layer

If you have users who need to explore and discuss data relating to asset contracts, you need to add the Contract \[ast\_contract\] table to the semantic layer. This table hierarchy is not supported by default.

1.  First, you open the Semantic Table Configuration list \[sn\_query\_gen\_table\_config\_list\] and press the **New** button.

    ![Semantic Table Generation list showing where to open it in Navigator and the New button.](../image/qgen-stg-list.png)

2.  Now you are in the form for creating a new Semantic Table Configuration record. You search for the Contract \[ast\_contract\] table and select it.

    ![Selecting the Contract table in a new Semantic Table Configuration record.](../image/qgen-stc-new-table.png)

3.  You want to enable semantic generation on the entire Contract table hierarchy, so you leave the **Enable Semantic Generation** and **Include Child Hierarchy** checkboxes selected and press **Submit**.

    ![The completed new record form for adding the Contract table to Semantic Table Configuration, ready to be submitted.](../image/qgen-new-form-filled.png)

4.  You see that the Contract \[ast\_contract\] table has been added to the Semantic Table Configurations table, and that semantic generation is enabled on its hierarchy.

    ![The Semantic Table Configurations list showing the newly added ast_contract table.](../image/qgen-ast-contract-added-stc.png)

5.  When you open the Entities list \[sn\_query\_gen\_entity\_list\], you see that the Contract table and all its children are represented by Entity records, and all the records are active.

    ![Entities added for the Contract table hierarchy.](../image/qgen-contract-entities.png)

6.  Looking in the Dimensions list \[sn\_query\_gen\_dimension\_list\], you see that many columns of the Contract table are represented, and you are confident that you have successfully added the table hierarchy to the semantic layer.

    ![Dimensions added for the Contract table.](../image/qgen-contract-dimensions.png)


**Parent Topic:**[Configuring Query Generation](../concept/configuring-query-generation.md)

## Add a batch of tables to the semantic layer

Instead of adding individual tables or database views to the semantic layer, you can select multiple ones from a list and enable Query Generation for them together.

### Before you begin

Role required: admin, now\_assist\_explorer\_admin, sn\_query\_gen.admin

### Procedure

1.  Navigate to the Tables list \[sys\_db\_object\_list\], the Database Views list \[sys\_db\_view\_list\], or a subset of one of those lists, such as Remote Tables.

2.  Set your session application scope, which will be reflected in the scopes of the Semantic Table Configuration records you create.

    **Important:** To add a database view, you must select the same application scope as that database view.

3.  Select the checkboxes for the desired tables or database views.

    ![Selected tables from a list.](../image/selected-tables.png)

4.  Expand **Actions on selected rows...**

5.  Select **Enable for Query Generation**.

    ![The Enable Query Generation action on a list of tables.](../image/querygen-enable-action-tables.png)

    When successful, a banner says `Selected tables have been successfully added to Query Generation semantic layer. View`.

6.  Select **View** to see a list of the tables or database views you just added to Semantic Table Configurations.

    You can disable semantic generation for any of the tables/database views or add support for their child hierarchies. You can also remove the tables/database views from Semantic Table Configurations.


