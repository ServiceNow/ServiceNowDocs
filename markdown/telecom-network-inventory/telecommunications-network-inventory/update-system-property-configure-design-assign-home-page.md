---
title: Update system property to configure the Design and Assign home page
description: Update the system property to add a playbook to the Design and Assign home page in the Telecommunications Network Inventory application. You can launch the Design and Assign function from the home page and execute the steps to achieve your goal.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Design and Assign function for your network services, Configuring Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Update system property to configure the Design and Assign home page

Update the system property to add a playbook to the Design and Assign home page in the Telecommunications Network Inventory application. You can launch the Design and Assign function from the home page and execute the steps to achieve your goal.

## Before you begin

Role required: admin, sn\_ni\_core.inventory\_admin

## About this task

Add the change model in the system property to use the playbook for the Design and Assign function. As you add, the Design and Assign home page lists a UI action to launch the playbook.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All**.

2.  Open the **sn\_ni\_ws.tni\_design\_assign\_chg\_models** record.

3.  In the **Value** field, add the sys\_id of the change model.

    **Note:** The default value is the sys\_id of the logical connection model that is available in the Design and Assign home page.

4.  Select **Update**.


## Result

The Change model name appears as a UI action in the Design and Assign home page. Selecting the UI action launches the playbook.

## What to do next

Use the playbook to design and assign a service request. To learn more, see [Using Design and Assign function](../concept/using-playbooks-design-assign-inventory-record.md).

**Parent Topic:**[Configuring Design and Assign function for your network services](../concept/configure-playbooks-design-assign-function.md)

**Related topics**  


[Configuring Design and Assign function for your network services](../concept/configure-playbooks-design-assign-function.md)

[Configure a Design and Assign function example](../concept/configure-design-assign-playbook-use-case.md)

