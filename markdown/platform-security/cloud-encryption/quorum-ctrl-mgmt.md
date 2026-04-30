---
title: Manage Quorum Control
description: After a withdrawal operation workflow is triggered, quorum actions can be managed from the Key Management Operations page. The key withdrawal operation is blocked until the quorum is met.
locale: en-US
release: yokohama
product: Cloud Encryption
classification: cloud-encryption
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Quorum Control Policy, Cloud Encryption with Key Management, Encryption]
---

# Manage Quorum Control

After a withdrawal operation workflow is triggered, quorum actions can be managed from the Key Management Operations page. The key withdrawal operation is blocked until the quorum is met.

## Before you begin

Role required: sn\_kmf.admin or sn\_kmf.cryptographic\_manager

When the quorum has been either approved or rejected, the requestor of the key withdrawal will receive an email notating if quorum was achieved or denied.

## Procedure

1.  Perform the steps to withdraw a customer managed key found in [Key management operations](key-mgmt-operations-ce.md#).

2.  View the Quorum Control Requests and Quorum Control Approvers tabs that activated. ![Shows the quorum control tabs.](../image/key-def-table.png)

3.  Open the **Quorum Control Requests** tab to view the actual request that is created.

    -   State:
        -   Open: The key withdrawal action is pending the quorum being met.
        -   Closed Complete: The quorum has been met and can be no further action on this particular quorum request.
    -   Approval:
        -   Requested: Approval emails have been sent and the workflow has been triggered to reach quorum.
        -   Approved: The key will be withdrawn and the instance will be shut down.
        -   Denied: The quorum request is canceled and no further action is taken with this request. A new withdrawal request will be required to withdraw the key.
4.  Open the Quorum Control Approvers tab to view the list of approvers and the state of the approval request.![Displays entries for the quorum control approvers.](../image/quorum-ctrl-approvers.png)

    State:

    -   Requested: The approver has not yet taken action on the approval request.
    -   Approved: The request has been approved either from the email or the approvals page.
5.  Select the **Key Management Transactions** tab to view the progress of the request step for the key withdrawal.

    -   Step 0 - Quorum Request: The actual quorum request. The quorum request must be completed in order to trigger the key withdrawal steps.
    -   Step 1 - Key Withdrawal: The key withdrawal step. This is composed of steps two through seven.
    -   Step 2 - Request\_preparation: Creates a request to trigger and the wrapping and rotation.
    -   Step 3 - request\_integrity\_check: Validates that the request is legitimate and secure.
    -   Step 4 - request\_validation: Validates that there is a request in progress, only one rotate request can process at a time.
    -   Step 5 - hsm\_key\_delete: Makes the call to KeySecure to delete the active key.
    -   Step 6 - key\_metadata\_withdraw: Converts the active key metadata lifecycle state to "destroyed."
    -   Step 7 - post\_withdraw: Makes a call to shut down the instance.

-   **[Approve or deny a quorum control request](quorum-transactions-approval.md)**  
Approve or deny a quorum control request from Key Management Transactions.
-   **[Approve or deny a quorum request](perform-quorum-action.md)**  
When a quorum request has been created, the minimum number of approvals is required by the members. After a withdrawal operation workflow is triggered, quorum actions can be managed using several methods. The users can grant approvals from the Key Management Operations page, **My Approvals** in the Instance, or directly from the request email. The key withdrawal operation is blocked until the quorum is met.

**Parent Topic:**[Quorum Control Policy](../concept/quorum-ctrl-policy.md)

