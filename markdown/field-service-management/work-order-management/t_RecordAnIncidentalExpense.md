---
title: Record an incidental expense
description: Record incidental expenses associated with your business travel through the Field Service application to execute work order tasks.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Execute work order tasks, Updating task status, Completing work orders on the web interface, Use, Field Service Management]
---

# Record an incidental expense

Record incidental expenses associated with your business travel through the Field Service application to execute work order tasks.

## Before you begin

Role required: admin, wm\_agent.

## About this task

Log incidentals to manage your expenses such as car rental cost, mileage, and vendor costs that you spend to execute your work order task at any point during the task life cycle. You can attach a receipt for a logged incidental.

For example, field service administrators might create an incidental in the Pending state before an agent begins work, based on an anticipated expense. Agents might create incidentals in the Incurred state as expenses arise during work.

Role required: wm\_admin or wm\_agent.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Work Order** &gt; **All Work Order Tasks**.

2.  Open a work order task for which you want to log incidentals.

3.  In the **Service Management Incidentals** related list, click **New**.

4.  Fill in the fields as described in the following table.

<table id="table_n1w_pwv_rr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service order task

</td><td>

\[Read-only\] Task from which the incidental was created.

</td></tr><tr><td>

Type

</td><td>

Select incidental type:-   **Mileage** for traveling to and from the task site.
-   **Car Rental** for renting the car.
-   **Vendor Cost** for all vendor-related costs on a contract.


</td></tr><tr><td>

Cost

</td><td>

Total cost of the incidental. -   From the **Currency** field, select the currency for the expense.
-   Enter cost:
    -   If the type is **Mileage**, the cost is read-only and is automatically calculated by multiplying **Quantity** and **Cost per mile**.
    -   If the type is **Car Rental**, enter the total cost of rental expenses.


</td></tr><tr><td>

Quantity

</td><td>

Number of units for the incidental. This field is required if the type is **Mileage**; enter the number of miles traveled. This field is hidden if the type is **Car Rental**.

</td></tr><tr><td>

State

</td><td>

Select the status of the expense: -   **Incurred** when the expense has already occurred
-   **Pending** when the expense has not yet occurred.


</td></tr><tr><td>

Cost per mile

</td><td>

Average cost of transportation per mile. This field is visible only if the type is **Mileage**.

</td></tr><tr><td>

Description

</td><td>

Helpful information about the incidental expense.

</td></tr></tbody>
</table>5.  Click **Submit**.


## Result

An incidental record is created, the system generates an expense line if the following conditions are met:

-   The state is **Incurred**.
-   The type is not **None**.
-   The cost is greater than zero.

**Note:** The expense line is deleted if any of these conditions change.

Field service administrators and agents can view all incidentals by navigating to **Field Service** &gt; **Agent** &gt; **Incidentals**.

