---
title: Transfer a legal request
description: Transfer a legal request to a new practice area or category if the request was submitted with an inappropriate practice area or category.
locale: en-US
release: australia
product: Legal Request Management
classification: legal-request-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Work on a legal request, Managing legal requests, Use, Legal Request Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Transfer a legal request

Transfer a legal request to a new practice area or category if the request was submitted with an inappropriate practice area or category.

## Before you begin

Ensure that the record producer is mapped to category. For more information, see [Add an intake form to a practice area](associate-categories-practice-area.md).

The transfer request action is available to the users having write access to the request, such as Practice Area Leads, Group Managers, and users with Request manager roles in New state.​ It is also available to the respective fulfillers to whom the request is assigned in the Assigned state.

Role required: sn\_lg\_ops.request\_fulfiller

## About this task

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  Select the List icon \(![List icon](../image/lsd-lcc-list-icon.png)\).

3.  Select **Assigned to Me** under **Legal Requests**.

    **Note:** Practice Area Leads and Group Managers can transfer a legal request without assigning the request to anyone.

4.  Open the legal request that you want to transfer.

5.  Select the More Actions icon \(![More Actions icon.](../image/more-button-icon.png)\) and then select **Transfer Request**.

6.  In the dialog box, fill in the fields.

<table id="table_i3s_5tw_d5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Practice area

</td><td>

Practice area to which you want to transfer the request.

</td></tr><tr><td>

Category

</td><td>

Category associated to the practice area.**Note:** If you select the Third party contract as the category, you need to use **Send to Requester** action instead of **Submit** after transferring the request.

</td></tr><tr><td>

Subcategory

</td><td>

Subcategory associated with the category.

</td></tr><tr><td>

Additional comments

</td><td>

Any comments that would be helpful in relation to the transfer of the legal request.

</td></tr></tbody>
</table>7.  Select **Transfer**.

    The information in the Variables section must be complete.

    -   If you have the variable information, update the Variables details and select **Submit**.

        An email notification is sent to the requester, fulfiller, and anyone on the Watch list.

        **Note:** If the legal request is transferred to **Contracts**, the **Submit** button is not available.

    -   If you do not have the complete variable information, select **Send to Requester** to send the request back to the requester.

        An email notification is sent to the requester, and requested for. For more information, see [Update a legal request by requester](submit-legal-request-requester.md).


## Result

-   The legal request is transferred to the selected practice area.
-   When a request is transferred, the newly created request does not inherit the Privileged and Confidential setting from the parent legal request.
-   A new request is created and the old request is canceled.
-   The state of the new request is Draft.
-   The fulfiller becomes the collaborator. Collaborators are assignees who have similar privileges as the person to whom the legal request is assigned.
-   Any attachments in ServiceNow® storage or external storage like Google Drive and Microsoft OneDrive are transferred to the new request.
-   After the request is sent to the requester, the fulfiller's name is moved from the Collaborators field to the Watch list.
-   The request state is changed to New after the variables are updated and submitted by the fulfiller.

**Parent Topic:**[Work on a legal request](work-on-legal-request.md)

