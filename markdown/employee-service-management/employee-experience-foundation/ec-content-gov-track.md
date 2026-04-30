---
title: Tracking content requests
description: After a content request is submitted, Content Governance enables the content requester, content managers, and content admins to track the status of the request and associated content.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Managing content requests with Content Governance, Manage, Employee Center, Employee Service Management]
---

# Tracking content requests

After a content request is submitted, Content Governance enables the content requester, content managers, and content admins to track the status of the request and associated content.

## Tracking as the content requester

After submitting a content request, the employee can track the status of the request by navigating to **My requests** and opening the content request. They can add a comment for the content manager, attach files, and review the details they submitted.![The content requester can track the request status from the My Request tab](../images/content-gov-request-view.png)

The state field of a content request provides a quick status update to the requester and content team, as well as triggers system actions. For more information, see [Understanding content request states](ec-content-gov-track.md#understanding-request-states).

## Tracking as a content manager or content admin

Content managers and content admins can view content requests by navigating to **Content Governance** &gt; **All Requests**. Each time an employee submits a content request, the system creates a record with the prefix CONREQ. This record can be assigned either to an individual content manager or to a group. The record is used for the following purposes:

-   Holds the request details, such as the type of content that needs to be created and the intended audience
-   Communicate with the employee who made the request
-   Holds the associated content once it's created in the Content Request Items list
-   Tracks the request status

Content admins and content managers can view all the content requests and associated content, even if they aren't assigned to that record.

## Understanding content request states

The content request state provides a quick update on the current status to the employee who made the content request, approvers, and the content team.

The status bar at the top of a content request record displays all the states, with the current state highlighted.![Content request status bar](../images/ec_status_bar.png)

<table id="table_jkp_yq2_bwb"><thead><tr><th>

Content request state

</th><th>

Content request item state

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New

</td><td>

Open

</td><td>

Content request was submitted

</td></tr><tr><td>

Assigned

</td><td>

Open

</td><td>

Content admin or manager assigns the request to a content manager or team, and manually updates the state

</td></tr><tr><td>

Work in Progress

</td><td>

Work in Progress

</td><td>

Content manager manually updates the state when they start working on the ticket

</td></tr><tr><td>

In Review

</td><td>

In Review

</td><td>

After the content manager creates the content and publishing plan and clicks **Send for review**, the system updates the state to "In Review" and assigns a task to the content requester and approvers to review the content**Note:** Once a content request item is **In Review**, the content cannot be edited. The content manager must revert the state to "Work in Progress" to edit the content.

</td></tr><tr><td>

Ready to Publish

</td><td>

Ready to Publish

</td><td>

When the requester clicks **Approve**, the system updates the state to **Ready to Publish**

</td></tr><tr><td>

Published

</td><td>

Published

</td><td>

The content manager manually updates the record to **Published** and the content becomes available to employees according to the publish plan configuration

</td></tr><tr><td>

Cancelled

</td><td>

Cancelled

</td><td>

The content admin cancels the request.

</td></tr></tbody>
</table>**Note:** Content request items require content and publishing plan in order to change the state to **In Review**, **Ready to Publish**, and **Published**.

For information on how to customize the approval process, see [Employee tasks page](employee-center-to-dos-page-configuration.md).

**Parent Topic:**[Managing content requests with Content Governance](ec-content-governance.md)

