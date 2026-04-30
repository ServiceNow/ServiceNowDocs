---
title: Create a service fulfillment step type
description: Expand the coverage of service fulfillment use cases beyond those supported by step types in base system. Using a service fulfillment step type, catalog item owners can define multiple steps that are part of the request fulfilment process.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Setting up the Catalog Builder, Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a service fulfillment step type

Expand the coverage of service fulfillment use cases beyond those supported by step types in base system. Using a service fulfillment step type, catalog item owners can define multiple steps that are part of the request fulfilment process.

## Before you begin

Role required: admin

## About this task

The following step types are available in the base system.

-   Task
-   Custom approval
-   Manager approval

## Procedure

1.  Set up a data store to store information needed for running the step. This information is provided by a catalog item owner while defining the request fulfillment process. Do one of the following.

<table id="choicetable_lxs_24x_jpb"><thead><tr><th align="left" id="d330367e67">

Option

</th><th align="left" id="d330367e70">

Description

</th></tr></thead><tbody><tr><td id="d330367e76">

**When additional input is required from the catalog item owner for a step type**

</td><td>

Create a table by extending the Service Fulfillment Step \[sc\_service\_fulfillment\_step\] table and add fields to store the additional input. For example, to create a step type for email notifications, the email id and body are the additional input provided by the catalog item owner while defining the steps. So, fields for email id and body should be added to the extended table to store the input.**Note:** Ensure that the new table has similar ACLs as that of the Service Fulfillment Step \[sc\_service\_fulfillment\_step\] table.

 **Note:** Ensure that the new table has the canCreate, canUpdate, and canRead application access enabled.

 For tables extending the Service Fulfillment Step \[sc\_service\_fulfillment\_step\] table, the **Domain master** attribute should be added and its value should be set as **service\_fulfillment\_stage**. The domain of a service fulfillment step is then inherited from the catalog item.

</td></tr><tr><td id="d330367e101">

**When no input is required for a step type**

</td><td>

Use the Service Fulfillment Step \[sc\_service\_fulfillment\_step\] base table. For example, a department head approval does not require any additional input from the catalog item owner and does not need a new table.

</td></tr></tbody>
</table>2.  Create a record producer to store the values provided by the catalog item owner to the data store \(base table or extended table\) of that step. For information about creating a record producer, see [Create a record producer](t_DefRecProdInSCat.md).

    **Note:**

    -   The Service Fulfillment Steps - Properties set variable set is automatically added to the record producer and it should not be removed from the record producer.
    -   All additional columns defined in the extended table should have corresponding variables mapped in the record producer.
    -   Configure the Record Producer form to display the **Allow edit** option and **Save Options** field. Also, select the **Allow edit** option and set the value of the **Save Options** field to **Save in Destination**.
    -   Ensure that the record producer is not restricted for the users with catalog\_builder\_editor role.
3.  Create a subflow to perform a sequence of actions by copying the Template: Service Fulfillment Steps subflow and then defining your subflow. For information about subflows, see [Subflows](https://www.servicenow.com/docs/access?context=subflows&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

<table id="table_x2q_phd_jpb"><thead><tr><th>

Parameter

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

requested\_item

</td><td>

Reference

</td><td>

RITM record

</td></tr><tr><td>

service\_fulfillment\_step\_data

</td><td>

Reference

</td><td>

Step data record. Update the state to one of the following values before ending the subflow:-   canceled
-   failed
-   completed


</td></tr><tr><td>

service\_fulfillment\_step

</td><td>

Reference

</td><td>

Step defined on a catalog item. It must refer to a table in which the record producer defined in the step configuration inserts a record.Do not update the step record.

</td></tr></tbody>
</table>    For information about subflow field types, see [Field types](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

4.  Create a step configuration to define the behavior and display of a service fulfillment step type.

    1.  Navigate to **Service Catalog** &gt; **Catalog Administration** &gt; **Service Fulfillment Step Configurations**.

    2.  Click **New**.

    3.  On the form, fill in the fields.

<table id="table_tvl_rlh_jpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the step configuration.

</td></tr><tr><td>

Application

</td><td>

Application scope in which the step configuration is supported.

</td></tr><tr><td>

Active

</td><td>

Option to enable the service fulfillment support for the flow.

</td></tr><tr><td>

Order

</td><td>

Order of the step configuration.Based on the order of step configurations, the corresponding service fulfillment step types are displayed in the list in the **Steps** region of the **Fulfillment** step.

 The step type corresponding to the step configuration with the least order is displayed beside the list and step types for all other step configurations are included in the list based on their order.

 ![order of service fulfillment step types](../image/step-type-order.png "Order of service fulfillment step types")

</td></tr><tr><td>

Hide

</td><td>

Hides the step type corresponding to this step configuration in the list in the **Steps** region of the **Fulfillment** step. No impact on existing steps.

</td></tr><tr><td>

Short description

</td><td>

Description of the step configuration.

</td></tr><tr><td>

Producer

</td><td>

Record producer that creates an instance of the step type in the step’s data store.

</td></tr><tr><td>

Service fulfillment subflow

</td><td>

Subflow triggered during the request fulfillment process.

</td></tr><tr><td>

Dynamic title

</td><td>

Text that should be displayed for the corresponding service fulfillment step in the **Steps** region of the **Fulfillment** step. If you don’t provide any value, the step configuration name is displayed. To display dynamic text, you can include the field name from the step's data store \(base table or the extended table\) where the associated record producer creates a record.

 For example, in the base system, the **Dynamic title** field for the Custom approval step configuration contains the following value:`Approval from ${approval_title}`

 Here, **approval\_title** is the field from the Service Fulfillment Approval Step \[sc\_service\_fulfillment\_approval\_step\] table where the associated record producer, Add custom approval, creates a record.

</td></tr></tbody>
</table>    4.  Click **Submit**.


**Parent Topic:**[Setting up the Catalog Builder](set-up-cat-builder.md)

