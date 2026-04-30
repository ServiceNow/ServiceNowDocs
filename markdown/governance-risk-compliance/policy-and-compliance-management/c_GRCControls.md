---
title: Manage controls
description: Learn how to rationalize, and consolidate controls to build an effective control framework when deploying your GRC application. Use entity-based access to manage control visibility, and ensure all controls are properly mapped to entities to maintain audit reliability.
locale: en-US
release: zurich
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Classic UI, Use, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Manage controls

Learn how to rationalize, and consolidate controls to build an effective control framework when deploying your GRC application. Use entity-based access to manage control visibility, and ensure all controls are properly mapped to entities to maintain audit reliability.

## Rationalize your controls

Controls are specific implementations of control objectives. Before uploading or creating controls, take time to streamline and align them with business goals and risk mitigation strategies. If you upload all your controls in bulk, you're missing the opportunity to refine and streamline your controls set. As your business changes and your IT data, processes, and technology improve, replace outdated controls and procedures when you deploy your GRC application. Consider the following:

-   How does this control affect my business objective?
-   Is this control actually preventing or detecting risk?
-   Is there a different control that you can place that better protects your business?
-   Is there a control that you can put in place that reduces process overhead and improves IT performance while also mitigating risk?
-   Can a complicated control be replaced with a simpler more effective control?

**Note:** When you define controls manually or when you import them from the Unified Compliance Framework \(UCF\), an entity is associated with the controls. It is a mandatory field on the Control form. If, however, you import controls from a source other than the UCF, you may encounter controls that do not have associated entities. It is important that you return to the Control form and [add an entity to the control](../task/t_CreateAControl.md). Missing entities can cause unreliable results in calculations. Also, if you encounter a control with an entity that has been disabled, the control should be retired.

## Consolidate your controls

Look for opportunities to consolidate controls. For example, you can look for common, repeated controls across multiple regulatory authorities of frameworks \(such as SOX,GLBA, and AML\). Avoid operating a single control multiple times for each regulation by cross-mapping controls and eliminating the redundant ones. This process establishes a single consolidated control framework. Performing and preserving the cross mapping of controls is critical for audits.

The following diagram shows how industry regulations \(financial, insurance, energy and utilities, and healthcare and pharmaceuticals\) and requirements can overlap.

![Industry regulations and requirements overlap.](../../grc-common/image/industry-regulations.png "Industry regulations and requirements overlap")

## Define controls and business rules

The business rules that you define up front establish the GRC configuration settings later. Be prepared to do the following tasks:

-   Identify the controls and control owners
-   Define the control tests and expected results
-   Establish the test and control frequencies
-   Identify the risks: Impact and likelihood
-   Prepare the attestations, assessments, questionnaires, and required evidence
-   Compose the likely use cases \(who needs to interact with or view the contents of the GRC system and for what purposes\)
-   Map the authoritative sources to policies, procedures, controls, or risks

## Control requirements

When Create control requirements option is enabled for a control objective, for every control generated under an entity type, control requirements are also created automatically. Previously, only controls were created for entity types. The number of Control Requirements equals the number of control objective requirements.

## Attestation at control requirement level

The Attestation at control requirement level feature allows attestation at a granular level for individual control requirements within a control. Admins can enable requirement-level attestation, assign respondents, and generate assessment tasks for each control requirement. Respondents then attest to requirements by indicating whether they are implemented or not, providing evidence or explanations as required. Failed attestations automatically generate issues, mark the parent control as non-compliant, and roll up the status to the associated entity and control objective.

## Entity Based Access \(EBA\)

EBA provides a framework for a more granular approach to managing data access to objects that are associated with an entity. Administrators can grant access to an entity's related records by adding users or user groups or by using entity user fields for entity-based access configuration. For more information, see [Entity Based Access](../../grc-common/concept/entity-based-access.md).

When a user is qualified based on these configurations and has the minimum required roles, they will have access to the following tables:

-   Control
-   Attestation
-   Policy exception to control

## EBA rules

When entity based record access rules are enabled on the Entity Based Access Configuration Properties page, any new controls, control attestations, indicators, and indicator tasks associated with a configured entity automatically inherit the entity-based access \(EBA\) value from that entity. Previously, users had to run bulk access updates to apply EBA restrictions whenever new objects were created.

For more information, see [Entity based record access rules to secure new records](../../grc-common/concept/continuous-monitoring-of-entity-based-access.md).

