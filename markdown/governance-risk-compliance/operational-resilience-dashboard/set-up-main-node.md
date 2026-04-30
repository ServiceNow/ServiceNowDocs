---
title: Configure the Main node configurations
description: Create the Main node configuration record to fetch data into Operational Resilience for reporting. Main node configurations are available with the base system. You can use the existing Main node configurations or create new Main node configurations for your business needs.
locale: en-US
release: yokohama
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Configure the Main node configurations

Create the Main node configuration record to fetch data into Operational Resilience for reporting. Main node configurations are available with the base system. You can use the existing Main node configurations or create new Main node configurations for your business needs.

## Before you begin

Role required: sn\_oper\_res.admin

## About this task

Main node configurations define how your source data is linked, for example, how one table is related to another table.  You can define the relationships in the following ways:

-   **Direct**

    It can be via a direct reference field in either of the table or it can be via an m2m table .

-   **Indirect**

    If the tables are not directly related, you can use scripts to define their relationship. The script option gives you more flexibility. However, for most of the use cases, the direct option serves the purpose.


Before creating the Main node configuration record, ensure that you have completed the following prerequisites:

1.  You can create a new Main node configuration with the sn\_oper\_res.admin role only.
2.  You have completed the configuration set up instructions listed on the [Configuring Operational Resilience](../concept/configure-operational-resilience.md) page.
3.  The Data Relationships Framework \(sn\_grc\_rel\_config\) application is installed in your instance by default.
4.  The entities are generated in Operational Resilience. Only when the entities are generated and the relationships are created in the Main node configurations, CMDB data can be brought into Operational Resilience for reporting.
5.  All Main node configurations with the source as **OpRes CMDB** run in parallel.
6.  To enable reporting, ensure that entities are generated and relationships are established in Main node configurations. Data can only be brought in for reporting after these steps are completed.

## Procedure

1.  Navigate to **All** &gt; **Data Relationships Framework** &gt; **Main node configurations**.

    **Note:** In order for the Main node configuration to be picked up by the scheduled job, its source should be **OpRes CMDB** and its status should be **True** \(**Active**\).

    The base version of Operational Resilience includes the following Main node configurations.

    ![Main node configurations.](../image/main-node-configs.png)

    You can update an existing Main node configuration or set up a brand new configuration in your instance.

2.  To create a new Main configuration record, select **New**.

    ![Config form.](../image/main-node-config-form.png)

    The Main node configuration form is displayed.

3.  On the form, fill in the fields.

    For descriptions of all the fields in the form, see [Main node configuration form](../reference/main-node-config-form.md).

    1.  Add the name for the configuration.

    2.  To use it in the Operational Resilience scheduled job, select the source as **OpRes CMDB** and set the status to **True**.

    3.  Select the table from where you want the hierarchy to start, for example, Service.

        Tables are the starting point of the entire tree structure that is received as an output. The Main node configuration starts with a table, such as \[cmdb\_ci\_service\], to generate a tree structure. It scans the table to create a hierarchy for each record. If you do not want to scan the entire table, and if you have specific business requirements, you can apply filter conditions ensuring that only relevant records are scanned.

    4.  Add conditions to filter the records for which this main node definition is created.

        The following example shows the filter condition for the "Service to dependency" configuration.

        ![Service to dependency"configuration.](../image/ser-to-dep-main-node.png)

        The following example shows the Business service downstream records configuration.

        ![Business service downstream record.](../image/business-ser-downstream-record.png)

    5.  Select **Submit**.

        The Main node configuration is created and displayed in the Main node configurations list.

        ![List.](../image/service-to-dep-from-list.png)

        Based on your Main node configuration settings, data for business services, services, offerings, application services, business processes is brought from CMDB into Operational Resilience.


## What to do next

Specify how the source table is connected to the target table in the Node relationship configurations.

![Node relationships configuration related list.](../image/node-rel-config-rel-list.png)

For details, see [Configure the Node relationship configurations](update-node-rel-config.md).

