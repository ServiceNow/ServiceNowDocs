---
title: Create invoice case from Universal Request
description: AP agents validate the incoming UR requests in the Source-to-Pay workspace and create an invoice case for further processing.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-11-17"
reading_time_minutes: 2
breadcrumb: [Universal Request in Accounts Payable Operations, Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Create invoice case from Universal Request

AP agents validate the incoming UR requests in the Source-to-Pay workspace and create an invoice case for further processing.

## Before you begin

Role required: Users must be part of the Accounts Payable Universal Request group which contains the roles sn\_uni\_req.routing\_agent, sn\_ap\_cm.agent, \[sn\_uni\_req.sensitiveinfo\_agent\] optional.

Plugins required:

-   Universal Request for Source-to-Pay Operations Plugin \[sn\_fsc\_ur\_common\] plugin \(contains dependent plugin Universal Request Plugin \[com.snc.universal\_request\]\)
-   Invoice Case Management \[com.sn\_ap\_cm\].

Users can also create own groups. For more information on creating own service- specific-assignment groups see, Universal Request is raised in the Employee Center or Supplier portal.

## Procedure

1.  Navigate to **Source-to-Pay workspace** &gt; **List** &gt; **Universal request**.

    The AP agent validates the UR case details and creates an invoice case for further processing.![Universal Request List view](../image/universal-req-list.png)

2.  Select a specific UR case to view case details.

    **Note:** Users with \[sn\_uni\_req.sensitiveinfo\_agent\] role can view and work on the tickets that are marked as restricted. Restricted tickets contain sensitive information and are secured from general viewing.

3.  Select **Create case** &gt;**Create invoice case**.

    The **Create New Invoice case** form appears. The associated UR details appear as a banner in the case. For more information on creating invoice case, see [Create an invoice manually](create-invoice.md).![Create invoice case](../image/create-invoice-ur.png)

4.  Select **Save** to save the changes.

5.  Select **Transfer** if the primary ticket belongs to a different team.

    If a ticket is transferred to another team and the user who submitted the UR doesn't have the necessary permissions to access that team's case, updates to the UR will not be visible to them.

    For more information on transferring a UR, see [Transfer a primary ticket](https://www.servicenow.com/docs/access?context=route-primarytask-to-ur&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).![Transfer UR](../image/transfer-ur.png)

6.  Select **Create Associated Ticket** to request other departments for assistance in resolving a universal request \(UR\).

    For more information on associated ticket, see [Create associated ticket for primary ticket of UR](https://www.servicenow.com/docs/access?context=create-associated-ticket&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).

    If the ticket is assigned to another team, and the original user who submitted the UR doesn’t possess the necessary privileges or access to view that team's case, they’ll be unable to monitor updates on the UR.

    ![Associated ticket](../image/ur-associated-ticket-success.png)

    An associated ticket is created.


## Result

Invoice case is created and processed. Once the case is resolved, the agent closes the case with appropriate reason. The UR is synced with invoice case details for invoice owners and suppliers to track the status of the UR.

**Parent Topic:**[Universal Request in Accounts Payable Operations](../concept/universal-request-in-apo.md)

**Related topics**  


[Using Invoice Case Management](../concept/use-invoice-case-mgmt.md)

