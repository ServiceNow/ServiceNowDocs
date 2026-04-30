---
title: Sample Services to dependencies configuration
description: Create a Services to dependencies sample Main node configuration record for linking services to dependencies.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Sample Services to dependencies configuration

Create a Services to dependencies sample Main node configuration record for linking services to dependencies.

## Before you begin

Role required: sn\_oper\_res.admin

## About this task

For the configuration sequence and instructions in Operational Resilience, see [Configuring Operational Resilience](../concept/configure-operational-resilience.md).

For instructions on creating the Main node configuration records, see [Configure the Main node configurations](set-up-main-node.md).

## Procedure

1.  Download the Operational Resilience application in your instance.

    For instructions on downloading the Operational Resilience application, see [Install Operational Resilience application](download-opres.md).

2.  Ensure that you have set up the pillars, entity types, entity filters and entities are generated.

    Refer to the configuration instructions on the [Configuring Operational Resilience](../concept/configure-operational-resilience.md) page.

3.  Ensure that you have the Data Relationships Framework application, which is available by default, is available in your instance.

    Ensure that you have completed other pre-requisites listed in the [Configure the Main node configurations](set-up-main-node.md).

4.  Navigate to **All** &gt; **Data Relationships Framework** &gt; **Main node configurations**.

    **Note:** In order for the Main node configuration to be picked up by the scheduled job, its source should be **OpRes CMDB** and its status should be **True** \(**Active**\).

5.  To create a new Main configuration record, select **New**.

    For descriptions of all the fields in the form, see [Main node configuration form](../reference/main-node-config-form.md).

6.  Add the name for the configuration as **Service to Dependencies**.

7.  To use it in the Operational Resilience scheduled job, select the source as **OpRes CMDB** and set the status to **True**.

8.  Select the table from where you want the hierarchy to start, for example, Service.

9.  Add conditions to filter the records for which this main node definition is created.

    The following example shows the filter condition for the **Service to Dependencies** configuration.

    ![Service to dependency"configuration.](../image/ser-to-dep-main-node.png)

10. Select **Submit**.

    The **Service to Dependencies** Main node configuration is created and displayed in the Main node configurations list.

    ![List.](../image/service-to-dep-from-list.png)

11. To define the node relationships, open the **Service to Dependencies** Main node configuration record and select **New** in the Node relationship configurations.

    The Node relationship configuration new record is displayed.

    ![Record.](../image/node-rel-config-new-record.png)

    For description of the fields, see [Relationship registry record form](../reference/rel-registry-record-form.md).

12. Select the table of your choice in the **Source table** field in the **Source** tab.

    ![Source table.](../image/node-rel-src-table.png)

    By default, the system auto-selects the table listed in the Main configuration record, the Service \[cmdb\_ci\_service\] table in this example. You can choose the auto-suggested table or a different table as per your requirements.

13. Select the relationship registry record in the **Relationship registry** field in the **Relationship** tab.

    The relationship registry record defines how the Source table links to another table.

    1.  Select the **Search** icon and select the Relationship registry record from the available list.

        ![Relationship tab.](../image/node-rel-conf-rel-tab.png)

        Selecting the search icon shows the out-of-the-box Relationship registries that have Service as the source table. You can select a Relationship registry from the list.

    2.  To select a new registry record instead of choosing a record from the out-of-the-box list, select **New**.

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
        Based on the selected drop-down value, a different list of tables is displayed in the **Relationship** field. The **One-to-one** option is considered in this example.

    6.  Select the relationship table in the **Relationship table** field.

        For One-to-one relationship type, the **Relationship** field shows the list of tables that are used as reference fields in the Source table.

        ![Table.](../image/rel-reg-table.png)

        After you select the relationship table, the table name is populated in the **Relationship** field.

    7.  Select **Submit**.

        You have configured the Source table and Relationship registry.

        ![Registry.](../image/rel-tab-rel-registry.png)

        You can configure the Target section in the Node relationship configuration record in the next step.

        ![Target fields.](../image/node-rel-target-fields.png)

14. For non-m2m tables, in the **Target** tab, select **Sys ID** as the **Target reference field** and choose the Relationship table as the **Target table**.

    The Target table and Target reference field are shown in the example.

    ![Target.](../image/node-rel-target.png)

15. Select **Submit**.

    The Node relationship configuration for the **Service to Dependencies** Main configuration record is now updated.

    ![Services to Dependencies.](../image/ser-to-dep-main-node-config.png)


