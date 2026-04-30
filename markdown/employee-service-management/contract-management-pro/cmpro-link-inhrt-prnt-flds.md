---
title: Link and inherit parent contract fields
description: Link parent contracts during drafting and negotiation phases to establish hierarchical relationship between the parent and child contracts, and automatically inherit the configured fields from the parent contract.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-06-15"
reading_time_minutes: 1
breadcrumb: [Linking parent-child contracts, Using Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Link and inherit parent contract fields

Link parent contracts during drafting and negotiation phases to establish hierarchical relationship between the parent and child contracts, and automatically inherit the configured fields from the parent contract.

## About this task

The following video walks you through the process of linking a parent contract request and inheriting its fields.Video providing step-by-step instructions on linking parent contract request and inheriting its fields, approximately one and a half minutes long. 

## Before you begin

Ensure that the contract request is in Draft, Work in progress, or Awaiting review state.

You must be either assigned to the contract request or a group manager or a collaborator.

Ensure that the parent contract is not a multiple contracts type third-party contract request.

Ensure that the parent child mapping is configured. For more information, see [Configure field mapping for parent-child contract linking](cncor-conf-parent-child.md).

Role required: sn\_cm\_core.contract\_fulfiller

## Procedure

1.  Open the contract request from workspace that you are using.

<table id="choicetable_zst_kcr_5bc"><thead><tr><th align="left" id="d66043e86">

Method

</th><th align="left" id="d66043e89">

Steps

</th></tr></thead><tbody><tr><td id="d66043e95">

**Contract Workspace listing**

</td><td>

1.  Navigate to **All** &gt; **Contract Workspace**.
2.  Click the list icon \(![List icon](../../legal-request-management/image/lsd-lcc-list-icon.png)\).
3.  Select **Contract requests** &gt; **All**
4.  Select a contract request.


</td></tr><tr><td id="d66043e142">

**Workspace used by your application**

</td><td>

1.  Navigate to your workspace.
2.  Open the list that displays the contract requests.
3.  Select a contract request.


</td></tr></tbody>
</table>2.  Select the Related contract requests tab.

3.  Select **Link parent contract**.

4.  In the Link contract window, select the check box corresponding to the contract request that you want to link as a parent contract.

    **Note:** You can select only one contract request when linking it as a parent contract.

    ![Link contract window for linking and inheriting fields from the parent contract.](../image/cmpro-link-contract.png "Link contract window")

5.  Select **Link and inherit fields**.

    The selected contract request is linked as a parent contract and its fields are inherited by the child contract. The parent-child relationship appears in a hierarchical order in the Related contract requests tab.

    The associated contract repository records for the contract requests will be automatically linked.

    The **Parent contract request** field is updated with the parent contract request number. The linked parent contract details appear in the activity stream.

    ![Parent-child hierarchy in the Related contract requests tab](../image/cmpro-parent-child-link.png "Parent-child hierarchy")


**Parent Topic:**[Linking parent-child contracts](../concept/cmpro-linking-parent-child.md)

