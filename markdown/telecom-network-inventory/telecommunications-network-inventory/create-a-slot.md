---
title: Create a slot for equipment
description: Added as per STRY57142377 - DOC1091704Create a slot to provide a designated space for the equipment to maintain, update and access all types of equipment. You can route cables using the Telecommunications Network Inventory application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/create-a-slot.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manually creating and reviewing your network asset instances, Define inventory records, Use, Telecommunications Network Inventory]
---

# Create a slot for equipment

Create a slot to provide a designated space for the equipment to maintain, update and access all types of equipment. You can route cables using the Telecommunications Network Inventory application.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent, sn\_ni\_core.inventory\_template\_manager, sn\_ni\_core.telco\_inventory\_catalog\_manager

## About this task

Slots help a rack to distribute the weight of the equipment across the rack evenly. On creating a slot, a record is created in the Slot \[cmdb\_ci\_container\_slot\] table.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(\[Omitted image "ni-workspace-list-icon.png"\] Alt text: List icon.\), and then go to **Inventory** &gt; **Slot**.

3.  Create a slot by selecting **New**.

4.  On the Equipment Holder form, fill in the fields.

    To learn more, see [Equipment Holder form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/tni-equipment-holder-form-configuration.md).

5.  Select **Set Inventory Attributes**.

6.  On the TNI CI Attributes form, fill in the fields.

    To learn more about the fields, see [TNI CI Attributes form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/ci-attribue-form.md).

7.  Select **Save**.


**Parent Topic:**[Manually creating and reviewing your network asset instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/creating-telecommunications-network-inventory.md)

