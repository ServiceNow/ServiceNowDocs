---
title: Delegation of legal duties and approvals
description: Legal fulfillers can delegate their legal duties to other users while they are unavailable. The delegate gets the same level of access as the legal fulfillers to work on their legal requests, legal matters, legal matter tasks, and approvals.
locale: en-US
release: zurich
product: Legal Request Management
classification: legal-request-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Legal Request Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Delegation of legal duties and approvals

Legal fulfillers can delegate their legal duties to other users while they are unavailable. The delegate gets the same level of access as the legal fulfillers to work on their legal requests, legal matters, legal matter tasks, and approvals.

Legal Service Delivery supports the following delegations:

-   **ServiceNow AI Platform delegation**

    This delegation method is active by default. This delegation enables lawyers to delegate all items to the delegate. However, while adding a delegate, lawyers can limit the delegation options:

    -   Delegate only approvals
    -   Delegate only assignments
    -   Delegate both approvals and assignments
    -   Delegate notifications
-   **Granular delegation**

    Granular delegation enables lawyers to choose which items from their assigned legal requests, legal matters, legal matter tasks, and approvals they want to delegate.

    **Note:** This delegation method requires activation of the Granular Delegation plugin \(com.glide.granular\_service\_delegation\).

    Before lawyers can use the delegation, the administrator must configure the delegation rule tables, delegation rules, and the **My Delegate** workspace list in the Legal Counsel Center Classic Workspace:

    -   Set the **My Delegate** workspace list on the Granular Delegate \[sys\_granular\_delegate\] table as active.
    -   Set the **My Delegate** workspace list on the Delegate \[sys\_user\_delegate\] table as inactive.
    For the new experience Legal Counsel Center Workspace, open **&lt;instance&gt;/sys\_ux\_list\_list.do?sysparm\_query=titleLIKEMy%20Delegates**.

    The **My Delegate** UX list must be configured as follows:

    -   The **My Delegates** list on the Granular Delegate \[sys\_granular\_delegate\] table must be active.
    -   The **My Delegates** list on the Delegate \[sys\_user\_delegate\] table must be inactive.
    A task is delegated when it matches the delegation rules specified for a delegation. For example, you can delegate only the Privacy Assessment requests. A delegation rule can be set on the Legal Request \[sn\_lg\_ops\_request\] table with the condition as **\[Category\] \[is\] \[Privacy\]**.


-   **[Delegate legal duties to another user](../task/delegate-legal-duties-approval.md)**  
Delegate legal duties relating to your assigned legal requests, legal matters, legal matter tasks, and approvals to another user when you might not have time or are unavailable.
-   **[Delegate specific legal duties to another user using granular delegation](../task/delegate-legal-duties-approval-granular.md)**  
Delegate specific legal duties relating to your assigned legal requests, legal matters, legal matter tasks, and approvals to another user when you might not have time or are unavailable. These specific duties are derived from the pre-defined delegation rules.
-   **[View and work on delegated legal duties](../task/view-delegated-legal-duties-approval.md)**  
Delegate legal duties relating to your assigned legal requests, legal matters, legal matter tasks, and approvals to another user when you might not have time or are unavailable.

**Parent Topic:**[Configuring Legal Request Management](legal-ops-administration.md)

**Related topics**  


[Setting up Granular Delegation](../../employee-service-management/granular-delegation/concept/granular-delegation-setup.md)

