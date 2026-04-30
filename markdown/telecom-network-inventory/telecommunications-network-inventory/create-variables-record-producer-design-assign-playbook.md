---
title: Create variables for Design and Assign function
description: Create the variables for a record producer in the Telecommunications Network Inventory application. You can use these variables as input fields in an activity card in the playbook for the Design and Assign function.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Design and Assign function, Configure, Telecommunications Network Inventory]
---

# Create variables for Design and Assign function

Create the variables for a record producer in the Telecommunications Network Inventory application. You can use these variables as input fields in an activity card in the playbook for the Design and Assign function.

## Before you begin

Role required: admin, sn\_ni\_core.inventory\_admin

## About this task

Create and add input variables to the record producer. The variables are displayed on the activity card in the playbook as input fields.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Record Producers**.

2.  Select a record producer that you want to create variables for.

3.  On the **Variables** tab, select **New**.

4.  On the **Variable** form, fill in the fields.

<table id="table_kfy_cbr_sdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Select the variable type.

</td></tr><tr><td>

Catalog item

</td><td>

By default, the record producer name is displayed.

</td></tr><tr><td>

Question

</td><td>

Question that you can ask users who are using the catalog item to obtain related information.

</td></tr><tr><td>

Name

</td><td>

Name to identify the question.**Note:** If this field is empty, its value is auto-populated based on the Question field.

</td></tr><tr><td>

Type Specification

</td><td>

Values specific to the type of variables.

</td></tr></tbody>
</table>5.  Select **Submit**.

    Repeat the preceding steps to create additional variables for the record producer.

6.  Select **Submit**.


## Result

The input variables are created and added to the record producer.

## What to do next

Add variables set to the record producer. To learn more, see [Add variable set to the record producer for Design and Assign function](add-variable-set-record-producer-design-assign-playbook.md).

**Parent Topic:**[Design and Assign function for your network services](../concept/configure-playbooks-design-assign-function.md)

**Related topics**  


[Record Producer](https://www.servicenow.com/docs/access?context=c_RecordProducer&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)

[Service catalog variables](https://www.servicenow.com/docs/access?context=c_ServiceCatalogVariables&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)

[Design and Assign function for your network services](../concept/configure-playbooks-design-assign-function.md)

[Configure a Design and Assign function example](../concept/configure-design-assign-playbook-use-case.md)

