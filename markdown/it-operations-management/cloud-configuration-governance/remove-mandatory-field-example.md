---
title: Remove a field from a cloud catalog form
description: Remove a field from the Cloud Provisioning and Governance catalog form when the user belongs to a specific group.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Cloud catalog form configuration examples, Form configuration with blueprints, Cloud Provisioning Blueprints, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Remove a field from a cloud catalog form

Remove a field from the Cloud Provisioning and Governance catalog form when the user belongs to a specific group.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer

Before you can follow this example, you should be familiar with creating blueprints and blueprint rules. See these resources:

-   [Cloud Provisioning Blueprints](../concept/blueprints.md)
-   [Build a Cloud Provisioning blueprint](create-blueprint-cmp.md)
-   [Configure a blueprint rule](configure-a-blueprint-rule.md#)

## About this task

The goal of this example is to hide the Cost Center field on the catalog form when the catalog requester belongs to the Database group. You can follow an example like this one when you want to show or hide catalog item fields based on values in other fields.

## Procedure

1.  Create a blueprint with a virtual server.

    For this example, a blueprint with a virtual server on an AWS datacenter is used.

    ![Virtual server on AWS](../image/blueprint-virtual-server-aws.png)

2.  On the blueprint form, click the **Catalog** tab, and then click the tile that represents the **Provision** operation.

    ![Catalog item](../image/request-operation-catalog-item.png)

3.  Click the **General Info** variable set in the Variable Sets related list.

4.  Click the **CostCenter** variable to open the Cloud Variable form.

5.  Configure the rule that removes the cost center based on the user group:

    1.  In the **Rules** related list, click **New**.

    2.  Fill out the **Name** and description **Fields**.

    3.  Right-click the form header and select **Save**.

6.  Configure the condition that requires the User Group to equal Database:

    1.  In the **Conditions** related list, click **New**.

    2.  On the form, fill in the fields.

        |Field|Value to enter or select|Description|
        |-----|------------------------|-----------|
        |Operand|UserGroup|This value is the User Group field that the user selects.|
        |Operator|--None--|Keep this value **--None--** because this condition is the only condition you need to configure. If you add more conditions, you can select another operator to determine how the system evaluates this condition in relation to the others.|
        |Value|287ee6fea9fe198100ada7950d0b1b73|This value is the Sys ID of the Database user group, which is provided as part of the demo data in your instance. See [Sys ID](https://www.servicenow.com/docs/access?context=c_UniqueRecordIdentifier&version=australia&pubname=australia-platform-administration&ft:locale=en-US) for more information.|

    3.  Click **Submit**.

7.  To understand why the Sys ID of the user group is required for the system, perform these steps:

    1.  Open the blueprint again and click the Provision operation again.

    2.  Click the **General Info** from the **Variable Sets** related list.

    3.  Click the **UserGroup** variable.

        Notice that on the **Type Specifications** tab, the system populates user groups from **UserGroupPool**. The system runs the scripted pool filter named **GroupsUserBelongsTo**.

        ![User Group property](../image/blueprint-user-group-property.png)

    4.  In the Cloud Admin Portal, navigate to **Manage** &gt; **Resource Pools**.

    5.  Find and open **UserGroupPool**.

        Notice that the values for the pool are derived from the table in the **Lookup Table** field, which in this case is the Group \[sys\_user\_group\] table.

        Also notice that there are two queries in the Resource Pool Filters related list:

        -   **All** is a generic query that returns the list of all records from the **Lookup Table**. The value it returns from that table is from the **Lookup Field**, which in this case is the Sys ID. However, the system ignores the **All** query in this case because the scripted query is present.
        -   **GroupsUserBelongsTo** is a scripted query that returns the Sys ID of records in the **Lookup Table**.
        **Important:** When a scripted query is present, the system uses it instead of the generic **ALL** query.

        Both the generic query and the scripted query return the Sys ID of the record in the lookup table. But what is actually happening here is that the system ignores the **All** query and the value specified in the **Lookup Field**, and it uses the **GroupsUserBelongsTo** script.

        ![User group pool](../image/blueprints-usergroup-pool.png "A scripted query")


**Parent Topic:**[Cloud catalog form configuration examples](../concept/example-blueprint-rules.md)

