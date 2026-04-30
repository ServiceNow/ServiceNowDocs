---
title: Transfer a request to another department
description: Transfer a request to another department with or without resolution to fulfill the request.
locale: en-US
release: yokohama
product: Request Management
classification: request-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Request Management integration with Universal Request, Configure, Request Management, IT Service Management]
---

# Transfer a request to another department

Transfer a request to another department with or without resolution to fulfill the request.

## Before you begin

Role required: itil, routing agent, sn\_request\_write, or sn\_hr\_core\_case\_writer

Configure the sn\_uni\_req.transfer\_type property in the Universal Request properties page to determine how to handle the request transfers. For more information, see [Universal Request properties](https://www.servicenow.com/docs/access?context=ur-properties&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).

The agent can transfer a request with one of the following reasons:

-   **Transfer with resolution**

    The request is resolved and transferred back to UR, a specific department, or a service. Agents can select this option when another departments help is required to fulfill the request.

-   **Transfer without resolution**

    The request isn’t resolved or doesn’t belong to the specific department and transferred back to UR, a specific department, or a service.


## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Open Records** &gt; **Items**.

2.  Select the request item that you want to transfer.

3.  Click **Transfer**.

    **Note:** To transfer a request, either you must be part of the assignment group or the request must have been assigned to you.

4.  In the **Transfer Ticket** dialog box, fill in the details.

<table id="table_j2d_2dj_5pb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Department

</td><td>

Department that you want to transfer the request to.

</td></tr><tr><td>

Transfer reason

</td><td>

Reason why you are transferring the request to the department.

</td></tr><tr><td>

Transfer notes

</td><td>

Brief description on the reason for transferring the primary ticket. These notes are read by the UR Routing agent who handles universal requests.

</td></tr><tr><td>

Copy additional comments and attachments

</td><td>

Option to copy the comments and attachments of the request while transferring. The option is automatically selected.**Note:** Work notes are not copied while transfer.

</td></tr></tbody>
</table>5.  Click **Transfer**.


## Result

The request item is transferred to the selected department. The request is transferred based on the direct transfer mappings in mapping configuration and transfer type configurations. For more information on configuring routing, see [Transfer configuration](https://www.servicenow.com/docs/access?context=configure-route-state&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).

**Parent Topic:**[Request Management integration with Universal Request](../concept/request-mgmt-integration-ur.md)

