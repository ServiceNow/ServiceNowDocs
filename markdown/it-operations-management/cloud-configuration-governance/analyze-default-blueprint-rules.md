---
title: Populate the location based on the cloud account
description: This example walks you through an existing set of blueprint rules that Cloud Provisioning and Governance provides by default.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Cloud catalog form configuration examples, Form configuration with blueprints, Cloud Provisioning Blueprints, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Populate the location based on the cloud account

This example walks you through an existing set of blueprint rules that Cloud Provisioning and Governance provides by default.

## Before you begin

Before you can follow this example, you should be familiar with creating blueprints and blueprint rules. See these resources:

-   [Cloud Provisioning Blueprints](../concept/blueprints.md)
-   [Build a Cloud Provisioning blueprint](create-blueprint-cmp.md)
-   [Configure a blueprint rule](configure-a-blueprint-rule.md#)

Role required: sn\_cmp.cloud\_service\_designer

## About this task

The goal of this example is to show you how a default set of blueprint rules accomplishes the task of populating the Location field based on the Cloud Account. Because this example walks you through default data, you do not need to create any records if you are following these steps.

This blueprint, which includes a virtual server that can be provisioned in an AWS datacenter, is used to illustrate the example:

![Virtual server on AWS](../image/blueprint-virtual-server-aws.png)

## Procedure

1.  Open a similar blueprint with a virtual server or similar.

2.  On the blueprint form, click the **Catalog** tab, and then click the tile that represents the **Provision** operation.

    ![Catalog item](../image/request-operation-catalog-item.png)

3.  Click the **General Info** variable set in the Variable Sets related list.

4.  Click the **CloudAccount** variable to open the Cloud Variable form.

    Notice these items:

    -   In the Rules related list at the bottom, two rules are provided:
        -   ReloadLocation reloads the value in the relocation field. This rule runs first because it has a lower order number than the other rule.
        -   TriggerChangeEvent Location tells the system to trigger the actions for the rules that are already configured for the Location variable.
    -   The **Lookup Select Box** field specifies that the Cloud Account field provides a selection for the user to make. The options that the user can select comes from the CloudAccountPool, which is on the **Type Specifications** field.

        ![Cloud account variable](../image/blueprint-cloudaccount-variable.png)

5.  Click the **Reload Location** rule, and then click the **Reload Location** action from the Actions related list.

    Notice these items:

    -   The **Action Type** is **Reload**, which tells the system to reload the catalog item form so that a new value for the field specified in the **Target Variable** \(the **Location**\) can be populated.

        ![Reload location](../image/blueprint-action-reload-location.png)

    -   The **DataSource** field tells the system to reload the location.
    -   The **KeyValues** list, which is only used when you specify a **Reload** action type, specifies that the user is passing in the cloud account via the form. The cloud account is necessary to reload the correct value for the location because the location is loaded from a pool. That pool has a filter that requires the input of the cloud account to return the correct location options.
6.  Navigate back to the CloudAccount catalog property form and open the other rule: **TriggerChangeEvent Location**.

7.  Click the **Actions** related list, open the **TriggerChangeEvent Location** action, and then click the **TriggerChangeEvent Location** action from the Actions related list.

    Notice these items:

    -   The **Action Type** is **TriggerChangeEvent**, which tells the system to trigger the actions for the rules that are already configured for the Location property. By default, several rules are already configured for the Location property. These include rules that reload other fields, like **OS Profile**, **Network**, and so on.

        ![TriggerChangeEvent Location](../image/blueprint-action-triggerchangeeventlocation.png)

    -   No **KeyValues** are required because this action is not a reload action.
    The result of these two rules on the CloudAccount attribute is illustrated in the following example:

    ![Selecting a cloud account to populate the location](../image/blueprint-selecting-cloudaccount.png)

8.  Perform these steps to see why the system populated the value **AWS Datacenter - us-east-1** in the **Location** field and how the system determines which location is related to the **My Cloud Account** value:

    1.  In the same blueprint, open the **General Info** variable set, and then open the **Location** parameter.

    2.  Click the **Type Specifications** tab.

        Notice the values that can be populated for the **Location** field from the **CloudLocationPool** resource pool.

    3.  Navigate to **Manage** &gt; **Resource Pools**, open **CloudLocationPool**, and notice these items:

        ![The Cloud Location pool](../image/cloud-location-pool.png)

        -   The locations come from the records in the **Lookup Table**, which in this example is **Associated Datacenter \[sn\_cmp\_ca\_assc\_datacenter\]**.
        -   The actual value to display to users in the Location field on the catalog item form comes from the **Lookup Field**. In this example, the **Lookup Field** specifies the Alias column from the Associated Datacenter \[sn\_cmp\_ca\_assc\_datacenter\] table. The **Alias** column holds the actual, user-readable names for all locations.
    4.  Go to the standard interface of your instance, not the Admin Portal, and enter `sn_cmp_ca_assc_datacenter.list` in the navigation filter.

        ![Getting the associated datacenters list](../image/assoc-datacenters-list.png)

        The list of datacenters that are already associated with cloud accounts appears.

        ![List of associated datacenters](../image/list-of-associated-datacenters.png)

        Notice that the **My Cloud Account** cloud account is already associated with **AWS Datacenter - us-east-1**, which is the value that the user sees in the Location field. The system knew to display that value because of the association in this Associated Datacenter table. The system created this association when your Cloud Provisioning and Governance administrator created the cloud account for AWS, and then ran discovery on the us-east-1 datacenter in that cloud account.

        It is possible that multiple datacenters could be associated with **My Cloud Account**. In that case, the Location field reloads all the associated datacenters and in the Location field. Since the Location field is of type Select, the field allows the user to select which location to choose.


**Parent Topic:**[Cloud catalog form configuration examples](../concept/example-blueprint-rules.md)

