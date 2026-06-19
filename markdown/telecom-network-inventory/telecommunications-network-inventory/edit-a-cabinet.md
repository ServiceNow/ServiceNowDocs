---
title: Edit a cabinet
description: Edit a cabinet to remove, add, or move the equipment from the selected cabinet. Organize and upgrade the components within the cabinet using the Telecommunications Network Inventory application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/edit-a-cabinet.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a cabinet, Create and maintain racks and cabinets, Manually creating and reviewing your network asset instances, Define inventory records, Use, Telecommunications Network Inventory]
---

# Edit a cabinet

Edit a cabinet to remove, add, or move the equipment from the selected cabinet. Organize and upgrade the components within the cabinet using the Telecommunications Network Inventory application.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(\[Omitted image "ni-workspace-list-icon.png"\] Alt text: List icon.\), and then go to **Inventory** &gt; **Cabinet**.

3.  Select a cabinet from the displayed list.

    A dashboard displays all equipment types added under the cabinet along with the cabinet view and information of the selected equipment.

4.  Select **Edit Cabinet**.

    Instead of the equipment types and cabinet view, a list of all equipment, and the front view of both edit configuration and current configuration is displayed.

5.  From the displayed list of equipment, search for the equipment to add in a cabinet by using either the filters or the search box.

    -   The existing filters automatically clear on entering a search. And, applying a filter clears your search terms.
    -   The equipment list can also be sorted based on latest creation date, highest number of Rack Units, and weight.
    -   The list shows all the equipment records included in the sn\_ni\_core.equipment system property, and the equipment that aren't in the cabinet.
    -   The info \(\[Omitted image "icon-info.png"\] Alt text: info icon\) expands and displays the equipment details on selecting an equipment or the info button.
6.  Perform any of the following actions while editing a cabinet.

<table id="table_tqd_2yr_lbc"><thead><tr><th>

Actions

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Add

</td><td>

1.  Select **\(\[Omitted image "icon-menu.png"\] Alt text: Options icon\)** &gt; **Add to Cabinet**.
2.  Fill in the fields and select **Add**.

To learn more about the fields, see add equipment to rack/cabinet table of [Change request and change task forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/change_request_forms.md).

You can also drag the equipment from the corner to the desired rack unit.

</td></tr><tr><td>

Move

</td><td>

1.  Select **\(\[Omitted image "icon-menu.png"\] Alt text: Options icon\)** &gt; **Move**.
2.  Fill in the fields and select **Move**.

To learn more about the fields, see add equipment to rack/cabinet table of [Change request and change task forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/change_request_forms.md).

You can also drag the equipment from the corner to the desired rack unit.

</td></tr><tr><td>

Remove

</td><td>

Select **\(\[Omitted image "icon-menu.png"\] Alt text: Options icon\)** &gt; **Remove**.

</td></tr><tr><td>

Reserve a rack unit

</td><td>

Select Options \(\[Omitted image "icon-menu.png"\] Alt text: Options icon\) of the rack unit that you want to reserve and select **Reserve**.

</td></tr></tbody>
</table>7.  Select **Save**.

    A change request is created with the implemented modifications under the **Change Tasks** tab. Once the changes are applied, work notes of the tasks are updated and are marked as closed.

    Select the displayed change request to see change tasks and more.

    **Note:** A change request is created only if the cabinet is modified.


## What to do next

To perform further actions, see [Optimizing rack and cabinet usage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/subsequent-actions.md).

**Parent Topic:**[Create a cabinet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-a-cabinet.md)

