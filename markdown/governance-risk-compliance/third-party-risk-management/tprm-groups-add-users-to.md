---
title: Add users to groups based on responsibilities
description: Assign users to groups before you implement or use the Third-party Risk Management application. Each group contains users with particular roles. Well-organized user groups simplify and improve process management and help to ensure that users are promptly notified of tasks in their areas of responsibility.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Add users to groups based on responsibilities

Assign users to groups before you implement or use the Third-party Risk Management application. Each group contains users with particular roles. Well-organized user groups simplify and improve process management and help to ensure that users are promptly notified of tasks in their areas of responsibility.

## Before you begin

Role required: admin

## About this task

Several user groups are created when you activate the TPRM app. In this procedure, you add users to each group. The roles mentioned in this procedure are described in [Roles in Third-party Risk Management](../reference/tprm-roles.md).

There’s an important practical result of including all users with a particular role in a group: Your risk management process isn’t affected when one or more members of the group are unavailable due to vacation, for example.

**Important:** Consider this to be an ongoing process, where the user who is assigned as the group manager is responsible for continuously updating group membership.

-   **Due diligence request assigners**

    Group members have the Third-party risk \(TPR\) assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role.

    Each member receives email notification of new requests for due diligence. For requests in the **New** or **Unassigned** state, no one has been specified in the **Assigned to** field. Any group member can assign or be assigned to a request.

    The individual who owns an assessment for audit purposes and monitors and manages overall assessment processes. The owner is responsible for confirming that the assessment is completed in a timely fashion by the third party, reviewing their responses, and creating and resolving issues. To drive the assessment to its completion, they are notified when an assessment reaches a particular milestone. They must have the TPR manager or TPR assessor role.

-   **Third-party Risk Managers**

    Group members have both the TPR approver role \[sn\_vdr\_risk\_asmt.approver\] and the TPR manager role \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\].

    Members can monitor and manage overall due diligence processes and approve new requests for due diligence.

-   **Third-party Risk Reviewers \(External assessment reviewers\)**

    Group members have the Third-party assessment reviewer role \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\].

    Members can monitor and manage interactions with third-party contacts during external due diligence processes.

-   **Contract risk negotiators**

    Group members have the Contract risk negotiator \[sn\_vdr\_risk\_asmt.contract\_negotiator\] role.

    Members work in the contract risk process.


## Procedure

1.  Navigate to **All** &gt; **Third-party Risk Management** &gt; **Administration** &gt; **User Groups**.

    The list of user groups appears.

    ![Pre-defined user groups for TPRM.](../image/tprm-groups.png)

2.  Select the name of the group to update.

3.  Specify a manager for the group.

    The group manager is responsible for continuously updating group membership. The group manager typically has the same role \(or higher\) as the members.

4.  Specify an email alias for the group.

    -   If you don’t specify an alias, then a separate email notification is sent to each member.
    -   If you specify an alias, then a single email notification is sent with all members in the **To:** list.
5.  On the Group Members related list, select **Edit**.

6.  Move all appropriate users from the **Collection** list to the **Group Members** list and then select **Save**.

7.  Use the Groups related list to add subgroups to the group that you’re defining.

    This option enables you to organize users into practical subsets.

8.  Repeat the process for each group.


**Related topics**  


[Roles in Third-party Risk Management](../reference/tprm-roles.md)

[TPRM and the Explicit Roles plugin](../../grc-vendor-risk/concept/vrm-and-explicit-roles-plugin.md)

