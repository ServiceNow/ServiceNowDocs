---
title: Linking parent-child contracts
description: The contract family hierarchy in the Related contract requests tab shows all related contract requests and lets you link, inherit from, and unlink parent contract requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/contract-management-pro/cmpro-linking-parent-child.html
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2026-06-11"
reading_time_minutes: 3
keywords: [contract family hierarchy, related contract requests, parent child sibling contracts, link parent contract, contract hierarchy view]
audience: sn\_cm\_core.contract\_fulfiller
breadcrumb: [Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Linking parent-child contracts

The contract family hierarchy in the Related contract requests tab shows all related contract requests and lets you link, inherit from, and unlink parent contract requests.

When you open a contract request and navigate to the **Related contract requests** tab, the tab displays the complete contract family hierarchy for that contract request. The hierarchy includes parent, child, sibling, and grandchild records.

From the same tab, you can link a parent contract request, inherit fields from it, or remove an existing link. When linked, the **Parent contract** field in the contract request Details tab is automatically populated with the parent contract request number. The associated contract repository records for the parent and child contract requests are also automatically linked.

The **Related contract requests** tab displays the following records:

-   The parent contract request of the currently open record
-   All sibling contract requests — other children of the same parent
-   Children and grandchildren of sibling records
-   Direct children and grandchildren of the currently open record

A visual indicator highlights the contract request that is currently open, distinguishing it from other records in the hierarchy.

## Access control for related contract requests

The **Related contract requests** tab displays only the contract records within the family hierarchy that you have access to. Records you're not authorized to view aren't displayed.

Access to a contract request is determined by your role in that contract request. You can view a contract request in the hierarchy if you're one of the following:

-   The assigned contract fulfiller
-   A group manager or fulfiller of the assignment group
-   A collaborator
-   A watchlist user
-   The requested-for user
-   The opened-by user

## Amendments in the hierarchy

When you create an amendment contract request, it is automatically created as a child record of the originating contract request and appears in the hierarchy on the **Related contract requests** tab.

## Choosing a linking action

The **Related contract requests** tab provides two linking actions.

<table id="cmpro-linking-parent-child-table-1"><thead><tr><th>

Action

</th><th>

Use when

</th><th>

Additional prerequisites

</th></tr></thead><tbody><tr><td>

**Link contract**

</td><td>

You want to establish the parent-child relationship only, without copying any fields from the parent.

</td><td>

The parent can be a contract request in any state except Cancelled. If the child contract is in Contract signed state, the parent must be in Contract signed or Closed complete state.

</td></tr><tr><td>

**Link and inherit fields**

</td><td>

You want to establish the parent-child relationship and automatically copy configured fields from the parent into the child contract request.

</td><td>

Contract request must be in Draft, Work in progress, or Awaiting review state only.Parent-child field mapping must be configured. For more information, see [Configure field mapping for parent-child contract linking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contract-management-pro/cncor-conf-parent-child.md).

The parent must not be a multiple contracts type third-party contract request.

</td></tr></tbody>
</table>The following conditions apply to both actions:

-   You must be assigned to the contract request, be a group manager, or a collaborator.
-   The parent contract must not be in a Canceled state.
-   Only one parent contract can be selected while linking.
-   The parent contract must be a single contract type using own paper or third-party paper.
-   A contract can't be linked as a parent of any contract before it in the hierarchy. For example, if Master Service Agreement \(MSA\) is the parent of Statement Of Work \(SOW\), then SOW can't be set as the parent of MSA.

-   **[Link parent contract requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contract-management-pro/cmpro-link-parent-cmr.md)**  
Link parent contracts during drafting and negotiation phases to establish hierarchical relationship between the parent and child contracts.
-   **[Link and inherit parent contract fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contract-management-pro/cmpro-link-inhrt-prnt-flds.md)**  
Link parent contracts during drafting and negotiation phases to establish hierarchical relationship between the parent and child contracts, and automatically inherit the configured fields from the parent contract.
-   **[Remove a linked contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contract-management-pro/cmpro-remove-linked-cntr.md)**  
Remove a linked parent contract from contract requests when you have linked a wrong contract request or the linking is no longer required.

**Parent Topic:**[Using Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contract-management-pro/cncore-use-cmpro.md)

**Related topics**  


[Link parent contract requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contract-management-pro/cmpro-link-parent-cmr.md)

[Link and inherit parent contract fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contract-management-pro/cmpro-link-inhrt-prnt-flds.md)

[Remove a linked contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contract-management-pro/cmpro-remove-linked-cntr.md)

[Configure field mapping for parent-child contract linking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contract-management-pro/cncor-conf-parent-child.md)

