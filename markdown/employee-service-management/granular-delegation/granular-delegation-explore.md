---
title: Exploring Granular Delegation
description: Use Granular Delegation to allow your employees to delegate their tasks to other employees.
locale: en-US
release: zurich
product: Granular Delegation
classification: granular-delegation
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Granular Delegation, Employee Service Management]
---

# Exploring Granular Delegation

Use Granular Delegation to allow your employees to delegate their tasks to other employees.

The base system provides your employees with the ability to delegate their tasks to other employees. This feature provides flexibility to your employees when:

-   Out-of-the-office
-   Assigned tasks are for the incorrect employee
-   Assigned tasks require escalation

## Tables

Granular delegation introduces two new tables:

-   **Granular Delegate \[sys\_granular\_delegate\]**

    This table specifies:

    -   Who the service delegate is
    -   When the service delegation occurs
    -   What notifications to send the delegate
-   **Delegation Rule \[sys\_delegation\_rule\]**

    This table specifies the condition for which task records are delegated if the rule is used in a delegation.


## Application menu

Users can access the granular delegation tables from the **Granular Delegation** application menu.

-   **Delegation Rules**

    Link to the Delegation Rule \[sys\_delegation\_rule\] table.

-   **Delegation Rule Tables**

    Link to the Delegation Rule Table \[sys\_delegation\_rule\_table\].

-   **My delegates**

    Link to the Delegate \[sys\_granular\_delegate\] table showing records where the current user has delegated tasks to another user.

-   **Delegated to me**

    Link to the Delegate \[sys\_granular\_delegate\] table showing records where the current user is the delegate.


## Approvals and assignments

Granular delegation allows you to delegate approvals and assignments separately. Task records include extensions of the Task table such as Change, Incident, and Problem records. Use a delegation rule to grant a delegate approval or assignment authority.

**Note:** Flows and workflows ignore delegation rules. If you use flows or workflows to manage task approvals or assignments, you must use the existing service delegation features instead.

-   **Approvals**

    Approval authority allows a delegate to approve or reject approval requests. Add delegation rule conditions to specify which records your delegate can approve. Only records matching the condition appear in the delegate's list of approvals.

    **Note:** A user must have the approval\_user or business\_stakeholder role to approve IT requests \(does not apply to HR approvals\) on Employee Centre. This role validation has not been implemented in Core UI 16 because modifying ACLs in UI16 might have broader implications at the NowPlatform level.

-   **Assignments**

    Assignment authority grants a delegate access to the task records assigned by delegation. Add delegation rule conditions to specify which records your delegate has access to work on. Only records matching the condition appear in the delegate's list of task assignments.


Granular delegation does not change a delegate's access to records. To access records, a delegate must already have the necessary roles. For example, to delegate task records, a delegate must have a role such as itil to access the Task table and its extensions.

Some HR records explicitly grant access to delegates.

## Notifications

Each time you authorize a delegate, the delegate receives the following **email** notifications:

-   **Start of delegation**

    The delegate receives a notification at the start of the delegation period.

-   **Assignment by delegation**

    The delegate receives a notification each time an approval or task is assigned.

    You can also specify additional notifications options.

-   **All notifications**

    Option to send the delegate a copy of all notifications you receive during the delegation period. Select this option when you want the delegate to receive the delegation notification. For example, you want the delegate to receive notifications about activity stream or record updates. It is set to False by default to avoid concerns around getting notifications that has critical and sensitive data.

    All columns are contained in the Granular Delegate \[sys\_granular-delegate\] table.

    **Note:** Notifications with the **Exclude Delegates** option enabled override the True setting of this option. Use the **Exclude Delegates** option to prevent delegates from seeing confidential or protected information.

-   **Meeting invitations**

    Option to forward delegates meeting invitations. Select this option to forward the delegate any meeting invitations the instance generates or receives for you. It is set to False by default.


## System property

Administrators can specify which versions of service delegation they want to support from the glide.approval.delegation.version system property.

The glide.approval.delegation.version system property specifies the service delegation features to support. Choices include `v1`, `v2`, and `v3`.

Enter `v1` to support only the prior service delegation features. This value disables support for granular delegation features.

Enter `v2` to support only granular delegation feature. This value disables support for the existing service delegation features.

Enter `v3` to support both granular and existing service delegation features.

-   Type: string
-   Default value: v3
-   Choices: v1, v2, v3
-   Location: System properties

## Scheduled jobs

The following scheduled jobs are provided:

-   Notify new delegates
-   Clean Granular Delegation Records

## E-signature support

Granular delegation supports Approvals with e-Signature \(com.glide.e\_signature\_approvals\). When enabled, the system requires delegates to enter their credentials to fulfill an approval.

