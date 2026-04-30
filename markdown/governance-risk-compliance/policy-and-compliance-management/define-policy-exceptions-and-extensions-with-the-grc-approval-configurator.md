---
title: Define policy exceptions and extensions with the GRC Approval Configurator
description: If you're a compliance manager, you can define the policy exceptions and extensions for granular, multi-level approval workflows by using the GRC Approval Configurator. The GRC Approval Configurator is a tool within the Governance, Risk, and Compliance application.
locale: en-US
release: yokohama
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2025-09-29"
reading_time_minutes: 5
breadcrumb: [Policy and Compliance Management enhancement steps, Implement, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Define policy exceptions and extensions with the GRC Approval Configurator

If you're a compliance manager, you can define the policy exceptions and extensions for granular, multi-level approval workflows by using the GRC Approval Configurator. The GRC Approval Configurator is a tool within the Governance, Risk, and Compliance application.

## GRC Approval Configurator Overview

A policy exception is a formal, temporary authorization to deviate from a standard policy or procedure, typically for a defined business reason or in response to an issue. A policy extension is a request to prolong the duration of an existing policy exception, requiring a re-assessment of the situation and potentially another approval. Both processes can be handled by using the GRC Approval Configurator.

The GRC Approval Configurator enables you to define the approval rules for exceptions and extensions, assign approvals to designated users or groups, and implement multi-level approval flows. Exception and Extension requests are automatically routed based on the configured rules and data within the record, and approvers can directly approve or reject extensions within their workspace.

## Benefits of using the GRC Approval Configurator for policy exceptions and extensions

The GRC Approval Configurator provides the following benefits for managing policy exceptions and extensions:

-   Customized approval processes: Create customized approval rules that are based on specific conditions such as the exception type, requester role, or policy domain. This process helps to control the approval workflow and verify that each request is evaluated appropriately.
-   Multi-level approvals: Configure a workflow that contains sequential approval levels to enable a thorough review and accountability. The workflow can include various stakeholders, such as compliance managers, subject matter experts \(SMEs\), and designated approvers.
-   Dynamic rule-based approvals: Set up multi-level approval rules that are based on dynamic conditions. For example, an approval workflow can be sent to users or groups that are selected from fields in the source record, or can be assigned to users or groups that you select manually. You can also configure whether only one approval or all approvals are required at each level.
-   Automated routing: Automate direct exception and extension requests to the relevant approvers based on the configured rules. The automated routing reduces manual effort and minimizes delays.
-   Workspace integration: Enable your approvers to review and act on requests directly within their workspace so that you can help to maintain a clear audit trail and improve operational efficiency.

## Workflow for policy exception approvals

The policy exception approval process consists of the following states:

-   New: When a policy exception is created, it enters the New state.

    At this stage, the verification approvals are triggered to validate whether the exception request is legitimate. These approvals are created by using the Verification Configuration template.

-   Analyze: After the verification is complete and approved \(based on the verification rule\), the request moves to the Analyze state.

    In this state, a compliance manager evaluates the request. If additional domain-specific insight is needed, they can either move it to the Review state for further analysis, or request input from an SME.

-   Review: In this state, the request is reviewed in detail by the SME for technical validation.
-   Awaiting Approval: After the SME input is gathered, the request enters the Awaiting Approval state for gathering the final approvals from the designated approvers \(based on the final approval configuration rules\).

-   Approved: After final approval, the policy exception is marked as Approved and becomes active.

-   Closed: When the exception is no longer required, it's moved to the Closed state.

## Workflow for policy extension approvals

You can extend approved extensions through a similar approval process. Extension requests are routed by using the same GRC Approval Configurator. You can configure multiple approvers or groups to approve or reject extension requests.

## Roles required for configuring policy exceptions and extensions

To configure policy exceptions and extensions, you must have the following roles:

-   sn\_compliance.manager to create approval rules.
-   sn\_grc.business\_user or sn\_grc.business\_user\_lite to view exception and extension records.

## Configuring policy exceptions and extensions

After you have the required roles, you can then configure the policy exceptions and extensions by using the Approval Configurator.

[Enable the GRC Approval Configurator](../task/enable-grc-approval-configurator.md)

Enable the GRC Approval Configurator so that you can manage policy exceptions and extensions with granular, multi-level approval flows.

[Define the policy verification rules](../task/define-policy-exception-verification-rules.md)

Configure granular approval rules for policy exception verification rules by using the GRC Approval Configurator.

[Define the policy exception approval rules](../task/define-approval-rules-grc-config.md)

Configure granular approval rules for policy exception approval rules by using the GRC Approval Configurator.

[Define extension rules for policy exceptions](../task/define-policy-exception-extension-rules.md)

Enable the GRC Approval Configurator from the Policy and Compliance Properties page to allow multiple approvers for policy extension approvals, replacing the single default approver \(Compliance Manager\).

-   **[Enable the GRC Approval Configurator](../task/enable-grc-approval-configurator.md)**  
Enable the GRC Approval Configurator so that you can manage policy exceptions and extensions with granular, multi-level approval flows.
-   **[Define the policy verification rules](../task/define-policy-exception-verification-rules.md)**  
Configure granular approval rules for policy exceptions and extensions by using the GRC Approval Configurator. This allows you to manage approvals with precise rule definitions and support multi-level approval workflows.
-   **[Define the policy exception approval rules](../task/define-approval-rules-grc-config.md)**  
Approval rules define how policy exception requests are reviewed and approved, enabling organizations to create customized, multi-level workflows.
-   **[Define extension rules for policy exceptions](../task/define-policy-exception-extension-rules.md)**  
Enable the GRC Approval Configurator from the Policy and Compliance Properties page to allow multiple approvers for policy extension approvals, replacing the single default approver \(Compliance Manager\).

**Parent Topic:**[Policy and Compliance Management enhancement steps](../../grc-policy-compliance-implementation/concept/policy-compliance-optional-steps.md)

