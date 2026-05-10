---
title: Add variable set to the record producer for Design and Assign function
description: Add a variable set to a record producer in the Telecommunications Network Inventory application. You can use the variable set as input fields in an activity card for the Design and Assign function.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Design and Assign function, Configure, Telecommunications Network Inventory]
---

# Add variable set to the record producer for Design and Assign function

Add a variable set to a record producer in the Telecommunications Network Inventory application. You can use the variable set as input fields in an activity card for the Design and Assign function.

## Before you begin

Role required: admin, sn\_ni\_core.inventory\_admin

## About this task

The variable set has common attributes which are retrieved during the change task creation. You can use an existing variable set or create a variable set depending on your requirement. To configure an activity in the Design and Assign playbook, use the **DA common variables** variable set.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Record Producers**.

2.  Select a record producer that you want to create variables for.

3.  On the **Variable Sets** tab, select **Edit**.

4.  Select **DA common variables**.

    The **DA common variables** set provides the common variables for the design and assign function.

5.  Select **Submit**.


## Result

The variable set is added to the record producer.

## What to do next

Create a subflow for the activity. [Create subflow for Design and Assign function](create-subflow-design-assign-playbook.md).

**Parent Topic:**[Configuring Design and Assign function for your network services](../concept/configure-playbooks-design-assign-function.md)

**Related topics**  


[Service catalog variable sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/c_ServiceCatalogVariableSets.md)

[Configuring Design and Assign function for your network services](../concept/configure-playbooks-design-assign-function.md)

[Configure a Design and Assign function example](../concept/configure-design-assign-playbook-use-case.md)

