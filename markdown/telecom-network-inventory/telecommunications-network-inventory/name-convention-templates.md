---
title: Naming convention for associated templates
description: Learn about the details of the naming convention for the associated templates that are automatically generated when you create an equipment or interface card template.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Naming convention for associated templates

Learn about the details of the naming convention for the associated templates that are automatically generated when you create an equipment or interface card template.

<table id="table_f4w_r1y_ztb"><thead><tr><th>

Variable name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

position

</td><td>

Unit position of either the interface or slot/holder that it is getting applied to. **Note:** The unit position always starts from 0. The slot/interface start number that is configured in the inventory model does not apply to the unit position.

</td></tr><tr><td>

parent\_slot\_name

</td><td>

Name of the slot that the card is inserted in, if the slot or interface belongs to a card.

</td></tr><tr><td>

parent\_slot\_position

</td><td>

Unit position of the slot that the card is inserted in, if the slot or interface belongs to a card.

</td></tr><tr><td>

equipment\_slot\_name

</td><td>

Name of the slot on the equipment where the base card is inserted in, if the slot or interface belongs to a card. The parent\_slot\_name and equipment\_slot\_name hold the same value if the current card is a base card.

</td></tr><tr><td>

equipment\_slot\_position

</td><td>

Unit position of the slot on the equipment where the base card is inserted in, if the slot/interface belongs to a card. The parent\_slot\_number and equipment\_slot\_number hold the same value if the current card is a base card.

</td></tr><tr><td>

bandwidth

</td><td>

Bandwidth value of the interface.

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Network Inventory reference](../concept/telecommunications-network-inventory-reference.md)

