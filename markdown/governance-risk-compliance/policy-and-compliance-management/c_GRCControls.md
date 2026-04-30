---
title: Manage controls
description: Controls are specific implementations of a control objective. Retired controls do not appear in the list. Before defining controls, take time to rationalize, consolidate, and define the important controls in your organization.
locale: en-US
release: xanadu
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using the Classic user interface for Policy and Compliance tasks, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Manage controls

Controls are specific implementations of a control objective. Retired controls do not appear in the list. Before defining controls, take time to rationalize, consolidate, and define the important controls in your organization.

## Rationalize your controls

If you upload all your controls in bulk, you are missing the opportunity to refine and streamline your controls set. As your business changes, and your IT data, processes, and technology improve, replace outdated controls and procedures when you implement your GRC application. Consider the following:

-   How does this control affect my business objective?
-   Is this control actually preventing or detecting risk?
-   Is there a different control you can place that better protects your business?
-   Is there a control you can put in place that reduces process overhead and improves IT performance while also mitigating risk?
-   Can a complicated control be replaced with a simpler more effective control?

**Note:** When you define controls manually or when you import them from the Unified Compliance Framework \(UCF\), an entity is associated with the controls. It is a mandatory field on the Control form. If, however, you import controls from a source other than the UCF, you may encounter controls that do not have associated entities. It is important that you return to the Control form and [add an entity to the control](../task/t_CreateAControl.md). Missing entities can cause unreliable results in calculations. Also, if you encounter a control with an entity that has been disabled, the control should be retired.

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

