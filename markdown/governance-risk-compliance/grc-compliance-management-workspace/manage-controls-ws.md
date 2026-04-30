---
title: Manage controls using the Compliance Workspace
description: Controls are specific implementations of a control objective. Retired controls do not appear in the list. Before defining controls, take time to rationalize, consolidate, and define the important controls in your organization.
locale: en-US
release: zurich
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Use, GRC Compliance Workspace, Use, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Manage controls using the Compliance Workspace

Controls are specific implementations of a control objective. Retired controls do not appear in the list. Before defining controls, take time to rationalize, consolidate, and define the important controls in your organization.

## Rationalize your controls

If you upload all your controls in bulk, you are missing the opportunity to refine and streamline your controls set.

-   How does this control affect my business objective?
-   Is this control actually preventing or detecting risk?
-   Is there a different control you can place that better protects your business?
-   Is there a control you can put in place that reduces process overhead and improves IT performance while also mitigating risk?
-   Can a complicated control be replaced with a simpler more effective control?

As your business changes, and your IT data, processes, and technology improve, replace outdated controls and procedures.

**Note:** When you define controls manually or when you import them from the Unified Compliance Framework \(UCF\), an entity is associated with the controls. It is a mandatory field on the Control form. If, however, you import controls from a source other than the UCF, you may encounter controls that do not have associated entities. It is important that you return to the Control form and [add an entity to the control](../task/create-control-ws.md). Missing entities can cause unreliable results in calculations. Also, if you encounter a control with an entity that has been disabled, the control should be retired.

## Consolidate your controls

Look for opportunities to consolidate controls. Look for common, repeated controls across multiple regulatory authorities of frameworks \(for example, SOX and GLBA and AML\). Avoid operating a single control multiple times for each regulation, by cross-mapping controls and eliminating the redundant ones. This process establishes a single consolidated set of controls = control framework, performing and preserving the cross mapping of controls is critical for audits.

![Industry regulations and requirements overlap](../../grc-common/image/industry-regulations.png "Industry regulations and requirements overlap")

## Define controls and business rules

The business rules you define up front, establish the GRC configuration settings later. Be prepared to:

-   Identify controls and control owners
-   Define control tests and expected results
-   Establish test and control frequencies
-   Identify risks: impact and likelihood
-   Prepare attestations, assessments, questionnaires, and required evidence
-   Compose likely use-cases \(who needs to interact with or view the contents of the GRC system and for what purposes\)
-   Map authoritative sources to policies, to procedures, to controls, and to risks

## Control requirements

When Create control requirements option is enabled for a control objective, for every control generated under an entity type, control requirements are also created automatically. Previously, only controls were created for entity types. The number of Control Requirements equals the number of control objective requirements.

## Attestation at control requirement level

The Attestation at control requirement level feature allows attestation at a granular level for individual control requirements within a control. Admins can enable requirement-level attestation, assign respondents, and generate assessment tasks for each control requirement. Respondents then attest to requirements by indicating whether they are implemented or not, providing evidence or explanations as required. Failed attestations automatically generate issues, mark the parent control as non-compliant, and roll up the status to the associated entity and control objective.

## Entity Based Access \(EBA\)

The Entity Based Access feature provides a framework for more granular approach to management of data access to objects associated with an entity. Administrators can grant access to an entity's related records by adding users or user groups, or by using entity user fields for entity-based access configuration. For more information, see [Entity Based Access](../../grc-common/concept/entity-based-access.md).

When a user is qualified based on these configurations and has the minimum required roles, they will have access to the following tables:

-   Control
-   Attestation
-   Policy exception to control

## Entity Based Access \(EBA\) rules

When entity based record access rules are enabled on the **Entity Based Access Configuration Properties** page, any newly created controls, control attestations, indicators, and indicator tasks associated with a configured entity will automatically inherit the entity-based access \(EBA\) value from that entity. Previously, users had to run bulk access updates to apply EBA restrictions whenever new objects were created.

For more information, see [Entity based record access rules to secure new records](../../grc-common/concept/continuous-monitoring-of-entity-based-access.md).

