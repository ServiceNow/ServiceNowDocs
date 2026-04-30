---
title: Transfer a legal ticket to another department
description: Transfer a legal ticket \(legal request or legal matter\) associated with a universal request to another department or back to the universal request for processing and resolution.
locale: en-US
release: xanadu
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Universal Request for Legal Service Delivery, Integration of Legal Service Delivery with ServiceNow applications, Legal Service Delivery, Employee Service Management]
---

# Transfer a legal ticket to another department

Transfer a legal ticket \(legal request or legal matter\) associated with a universal request to another department or back to the universal request for processing and resolution.

## Before you begin

Role required: sn\_lg\_ops.legal\_fulfiller

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  Click the List icon \(![List icon](../image/lsd-lcc-list-icon.png)\).

3.  Open the list of legal requests or legal matters.

    -   To open the legal request list, in the **Lists** tab, select **Assigned to Me** under **Legal Requests**.
    -   To open the legal matter list, in the **Lists** tab, select **Assigned to Me** under **Matters**.
4.  Open a legal request or legal matter that you want to transfer.

5.  Select **Transfer**.

6.  In the Transfer Ticket dialog box, fill in the fields.

<table id="table_i3s_5tw_d5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action

</td><td>

Transfer options to other department or back to universal request.

</td></tr><tr><td>

Department

</td><td>

Department to which you want to transfer the request.If the user is not sure which department to transfer the legal ticket to, the **I'm not sure** option transfers the ticket back to the universal request.

</td></tr><tr><td>

Service

</td><td>

The service or request type within the selected department.**Note:** **Employee Relations** must be selected to transfer an ethics complaint legal matter to the Human Resources department. For any other service selected, an error message is displayed.

</td></tr><tr><td>

Transfer reason

</td><td>

Option to specify whether the legal ticket is being transferred with a resolution.-   **Transfer with resolution**: The legal ticket is resolved and needs further processing by another department. The state of the legal ticket will update to Close Complete.
-   **Transfer without resolution**: The legal ticket is not resolved or does not belong to the Legal department. The state of legal ticket will update to Close Incomplete.


</td></tr><tr><td>

Transfer notes

</td><td>

Details that might be useful for the department to know for further processing.

</td></tr><tr><td>

Copy additional comments and attachments

</td><td>

Options for including additional comments and attachments from the legal ticket to the request of another department with the transfer.By default, this option is selected. If the additional comments and attachments shouldn't be transferred, clear the check box.

</td></tr></tbody>
</table>7.  Select **Transfer**.


## Result

-   The legal ticket is transferred to the selected department.
-   The legal ticket no longer remains a primary ticket for the universal request.

**Parent Topic:**[Universal Request for Legal Service Delivery](../concept/universal-requests-legal.md)

