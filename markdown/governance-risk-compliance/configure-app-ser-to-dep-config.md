---
title: Sample Application service to dependencies configuration
description: Create an Application service to dependencies sample Main node configuration record for linking an application service to the dependencies.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Sample Application service to dependencies configuration

Create an Application service to dependencies sample Main node configuration record for linking an application service to the dependencies.

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

6.  Add the name for the configuration as **Application service to dependencies**.

7.  To use it in the Operational Resilience scheduled job, select the source as **OpRes CMDB** and set the status to **True**.

8.  Select the table from where you want the hierarchy to start, for example, Application Service \[cmdb\_ci\_service\_auto\].

9.  Add conditions to filter the records for which this main node configuration is created.

    This is an optional step.

    The **Application service to dependencies** Main node configuration is shown in the example.

    ![Application service to dependencies.](../image/app-ser-to-dep-main-node.png)

10. Select **Submit**.

    The **Application service to dependencies** Main node configuration is created and displayed in the Main node configurations list.

    ![List.](../image/app-ser-to-dep-list.png)

11. To define the node relationships for the **Application service to dependencies** Main node configuration, open the record from the list and select **New** in the Node relationship configurations.

    The Node relationship configuration new record is displayed.

    ![New.](../image/app-ser-to-dep-new.png)

    For the description of the fields, see [Relationship registry record form](../reference/rel-registry-record-form.md).

12. Select the table of your choice in the **Source table** field in the **Source** tab.

    By default, the system auto-selects the table listed in the Main configuration record, for example, Application Service \[cmdb\_ci\_service\_auto\]. You can choose the auto-suggested table or a different table as per your requirements.

13. Select the relationship registry record in the **Relationship registry** field in the **Relationship** tab.

    The relationship registry record defines how the Source table links to another table.

    1.  Select the **Search** icon and select the Relationship registry record from the available list.

        Selecting the search icon shows the out-of-the-box Relationship registries that have Service as the source table. You can select a Relationship registry from the list.

        ![Record.](../image/app-ser-rel-reg.png)

        You can also create a new registry record if the out-of-the-box options do not meet your needs.

    2.  Add a meaningful name for the new Relationship registry record.

        You can add a proper name to avoid confusion because there might be other registries with the same name.

    3.  Select the relationship table in the **Table** field.

        The table should be the same as the Source table from the previous screen. This table name may be different from the table that you have defined in the Main node configuration record.

    4.  Select the relationship type for the table in the **Relationship type** field.

        Once the table is selected, the following options are displayed in the drop-down.

        1.  **One-to-one**
        2.  **One-to-many**
        3.  **Many-to-many**
        4.  **Scripted relationship**
        Based on the selected drop-down value, a different list of tables is displayed in the **Relationship** field. The **One-to-one** option is shown in this example.

    5.  Select the relationship table in the **Relationship table** field.

        ![Relationship.](../image/app-ser-to-dep-src-target.png)

        After you select the relationship table, the table name is populated in the **Relationship** field.

14. Select the **Target table** in the **Target** tab.

    The Target table and Target reference field are shown in the example.

    ![Contract.](../image/app-ser-contract-table.png)![Target.](../image/app-ser-target.png)

15. Select **Submit**.

    The Node relationship configuration for the **Application service to dependencies** Main configuration record is now updated.

    ![Added.](../image/app-ser-to-dep-added.png)


