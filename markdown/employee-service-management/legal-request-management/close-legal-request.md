---
title: Close a legal request
description: You can close a legal request assigned to you when you've resolved it.
locale: en-US
release: australia
product: Legal Request Management
classification: legal-request-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Work on a legal request, Managing legal requests, Use, Legal Request Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Close a legal request

You can close a legal request assigned to you when you've resolved it.

## Before you begin

If you've installed Legal Matter Management and have a legal request promoted to a legal matter, the system closes legal requests automatically when the matter owner chooses to close the related requests while closing the matter.

**Note:** A legal request cannot be closed if there are any open ad hoc approval records for it or its attachments.

Role required: sn\_lg\_ops.legal\_fulfiller

## About this task

As a collaborator added to a request, you can access and work on the request just as assignees can. However, you can't modify the **Assigned to** and **Assignment group** fields.

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  Click the list icon \(![List icon](../image/lsd-lcc-list-icon.png)\).

3.  In the **Lists** tab, open a legal request by selecting an option under **Legal Requests**.

<table id="choicetable_jhj_kb3_gtb"><thead><tr><th align="left" id="d384943e108">

Option

</th><th align="left" id="d384943e111">

Steps

</th></tr></thead><tbody><tr><td id="d384943e117">

**As an assignee**

</td><td>

1.  Select the **Assigned to Me** option.
2.  Select a request to work on.
3.  If the request is newly assigned to you, select **Start Work** to start working on the request.

The state of the legal request is Work in progress and the document is Legal review.

</td></tr><tr><td id="d384943e146">

**As a collaborator**

</td><td>

1.  Select the **Collaborations** option.
2.  Select a request to work on.


</td></tr></tbody>
</table>4.  [Attach files](manage-attachments-legal-request.md) that are a solution for the request or a link to the knowledge base article as reference material for the requester.

5.  Close the request based on the work done on the request:

    -   If your work on the request resolved the request, click **Close Complete**.
    -   If you have done some work on the request but were unable to resolve the request, click **Close Incomplete**.
6.  In the dialog box, enter comments to explain why the request was closed in the **Additional comments** field.

7.  Click **OK**.


## Result

The legal request is closed based on the [system property](../reference/legal-properties.md#prop_lrm_request_open) **sn\_lg\_ops.allow\_request\_closure\_with\_open\_matters** and whether or not there is a legal matter associated with the request.

-   If the property is set to false and there is an open associated legal matter, the request is closed only after the legal matter is closed.
-   If the property is set to true, the request is closed regardless of the state of the associated legal matters.

The state of the request changes to Closed Complete or Closed Incomplete, depending on the option selected.

**Parent Topic:**[Work on a legal request](work-on-legal-request.md)

