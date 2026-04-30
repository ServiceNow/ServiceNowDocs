---
title: Set up dynamic approval configuration on a policy record
description: A policy is a set of guidelines and rules established by a business organization to govern its operations. Creating an approval configuration record for a policy enables you to define one or more approval levels and approval rules based on various dynamic conditions.
locale: en-US
release: zurich
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Enhancement steps, Implement, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Set up dynamic approval configuration on a policy record

A policy is a set of guidelines and rules established by a business organization to govern its operations. Creating an approval configuration record for a policy enables you to define one or more approval levels and approval rules based on various dynamic conditions.

Beginning with the Zurich release, you can set up dynamic approval configuration on a policy record. The policy table consists of the policy records that regulate the status of the policies. Before implementing a policy, it goes through a review and approval process.

Setting up dynamic approval configuration on a policy record enables you to define multiple levels of approvals based on various dynamic conditions such as policy type, state, and owner that are related to the policy fields. When you set up dynamic approval configuration on a policy record, the approvers for a policy are added dynamically to the policy record.

## Limitations of adding the approvers manually

The existing approval configuration process uses the manual approach that has the following limitations:

-   The approval configuration process uses a single level of approval. If multiple levels of approval are not used, it increases the possibility of introducing errors and oversights in the approval process.
-   The approvers for a policy cannot be changed based on dynamic or changing conditions of the approval process.
-   The approvers are added manually to the record. The process can be time consuming, especially in large organizations or complex decision-making structures.
-   Adding the approvers manually can lead to significant delays. Waiting to receive all approvals can slow down the decision-making process and decrease productivity.

## Benefits of dynamic approval configuration

Setting up dynamic approval configuration on a policy record offers the following benefits:

-   Organizations often encounter dynamic and changing environments. Having the flexibility to change the approvers allows the approval process to adapt to shifting circumstances. It ensures that the most appropriate individuals are involved in the approval process at any given time.
-   For complex or high-stake decisions, configuring multiple levels of approvals enables the reviewers to conduct a comprehensive review of relevant factors. It ensures that the decisions are not rushed and that the potential impacts are carefully assessed for different scenarios.
-   Changing the approvers dynamically can streamline the approval process and reduce the administrative overhead, thereby saving time and resources.

## Use cases for requesting multiple levels of approvals

Approval configuration can help create complex approval levels without manually adding approvers for each policy. In some cases, a policy owner may want to conduct multiple levels of approvals for a policy. For example, a policy is related to the HR domain. The compliance team, legal team, and HR team want to review and approve it. The policy owner can assign the HR team as Level 1 approvers of the policy.

When the HR team approves the policy, it is assigned to the Compliance team for Level 2 approval. It is then assigned to the legal team for Level 3 approval of the policy. Also, the policy owner may want to select the approvers dynamically based on certain rules that match with the policy.

This use case highlights the importance of integrating dynamic approval configuration with a policy and configuring the policy approval rules with Approval Configurator.

## Approval configurator

To use the approval configuration, the approval method on the policy should be selected as **Use approval rule** as shown in the following example.

![Use approval rule.](../image/use-approval-rule.png)

Approval configuration should be created for the policy and valid approval rules should be configured for the users.

Use the **Policy Approval Rules** module to configure the approval rules.

## Configuring policy approval rules using Approval Configurator

You can set up various approval rules using the Approval Configurator:

-   Set up multi-level approval rules based on dynamic conditions.
-   Send approvals to a user or a group of users selected from a field from the source record or select the user or groups manually.
-   Set up only one approval or all approvals as required approvals.

To set up approval configuration on a record, see the following sections.

1.  To set up an approval configuration record, see [Set up an approval configuration record](../../grc-common/task/set-up-approval-configurator.md).
2.  To assign an approval level for the approval configuration record, see [Assign an approval level for the approval configuration record](../../grc-common/task/set-up-approval-levels.md).
3.  To set up an approval rule for the approval level in the approval configuration record, see [Set up an approval rule for the approval level](../../grc-common/task/set-up-approval-rules.md).

**Note:**

For more information on the roles in the GRC: Approver Configurator application, see [Roles installed with GRC: Approver Configurator](../../grc-common/reference/roles-installed-with-approver-configurator.md).

## Roles required for creating policy approval rules

To create the policy approval rules, the following roles are required:

-   A user with the sn\_compliance.manager role can create policy approval rules with the sn\_grc\_appr.admin role.
-   Users with the sn\_grc.business\_user and sn\_grc.business\_user\_lite and above roles can view a policy.
-   A user should have mp\_document\_user with either the sn\_grc.business\_user or sn\_grc.business\_user\_lite role to access the document when redlining is enabled.

## Workflow for setting up approval configuration

When you set up approval configuration on a policy record, the workflow contains the following steps.

1.  When an approval is requested for a policy record, the state of the policy changes to the **Awaiting approval** state.
2.  If the approval method is selected as **Use approvers**, it uses the approvers mentioned in the policy record.
3.  If the approval method is selected as **Use approval rule**, it checks for a valid configuration that suits the policy record. The dynamic approval configuration searches for the approval configuration record that is related to the policy.
4.  The dynamic approval configuration then retrieves the approvers from each approval level record and sends an approval request for each level.
5.  If a valid configuration is not found, an error message is displayed that there is no valid configuration for the policy.

The workflow steps are shown in the following example.

![Approval configuration process.](../image/policy-approval-process.png)

If you are the policy owner, you can select the approvers for the policy in the **Approvers** field of the Policy form. The approvers are usually the users who have the Compliance User role. If you do not have proper access, you cannot access the policy record. To request access to the policy record, you must contact the Compliance Administrator.

## Integrating dynamic approval configuration with a policy

To integrate dynamic approval configuration with a policy record, you can set up multiple approval levels and for each level, you can set up the approval rules. Based on the approval levels and rules setup, the approvals are triggered automatically. When one level is approved, the policy record is submitted for the next level of approval.

The workflow for integrating dynamic approval configuration with a policy is shown in the following example and steps.

![Integrating dynamic approval configuration.](../image/integrating-approval-config-with-policy.png)

-   When an approval is requested for the policy, the state of the policy changes to the **Awaiting approval** state.
-   The dynamic approval configuration searches for the approval configuration record that is suitable to the current policy.
-   If dynamic approval configuration is not set up on a policy record or even though it is set up, it is not applicable to that particular policy record, an error message is displayed that no valid configuration is found for the policy record and the record gets aborted. Users have to go back to your policy record and select the approvers or create a valid configuration for the policy record.
-   If dynamic approval configuration is set up, the approvers, approval levels, and rules are added based on the configuration of the approval configuration record.

The complete workflow is shown in the following example.

![Workflow.](../image/approval-config-workflow.png)

## Components used for dynamic approval configuration

The following components are used for setting up the dynamic approval configuration on a policy:

-   The Policy approval rules module creates or checks the approval configurations with the source table as policy.
-   The Policy approval table stores the approvers of each level of the approval configuration. It can be used for tracking the status of the approval levels.
-   Based on the current level decision, the policy either gets forwarded to the next level of approval or if it gets rejected, it is reset to the **Draft** state. If all levels are approved, the policy moves to the **Published** state.

-   **[Policy dynamic approval setup](../task/configure-dynamic-approval-for-a-policy-without-redlining.md)**  
Set up dynamic approval configuration on a policy. Based on the configured approval levels, the Policy and Compliance Management application configures one or more approval rules on the policy record.
-   **[Policy dynamic approval setup with redlining](../task/configure-dynamic-approval-for-policy-redlining.md)**  
Set up dynamic approval configuration on a policy for which redlining is enabled.

**Parent Topic:**[Policy and Compliance Management enhancement steps](../../grc-policy-compliance-implementation/concept/policy-compliance-optional-steps.md)

