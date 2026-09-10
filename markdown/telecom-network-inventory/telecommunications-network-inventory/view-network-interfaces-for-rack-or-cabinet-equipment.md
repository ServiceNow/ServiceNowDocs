---
title: View network interfaces for rack or cabinet equipment
description: View all network interfaces for equipment placed in a rack or cabinet, without opening each equipment record individually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/view-network-interfaces-for-rack-or-cabinet-equipment.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Viewing rack or cabinet equipment details, Use, Telecommunications Network Inventory]
---

# View network interfaces for rack or cabinet equipment

View all network interfaces for equipment placed in a rack or cabinet, without opening each equipment record individually.

## Before you begin

Role required: sn\_ni\_core.inventory\_agent

-   Rack or Cabinet CI records must exist in the system.
-   The sn\_ni\_core application must be installed.
-   Equipment CIs must be placed in the rack or cabinet and must have network interfaces defined.

## About this task

The Network Interfaces related list aggregates all interfaces from equipment placed in the rack or cabinet, including equipment nested inside chassis and sub-slots. Use this list to review interface details and identify available ports.

## Procedure

1.  Navigate to Network Inventory Workspace or Service Operation Workspace

2.  Select the \[Omitted image "lists\_icon-proactive.png"\] Alt text: list icon list icon, and then go to Inventory &gt; Rack or Inventory &gt; Cabinet.

3.  Select the rack or cabinet record.

4.  Select the Network Interfaces tab.


## Result

**Note:** Only equipment CIs contribute interfaces to the list. Slot CIs placed in the same rack are excluded. If no interfaces appear, verify that the rack contains at least one equipment CI \(not only slot CIs\).

You can see all network interfaces for the rack or cabinet's equipment in a single list, without navigating to each equipment record.

**Parent Topic:**[Viewing rack or cabinet equipment details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/viewing-rack-or-cabinet-equipment-details.md)

