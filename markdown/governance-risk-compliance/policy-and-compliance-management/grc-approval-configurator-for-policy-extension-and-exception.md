---
title: GRC Approval Configurator for approving policy exceptions and extensions
description: Users can now manage policy exceptions and extensions with granular, multi-level approval flows using the GRC Approval Configurator.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Enhancement steps, Implement, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# GRC Approval Configurator for approving policy exceptions and extensions

Users can now manage policy exceptions and extensions with granular, multi-level approval flows using the GRC Approval Configurator.

Users can now configure policy exceptions and extensions through the GRC Approval Configurator. The GRC Approval configurator enables more granular rule definitions and broader configuration options for policy exceptions and extensions.

The GRC Approval Configurator allows users to define approval rules for exceptions and extensions, assign approvals to designated users or groups, and implement multi-level approval flows. Exception and Extension requests are automatically routed based on the configured rules, and approvers can directly approve or reject extensions within their workspace.

## Benefits of Using Approval Configurator for Policy Exceptions and Extensions

The GRC Approval Configurator provides several benefits when managing policy exceptions and extensions, including:

-   Customized approval processes: Create tailored approval rules based on specific conditions such as exception type, requestor role, or policy domain. This allows for precise control over the approval workflow and ensures that each request is evaluated appropriately.
-   Multi-level approvals: Configure sequential approval levels involving various stakeholders—such as Compliance Managers, Subject Matter Experts \(SMEs\), and designated approvers—to ensure thorough review and accountability.
-   Dynamic rule-based approvals: Set up multi-level approval rules based on dynamic conditions. Approvals can be sent to users or groups selected from fields in the source record, or manually assigned. You can also configure whether only one approval or all approvals are required at each level.
-   Automated routing: Automatically direct exception and extension requests to the relevant approvers based on predefined rules. This reduces manual effort and minimizes delays.
-   Workspace integration: Approvers can review and act on requests directly within their workspace, maintaining a clear audit trail and improving operational efficiency.

## Workflow for policy exception approvals

The policy exception approval process consists of five main states:

-   New: When a policy exception is created, it enters the New state.

    At this stage, verification approvals are triggered to validate whether the exception request is legitimate. These approvals are created using the Verification Configuration template.

-   Analyze: After the verification is complete and approved \(based on the verification rule\), the request moves to the Analyze state.

    Here, a Compliance Manager evaluates the request. They can either move it to the Review state for further scrutiny, or request input from a Subject Matter Expert \(SME\) if additional domain-specific insight is needed.

-   Review: In this state, the request is reviewed in detail by the SME for technical validation.
-   Awaiting Approval: After the SME input is gathered, the request enters the Awaiting Approval state for gathering the final Approvals from designated approvers \(based on the final approval configuration rules\).

-   Approved: After final approval, the policy exception is marked as Approved and becomes active.

-   Closed: After the exception is no longer required, After the exception or extension is no longer needed, it is moved to the Closed state.

## Workflow for policy extension approvals

Approved exceptions can be extended through a similar approval process. Extension requests are routed using the same GRC Approval Configurator. Multiple approvers or groups can be configured to approve or reject extension requests.

## Configuring policy exceptions and extensions

You can set up the approval rules using the Approval Configurator:

-   Enable the GRC Approval Configurator from the Policy and Compliance Properties page. For more information, see [Enable GRC Approval Configurator](../task/enable-grc-approval-configurator.md).
-   Configure granular approval rules for policy exceptions and extensions using the GRC Approval Configurator. For more information, see [Define policy exception and extension rules](../task/define-policy-exception-verification-rules.md).
-   -   
## Roles required for configuring policy exceptions and extensions

Users must have the following roles:

-   sn\_compliance.manager to create approval rules.
-   sn\_grc.business\_user or sn\_grc.business\_user\_lite to view exception and extension records.

-   **[Enable GRC Approval Configurator](../task/enable-grc-approval-configurator.md)**  
Enable the GRC Approval Configurator from the Policy and Compliance Properties page.
-   **[Define policy exception and extension rules](../task/define-policy-exception-verification-rules.md)**  
Configure granular approval rules for policy exceptions and extensions using the GRC Approval Configurator.

**Parent Topic:**[Policy and Compliance Management enhancement steps](../../grc-policy-compliance-implementation/concept/policy-compliance-optional-steps.md)

