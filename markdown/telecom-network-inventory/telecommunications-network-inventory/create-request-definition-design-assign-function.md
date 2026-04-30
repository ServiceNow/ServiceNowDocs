---
title: Create a request definition for Design and Assign function
description: Create a request definition and use it to configure the Design and Assign playbook. You can use this request definition to configure an activity for the Design and Assign playbook.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Design and Assign function for your network services, Configuring Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Create a request definition for Design and Assign function

Create a request definition and use it to configure the Design and Assign playbook. You can use this request definition to configure an activity for the Design and Assign playbook.

## Before you begin

Role required: admin, sn\_ni\_core.inventory\_admin

## About this task

You create a request definition and attach the subflow to it. You can use the request definition to configure the activity in the playbook for the Design and Assign function.

## Procedure

1.  Navigate to **All** &gt; **Telecom Network Inventory** &gt; **Administration** &gt; **Request Definitions**.

2.  Select **New**.

3.  On the Request Definition form, fill in the fields.

<table id="table_o5k_4cg_sdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ID

</td><td>

Unique identifier for the request definition.**Note:** You can't modify an ID after the request definition is created.

</td></tr><tr><td>

Name

</td><td>

Name to identify the request definition.

</td></tr><tr><td>

Task type

</td><td>

Task table that is associated with the change request. Set the **Task type** field as **Change Task**.

</td></tr><tr><td>

Flow

</td><td>

Subflow that is associated with the request definition.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

A request definition is created.

## What to do next

Create and configure the playbook for Design and Assign function. To learn more, see [Create a playbook for the Design and Assign function](create-playbook-design-assign-function.md).

**Parent Topic:**[Configuring Design and Assign function for your network services](../concept/configure-playbooks-design-assign-function.md)

**Related topics**  


[Configuring Design and Assign function for your network services](../concept/configure-playbooks-design-assign-function.md)

[Configure a Design and Assign function example](../concept/configure-design-assign-playbook-use-case.md)

