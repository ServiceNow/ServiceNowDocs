---
title: Fallout Management data model
description: Manage and fix the processing issues that occur during the fulfillment of a customer or service order. With Fallout Management, you can identify the order processing exceptions and create a fallout record to investigate and resolve the underlying processing issue. Fallout Management enables a customer or service order to continue until it's completed.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Order Management, Exploring Sales Customer Relationship Management, Sales Customer Relationship Management]
---

# Fallout Management data model

Manage and fix the processing issues that occur during the fulfillment of a customer or service order. With Fallout Management, you can identify the order processing exceptions and create a fallout record to investigate and resolve the underlying processing issue. Fallout Management enables a customer or service order to continue until it's completed.

The Fallout Management data model extends the Task table. The following table lists the attributes that apply to order fallout processing.

<table id="table_as2_qdv_t4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique system-assigned fallout number, starting with a prefix of FO, up to seven digits in length.

</td></tr><tr><td>

Assigned to

</td><td>

Identifier for the assigned person responsible for acting on the fallout record.

</td></tr><tr><td>

Created by

</td><td>

Identifier for the fallout administrator who created the fallout record.

</td></tr><tr><td>

Created on

</td><td>

Timestamp that includes the date and time that the fallout record was created.

</td></tr><tr><td>

State

</td><td>

Indicator of the current processing state for the fallout record. Unless otherwise indicated, the fallout manager or agent manually assigns the appropriate state to the fallout record, depending on where it currently resides in the processing cycle.

-   **Open**

Fallout record that is new and not currently assigned to a person to work on.

-   **In Progress**

Fallout record that is assigned and currently being worked on.

-   **On Hold**

Fallout record that is on hold. No further fallout processing can take place until you release the hold.

-   **Awaiting Information**

Fallout record that is on hold and waiting for more information before processing can proceed.

-   **Resolved**

Fallout issue that has a resolution but you have not formally closed it.

-   **Closed Completed**

Fallout record that is complete and closed.

-   **Canceled**

Fallout record that the fulfillment manager canceled. No further fulfillment processing can take place.


</td></tr><tr><td>

Originated from

</td><td>

Identifier of the originating order task record that the fallout record is associated with.

</td></tr><tr><td>

Activity

</td><td>

Listing of the processing activities and changes in the field values that have taken place for the fallout record. To expand, collapse, or filter by activity stream:

-   Click the activity stream filter icon \(![Activity stream filter icon.](../image/activity-stream-filter.png)\) to filter by additional comments, attachments, or state.
-   Click the more options icon \(![More options icon.](../image/more-options.png)\), and then select the appropriate one:

![More options selection.](../image/more-options-filter.png)


</td></tr><tr><td>

Attachments

</td><td>

File attachments for the fallout record. Click **Browse** to add the file as an attachment.

</td></tr></tbody>
</table>**Related topics**  


[Managing order fallout](fallout-management-overview.md)

[Create automated and manual fallout records](creating-automated-manual-fallout-records.md#)

[Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)

[Flows](https://www.servicenow.com/docs/access?context=flows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)

[Create a flow](https://www.servicenow.com/docs/access?context=create-flow&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)

