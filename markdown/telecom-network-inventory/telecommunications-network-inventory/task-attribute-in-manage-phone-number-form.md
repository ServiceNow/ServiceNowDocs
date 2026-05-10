---
title: Task Attribute in Manage Phone Number Form
description: The Task attributes in Manage Phone Number Form form enables you to design and assign a phone number in the Telecommunications Network Inventory application.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2026-05-09"
reading_time_minutes: 2
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Task Attribute in Manage Phone Number Form

The Task attributes in Manage Phone Number Form form enables you to design and assign a phone number in the Telecommunications Network Inventory application.

<table id="table_rgv_w4f_4xb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action

</td><td>

Action that you can select:-   **Allocate**: Allocates the numbers from a block
-   **De-allocate**: De-allocates the numbers. The status of the numbers is changed to Quarantine.

**Note:** When you select this action, you must select an allocation or the selected numbers that you want to deallocate. This action results in changing the status to Quarantine.

-   **Ported-in**: Includes the numbers that are moved from another operator. The numbers are stored in a telephone number allocation of telephone numbers only.

**Note:** Multiple allocations get created if the numbers aren’t in a series of numbers. Also, by default, the numbers are changed to the assigned or the ported-in status.

-   **Create**: Creates the phone number allocation for the numbers that are assigned to an external telephone block. You’re assigning the numbers to a network inventory-based phone number allocation.

</td></tr><tr><td>

Service

</td><td>

Service for these numbers. The selected service gets assigned to the numbers.**Note:** Ensure that you’ve created a service for this phone number. To learn more, see [Manage your network functions](../concept/services.md).

</td></tr><tr><td>

Quantity

</td><td>

Total number of required phone numbers.**Note:** This field disappears for a deallocated action.

</td></tr><tr><td>

Line number

</td><td>

Enter your required line number in xxxx-xxxx or xxx-xxx or xxx, xxx-xxx format.**Note:** Multiple telephone number allocations are created if the line number isn’t in a series of numbers. Also, the status of these numbers gets updated to either assigned or ported-in and the availability is No.

</td></tr><tr><td>

Available telephone numbers

</td><td>

Displays the list of telephone numbers that are available for allocation based on the selected country code, area code, and central office code.

</td></tr><tr><td>

Country code

</td><td>

Country dialing code used to generate and manage the telephone numbers**Note:** This field appears only if Allocate action is selected in from the **Action** dropdown.

</td></tr><tr><td>

Central office code

</td><td>

This field is optional to support geographies where the central office code isn’t a distinct or mandatory component of the telephone number.**Note:** This field appears only if Allocate action is selected from the **Action** dropdown.

</td></tr><tr><td>

Area code

</td><td>

Geographic area code that forms part of the telephone number.**Note:** This field appears only if Allocate action is selected from the **Action** dropdown.

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Network Inventory reference](../concept/telecommunications-network-inventory-reference.md)

