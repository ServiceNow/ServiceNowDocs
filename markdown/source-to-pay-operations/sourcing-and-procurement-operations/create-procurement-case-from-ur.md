---
title: Create a procurement case from a Universal Request
description: When a Universal Request arrives in the Source-to-Pay Workspace, create a linked procurement case to track and manage the request through fulfillment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/sourcing-and-procurement-operations/create-procurement-case-from-ur.html
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-06-03"
reading_time_minutes: 1
keywords: [Universal Request, universal request, ur]
breadcrumb: [Create a Universal Request, Use Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Create a procurement case from a Universal Request

When a Universal Request arrives in the Source-to-Pay Workspace, create a linked procurement case to track and manage the request through fulfillment.

## Before you begin

Role required: sn\_uni\_req.routing\_agent and sn\_uni\_req.sensitiveinfo\_agent

The Universal Request for Source-to-Pay Operations plugin \(sn\_fsc\_ur\_common\) must be active. To activate the plugin, see [Install Universal Request for Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/install-universal-request-spo.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Source-to-Pay Workspace**.

2.  Select the list icon.

3.  Navigate to **Universal request** &gt; **All**.

4.  Select a Universal Request to review the case details.

5.  Select **Create Case** &gt; **Create Procurement Case**.

    The Create New Procurement Case form opens with details automatically populated from the Universal Request.

6.  Select **Save**.

7.  Select **Transfer** to move the Universal Request to a different department.

    For more information, see [Transfer a primary ticket](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/universal-request-for-hr-service-delivery/route-primarytask-to-ur.md)

8.  Select **Create Associated Ticket** to request assistance from another department while keeping the current procurement case as the primary ticket.

    For more information, see [Create associated ticket for primary ticket of UR](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/universal-request-for-hr-service-delivery/create-associated-ticket.md).

    **Note:** If an associated ticket is assigned to a team whose cases are not visible to the employee, the Universal Request does not display ticket updates.


## Result

A procurement case is created and linked to the Universal Request. When the procurement case moves to **In Progress** or **Closed Complete**, the Universal Request status syncs automatically based on state mapping, and the employee can track progress in Employee Center.

**Parent Topic:**[Create a Universal Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/create-universal-request.md)

