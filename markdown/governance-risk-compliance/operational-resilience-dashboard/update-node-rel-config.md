---
title: Configure the Node relationship configurations
description: Create a Node relationship configuration record to establish relationships between nodes. Update the node relationships including source table, both Configuration Items \(CI\) and non-CI relationships. The Node relationship configurations define the connections between the source table and other tables \(target tables\), specifying how they are related.
locale: en-US
release: yokohama
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure the Main node configurations, Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Configure the Node relationship configurations

Create a Node relationship configuration record to establish relationships between nodes. Update the node relationships including source table, both Configuration Items \(CI\) and non-CI relationships. The Node relationship configurations define the connections between the source table and other tables \(target tables\), specifying how they are related.

## Before you begin

Role required: sn\_oper\_res.admin

## Procedure

1.  Navigate to **All** &gt; **Data Relationships Framework** &gt; **Main node configuration**.

2.  Open the desired Main node configuration from the list.

    The following example shows the Main node configurations available in the instance.

    ![List.](../image/service-to-dep-from-list.png)

3.  To add a Node relationship configuration, select **New** in the Node relationship configurations related list.

    The Node relationship configuration form is displayed.

    ![Record.](../image/node-rel-config-new-record.png)

    For description of the fields in the Node relationship configuration form, see [Node relationship configuration form](../reference/node-relationship-configuration-form.md).

    You can set up these relationship registries by creating a Relationship Registry record in the Relationship Registries module. The Relationship Registry new record form is shown in the example.

    ![Rel regisry record.](../../grc-common/image/rela-registry-record-new.png)

    For the description of the fields in the Relationship registry form, see [Relationship registry record form](../reference/rel-registry-record-form.md).

4.  Select the table of your choice in the **Source table** field in the **Source** tab.

    ![Source table.](../image/node-rel-src-table.png)

    By default, the system auto-selects the table listed in the Main configuration record, the Service \[cmdb\_ci\_service\] table in this example. You can choose the auto-suggested table or a different table as per your requirements.

5.  Select the relationship registry record in the **Relationship registry** field in the **Relationship** tab.

    The relationship registry record defines how the Source table links to another table.

    1.  Select the **Search** icon and select the Relationship registry record from the available list.

        ![Relationship tab.](../image/node-rel-conf-rel-tab.png)

        Selecting the search icon shows the out-of-the-box Relationship registries that have Service as the source table. You can select a Relationship registry from the list.

    2.  To select a new registry record instead of choosing a record from the out-of-the-box list, select **New**.

        ![New relationship registry.](../image/node-rel-conf-rel-tab-new.png)

        You can create a new registry record if the out-of-the-box options do not meet your needs.

    3.  Add a meaningful name for the new Relationship registry record.

        You can add a proper name to avoid confusion because there might be other registries with the same name.

    4.  Select the relationship table in the **Table** field.

        The table should be the same as the Source table from the previous screen. This table name may be different from the table that you have defined in the Main node configuration record.

    5.  Select the relationship type for the table in the **Relationship type** field.

        Once the table is selected, the following options are displayed in the drop-down.

        1.  **One-to-one**
        2.  **One-to-many**
        3.  **Many-to-many**
        4.  **Scripted relationship**
        Based on the selected drop-down value, a different list of tables is displayed in the **Relationship** field.

    6.  Select the relationship table in the **Relationship table** field.

        For One-to-one relationship type, the **Relationship** field shows the list of tables that are used as reference fields in the Source table.

        The table name is populated in the **Relationship** field.

        ![Table.](../image/rel-reg-table.png)

    7.  Select **Submit**.

        You have configured the Source table and Relationship registry.

        ![Registry.](../image/rel-tab-rel-registry.png)

        To select the target table, configure the Target section in the Node relationship configuration record in the next step.

        ![Target fields.](../image/node-rel-target-fields.png)

6.  Configure the **Target** tab.

    All the relationship options are explained in this step.

<table id="choicetable_vzr_ppt_1gc"><thead><tr><th align="left" id="d203934e335">

Step

</th><th align="left" id="d203934e338">

Description

</th></tr></thead><tbody><tr><td id="d203934e344">

**One-to-one**

</td><td>

For non-m2m tables, in the **Target** tab, select **Sys ID** as the **Target reference field** and choose the Relationship table as the **Target table**.

This is valid for One-to-one and One-to-many types.

![Target.](../image/node-rel-target.png)

</td></tr><tr><td id="d203934e373">

**One-to-many**

</td><td>

If the Relationship table is an m2m table, select **Sys ID** in the **Target reference field** and then in **Target table**, select the same table as the **Relationship table**.

![One-to-many.](../image/one-to-many.png)For One-to-many, the relationship shows the list of tables that has source table as a reference field.

</td></tr><tr><td id="d203934e402">

**Many-to-many**

</td><td>

For Many-to-many, the **Relationship** field shows the list of m2m tables in which the source table is referred. Notice that for Many-to-many, you have to select the field from the drop-down that you want as output. For example, \[cmdb\_rel\_ci\] table has **Parent** \(cmdb\_ci\) and **Child** \(cmdb\_ci\) fields. If you want to find the child service, you can select **Child**.![Many-to-many.](../image/many-to-many.png)

</td></tr><tr><td id="d203934e431">

**Scripted**

</td><td>

For the Scripted relationship, you can select the record from sys\_relationship. You can define the relationship via script.

![Script.](../image/scripted.png)![Updated script.](../image/scripted-2.png)As you can see, the **Applies to** table has to be as same as the **Table** field from the previous screen. Here the value in **Table** field is \[cmdb\_ci\_service\_business\] but in the **Relationship** field, it is \[cmdb\_ci\_service\]. This configuration works because the \[cmdb\_ci\_service\_business\] table extends to the \[cmdb\_ci\_service\] table.

</td></tr></tbody>
</table>7.  Select **Submit**.

    The Node relationship configuration for the Main configuration record is now updated. The example shows the Node relationship configuration for the **Service to Dependencies** Main configuration record.

    ![Services to Dependencies.](../image/ser-to-dep-main-node-config.png)


