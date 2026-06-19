---
title: Create Managed Network
description: Created topic as per DOC1076129.Create a managed network to manage all your networks and IP addresses using the Telecommunications Network Inventory application. You can create, review, update, and delete a network.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/create\_managed\_network.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage IP addresses, Inventory number allocation, Define inventory records, Use, Telecommunications Network Inventory]
---

# Create Managed Network

Create a managed network to manage all your networks and IP addresses using the Telecommunications Network Inventory application. You can create, review, update, and delete a network.

## Before you begin

-   Install network discovery plugins. To learn more, see Network discovery.
-   Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent, sn\_ni\_core.inventory\_template\_manager, sn\_ni\_core.telco\_inventory\_catalog\_manager.

## About this task

Managed network enables you to add IP pool and IP network subnet in your network. Also, a network can’t have a duplicated IP address.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(\[Omitted image "ni-workspace-list-icon.png"\] Alt text: List icon.\), and then go to **Inventory Number Allocation** &gt; **Managed Network**.

3.  Select **New**.

4.  Under the **Details** tab, on the form, fill in the fields.

    To learn more, see [Managed Network form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/managed_network_form.md).

5.  Add packs to this service by selecting **Add Packs**.

    To learn more about the packs, see [Attribute packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunication-network-inventory-pack.md).

6.  Add the attachments, such as the graphics or documents, by selecting the attachment icon \(\[Omitted image "attachments-icon.png"\] Alt text: Attachment icon.\) in the right panel.

7.  Select **Save**.

    CMDB 360 data and packs related tabs appear on the form. To learn more, see [Related tabs in the Network inventory forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/inventory-related-tab.md).

8.  View the related network inventories by selecting the brick icon \(\[Omitted image "infrastructure-relashionship.png"\] Alt text: brick icon.\).

    The Infrastructure Relationships section shows all the related network inventories that are grouped by the individual network asset instances.


## What to do next

You can review, or update the fields, create a related tab record, or can delete a record. To learn more, see [Update or delete a record of an inventory number allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/update_and_delete_ip_address_space.md).

**Parent Topic:**[Manage IP addresses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/manage-ip-addresses.md)

