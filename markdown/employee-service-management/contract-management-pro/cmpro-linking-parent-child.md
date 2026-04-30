---
title: Linking parent-child contracts
description: Link a parent contract to a child contract to establish hierarchical relationships between contract requests and inherit fields from the parent contract request.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Linking parent-child contracts

Link a parent contract to a child contract to establish hierarchical relationships between contract requests and inherit fields from the parent contract request.

You can associate a contract request with a parent contract from the Related Contract Request tab. When linked, the **Parent contract** field in the contract request Details tab is automatically populated with the parent contract request number. Depending on configuration, child contracts can inherit fields from the parent contract. Additionally, the associated contract repository records for the parent and child contract requests are automatically linked.

To link a contract as a parent, the following conditions must be met:

-   The user must be assigned to the contract request, be a group manager, or a collaborator.
-   The contract request must be in one of the following states: Draft, Work in progress, Awaiting review, or Contract signed.

    **Note:** If the contract request is in Contract signed state, the parent contract request must be in Contract signed or Closed complete state.

-   The parent contract must not be in a Canceled state.
-   Only one parent contract can be selected while linking.
-   The parent contract must be a single contract type using own paper or third-party paper.

-   **[Link parent contract requests](../task/cmpro-link-parent-cmr.md)**  
Link parent contracts during drafting and negotiation phases to establish hierarchical relationship between the parent and child contracts.
-   **[Link and inherit parent contract fields](../task/cmpro-link-inhrt-prnt-flds.md)**  
Link parent contracts during drafting and negotiation phases to establish hierarchical relationship between the parent and child contracts, and automatically inherit the configured fields from the parent contract.
-   **[Remove a linked contract](../task/cmpro-remove-linked-cntr.md)**  
Remove a linked parent contract from contract requests when you have linked a wrong contract request or the linking is no longer required.

**Parent Topic:**[Using Contract Management Pro](cncore-use-cmpro.md)

**Related topics**  


[Link parent contract requests](../task/cmpro-link-parent-cmr.md)

[Link and inherit parent contract fields](../task/cmpro-link-inhrt-prnt-flds.md)

[Remove a linked contract](../task/cmpro-remove-linked-cntr.md)

[Configure field mapping for parent-child contract linking](../task/cncor-conf-parent-child.md)

