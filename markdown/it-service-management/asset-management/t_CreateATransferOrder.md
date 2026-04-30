---
title: Create a transfer order for Asset Management
description: Create a transfer order in order to transfer assets from one location to the other.Transfer order lines specify the exact items that comprise a transfer order.Create customized template tasks to configure your specific task workflow for transfer order lines. Default template tasks are available with the Asset Management application. You can’t modify or delete a default template task.Create template subtasks to add granularity to the transfer order line tasks. For example, before preparing for shipment, for a computer, you may want to create sub tasks for imaging the computer or adding additional software.
locale: en-US
release: xanadu
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Asset Management, IT Service Management]
---

# Create a transfer order for Asset Management

Create a transfer order in order to transfer assets from one location to the other.

## Before you begin

Role required: inventory\_user

## Procedure

1.  Navigate to **All** &gt; **Inventory Management** &gt; **Transfer Orders** &gt; **Create Transfer Order**.

2.  Click the **From stockroom** list to select a stockroom from which the item\(s\) is to be shipped.

3.  Click the **To stockroom** list to select a stockroom where the item\(s\) is to be shipped.

4.  Click **Submit**.

    Once the transfer order is created, you can create transfer order lines to specify the items that the transfer order comprises of. See [Create a transfer order line](t_CreateATransferOrder.md#) .


**Parent Topic:**[Asset Management](../concept/c_AssetManagement.md)

## Create a transfer order line

Transfer order lines specify the exact items that comprise a transfer order.

### Before you begin

Role required: inventory\_user

### About this task

A transfer order can contain one or more transfer order lines. Under a single transfer order, all transfer order lines will have the same From location and To location. Each line contains an asset to transfer and the quantity to transfer. The item to transfer is identified by asset name and model name. A transfer order line can involve one quantity of a non-consumable asset or multiple quantities of a consumable asset. A bundled model can be transferred.

### Procedure

-   After creating a transfer order, click **New** in the **Transfer Order Lines** related list and fill in the fields as appropriate.

    |Field|Description|
    |-----|-----------|
    |Number|Internal unique number identifying the transfer order line.|
    |Transfer Order|The transfer order to which the transfer order line belongs.|
    |Model|Model of the items requested by the transfer order line. For example, a printer. If the Asset field is filled out first, the Model field is automatically filled in with the model corresponding to the asset.|
    |Quantity requested|Number of items requested by the transfer order line. For example, 3 computers are requested to be transferred.|
    |Quantity received|Number of items already received. For example, 3 keyboards are transferred, 2 are received.|
    |Stage|Current stage of the transfer order. Transfer order lines can only be created when a transfer order is in **Draft** stage.|
    |Request line|Requested item to associate with the transfer order line.|
    |Asset|Asset requested by the transfer order line. For example, a specific printer. The asset can filter on stockrooms.|
    |Quantity remaining|Number of items yet to be received. For example, 3 keyboards had been requested, 2 are received, 1 is remaining.|
    |Quantity returned|Number of items that already needed to be returned.|


### Create a customized template task

Create customized template tasks to configure your specific task workflow for transfer order lines. Default template tasks are available with the Asset Management application. You can’t modify or delete a default template task.

#### Before you begin

Role required: inventory\_user

#### About this task

Template tasks help you progress through the various stages of the transfer order line. Custom template tasks are stored in the Custom Template Task \[alm\_custom\_template\_task\] table. The template tasks are based on model categories. For example, when you create a customized template task for the Application model category, whenever a transfer order line is created for the Application model category, the template tasks associated with the Application model category are used as transfer order line tasks. When you create customized template tasks, make a copy of the Transfer Order Line workflow and update the workflow accordingly. For example, if you need only four tasks out of five, you can delete the additional task from the workflow.

**Note:** Two template tasks can’t be created when they’re based on the same model category, the same order number and the same stage. The model category, the order, and the stage have to be unique for each template task. For example, you can’t create two template tasks for Prepare for Shipment, based on the Application model category, order number 200, and the stage as Requested. If you try to create an identical template task as mentioned in the example, an error message is displayed.

#### Procedure

1.  Navigate to **All** &gt; **Inventory** &gt; **Transfer Order Lines** &gt; **Template Tasks**.

    All the default template tasks that are available with the Asset Management application are listed.

2.  Click **New**.

    You can also customize a template task by copying a default template task. Click **Copy Default Template** and select a model category.

3.  Fill out the form fields \(as shown in the table\).

    |Field|Description|
    |-----|-----------|
    |Task name|Name of the template task|
    |Model category|Model category this template task is based on.|
    |Order|Order in which the template task is added to the transfer order line.|
    |Short description|Brief description about this template task.|
    |Next stage|Stage that this template task gets executed.|

4.  Click **Submit**.


### Create a template subtask

Create template subtasks to add granularity to the transfer order line tasks. For example, before preparing for shipment, for a computer, you may want to create sub tasks for imaging the computer or adding additional software.

#### Before you begin

Role required: inventory\_user

#### About this task

The template subtasks that you create are stored in the Template Subtask \[alm\_template\_subtask\] table. When a transfer order line task is created and if subtasks are defined for that transfer order line task, then the subtasks are automatically added to the transfer order line task.

#### Procedure

1.  Navigate to **All** &gt; **Inventory** &gt; **Transfer Order Lines** &gt; **Template Subtasks**.

2.  Click **New** and fill out the form fields \(as shown in the table\).

    |Field|Description|
    |-----|-----------|
    |Short Description|A brief description of the subtask.|
    |Subtask name|A name for the subtask.|
    |Task|The task that this subtask is associated to.|

3.  Click **Submit**.


