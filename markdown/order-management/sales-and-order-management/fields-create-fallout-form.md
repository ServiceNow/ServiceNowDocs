---
title: Fallout form fields
description: The Fallout form enables you to manually create, review, and modify the order fallout records.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2025-10-13"
reading_time_minutes: 2
breadcrumb: [Order Management reference, Reference, Sales Customer Relationship Management]
---

# Fallout form fields

The Fallout form enables you to manually create, review, and modify the order fallout records.

<table id="table_bty_b5h_rqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique system-assigned fallout number, starting with a prefix of FO.

</td></tr><tr><td>

Fallout Type

</td><td>

Category that indicates the type of fallout activity.

-   **Billing Issue**

Billing issues and disputes that exist for the ordered item.

-   **Inventory Allocation Failure**

Inadequate inventory. An ordered item can't be fulfilled.

-   **Provisioning Failure**

Associated system that is unavailable due to connectivity problems, timeouts, or other issues.


**Note:** You can also create additional fallout types, as per the requirements of your enterprise. To learn more, see [Create additional fallout types](../concept/configure-fallout-management.md#).

To view the associated details or search for another fallout type:

-   Select the detail icon ![](../image/field-more-info.png) to view the associated details for the fallout type.
-   Select the search icon ![](../image/field-search.png) to search and select another fallout type.

</td></tr><tr><td>

Related order task

</td><td>

Identifier of the order task that the fallout record originated from.

</td></tr><tr><td>

Order Line Item

</td><td>

Identifier of the customer or service order line item that the fallout record originated from.

</td></tr><tr><td>

State

</td><td>

Indicator of the current processing state for the fallout record. Unless otherwise indicated, the fallout manager or agent manually assigns the appropriate state to the fallout record, depending on where it currently resides in the processing cycle.

-   **Open**

Fallout record that is new and not currently assigned to a person to work on.

-   **In progress**

Fallout record that is assigned and currently being worked on.

-   **On hold**

Fallout record that is on hold. No further fallout processing can take place until you release the hold.

-   **Awaiting information**

Fallout record that is on hold and waiting for more information before processing can proceed.

-   **Resolved**

Fallout issue that has a resolution but you have not formally closed it.

-   **Closed complete**

Fallout record that is complete and closed.

-   **Canceled**

Fallout record that the fulfillment manager canceled. No further fulfillment processing can take place.


</td></tr><tr><td>

Priority

</td><td>

Relative priority or importance of the fallout record.

-   **1-Critical**

Fallout record that has urgent time criticality that requires immediate attention.

-   **2-High**

Fallout record that has a high time criticality, though not as urgent as a Critical priority fallout.

-   **3-Moderate**

Fallout record that has a medium time criticality and urgency.

-   **4-Low**

Fallout record that has a low time criticality and urgency.

-   **5-Planning**

Fallout record that was created for planning purposes.


</td></tr><tr><td>

Assignment group

</td><td>

Name of the assigned group that is responsible for acting on the fallout record.

</td></tr><tr><td>

Assigned to

</td><td>

Name of the assigned person who is responsible for acting on the fallout record.

</td></tr><tr><td>

Short description

</td><td>

Short description of the fallout task.

</td></tr><tr><td>

Work notes \(Private\)

</td><td>

Free-form private work note text for internal purposes only. The customer can't see this detail.

</td></tr><tr><td>

Attachments

</td><td>

File attachments for the fallout record. Select **Select file** to add the file as an attachment.

</td></tr></tbody>
</table>**Parent Topic:**[Order Management reference](order-mgt-reference.md)

