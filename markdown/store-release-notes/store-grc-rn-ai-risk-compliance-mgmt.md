---
title: AI Risk and Compliance Management release notes
description: Version history for the AI Risk and Compliance Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-ai-risk-compliance-mgmt.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance version history release notes, ServiceNow Store version history release notes]
---

# AI Risk and Compliance Management release notes

Version history for the AI Risk and Compliance Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 23.0.3 - September 2026 \(Brazil\)**
    -   New:
        -   Enhanced AI Control Tower to automatically classify AI systems by risk at onboarding, helping identify managed and unmanaged assets and reducing manual review effort.
        -   Improved user experience and ability to save &amp; continue Evaluation configurations for continuous monitoring of AI assets.
        -   Enhanced AI Control Tower to support domain-separation readiness, enabling assessment and planning for client-level data segregation and multi-tenant deployments.
        -   Introduced new onboarding Playbook with dynamic &amp; risk-based execution &amp; lifecycle task management.
        -   Introduced new AI capabilities to recommend control objectives and risk statements on AI impact assessment task.
    -   Fixed:
        -   Fixed an issue where the Recommendation section was incorrectly displayed on the Risk and Compliance page.
        -   Fixed an issue where the Group Attestation action was not visible in the Attestation related list.
        -   Fixed upgrade-impact issues related to the introduction of a new field on the CCM Configuration record.
        -   Fixed an issue where the AI Asset Task state was not updated to Review after assessments were submitted.
-   **Version 22.5.4 - August 2026 \(Australia\)**
    -   New:
        -   Product Owner Persona \(Risk-based Tasks\)AI product owners can now access and act on risk and compliance lifecycle tasks, such as impact assessments and control attestations, from the Task Inbox and Activity Center in AI Control Tower. The Activity Center surfaces AI asset tasks, issues, policy exceptions, and AI cases for this persona. On the asset record page, the Risk and Compliance tab now shows only the Governance widget for product owners; risk assessments and regulatory risk assessments are hidden from the Assessments section, matching the scope of tasks this persona is responsible for.
        -   Continuous Controls Monitoring Continuous Controls Monitoring helps automate control verification and provide real-time visibility into control health, thereby reducing manual testing. Configure indicators that run on a schedule to evaluate whether a control is compliant or non-compliant. When an indicator fails, an issue is created so that the product owner of the affected asset can remediate it.
    -   Changed: As part of MRA Security Enhancements, Strengthened authorization validation within Multiple Record Association \(MRA\) workflows to improve security and ensure access checks are consistently enforced during record association operations
-   **Version 22.2.5 - August 2026 \(Zurich\)**
    -   New:
        -   Product Owner Persona \(Risk-based Tasks\)AI product owners can now access and act on risk and compliance lifecycle tasks, such as impact assessments and control attestations, from the Task Inbox and Activity Center in AI Control Tower. The Activity Center surfaces AI asset tasks, issues, policy exceptions, and AI cases for this persona. On the asset record page, the Risk and Compliance tab now shows only the Governance widget for product owners; risk assessments and regulatory risk assessments are hidden from the Assessments section, matching the scope of tasks this persona is responsible for.
        -   Continuous Controls Monitoring Continuous Controls Monitoring automates and accelerate control verification, reducing manual testing burden and providing real-time visibility into control health. Configure indicators that run on a schedule to evaluate whether a control is compliant or non-compliant. When an indicator fails, an issue is created so that the product owner of the affected asset can remediate it.
    -   Changed: As part of MRA Security Enhancements, Strengthened authorization validation within Multiple Record Association \(MRA\) workflows to improve security and ensure access checks are consistently enforced during record association operations
-   **Version 22.4.1 - July 2026 \(Australia\)**
    -   New
        -   Create and document governance, risk, and compliance issues with guided assistance from the employee center.
        -   Generate concise summaries of complex GRC issues for faster review and decision-making.
        -   Create executive summaries of risk assessments to communicate findings to stakeholders.
        -   Generate responses to assessment questions based on past assessments and reference documentation.
        -   Identify related control objectives from your controls library to reduce duplication.
-   **Version 22.3.5 - June 2026 \(Australia\)**
    -   New:
        -   Manage Smart Assessment  templates with versioning support. Create, publish, and delete template versions to support consistent assessment governance.
        -   View the entity, risk, and control for each assessment directly in task and work queue lists, without opening individual records.
        -   Access authority documents, agency mappings, and citations for additional AI regulatory frameworks in the AI Risk and Compliance content pack.
    -   Changed:
        -   Added automated impact assessment flow whenever an AI Dataset is created.
        -   Standardized query range security ACLs are now applied across all tables, ensuring consistent query access for authenticated users with appropriate read permissions throughout the platform. These ACL rules are installed automatically during upgrade with no administrator action required — automated upgrade scripts handle the full transition, including detection and processing of previously customized ACLs to ensure existing configurations continue to function without interruption. If your instance includes administrator-modified query range ACLs, a post-upgrade review is recommended to confirm alignment with your intended access policies.
    -   Fixed:
        -   Localization &amp; Performance issues are fixed.
        -   Fixed issue w.r.t to retired controls. Retired controls are excluded from the control based widgets.
        -   Fixed issue related to synchronization of AI asset life cycle tasks between AI Risk and Compliance and AICT workspace.
        -   Fixed functional domain issue w.r.t indicators feature on AI asset record page.
-   **Version 22.2.2 - May 2026 \(Australia\)**
    -   New: Added new API logic to support AICT AINPX product changes.
    -   Fixed: Fixed AI asset intake related changes.
-   **Version 22.1.2 - April 2026**
    -   New:
        -   Implemented Intake form enhancements to support only ServiceNow AI for non AICT product tier product offerings.
        -   Restricted the Intake form support for Enterprise AI for non AICT product tier product offerings.
-   **Version 22.0.3 - March 2026**
    -   New:
        -   New Automated risk classification feature for assets.
        -   Support for managed and unmanaged assets feature.
        -   Handled control objective workflow changes.
        -   Entity class restriction feature to support only AI asset types.
    -   Changed: Adopted smart assessment template category changes.
    -   Fixed: Fixed security and localisation issues.
-   **Version 21.1.1 - December 2025 \(Zurich\)**
    -   New:
        -   Entity-based access control
            -   Implemented the Entity-based Access Control feature, which facilitates object access through entities. You can map entities to specific users or user groups, enabling a granular level of access control.
            -   Administrators can grant access to an entity’s related records by adding users, user groups, entity user fields, or entity user group fields, minimizing the risk of unnecessary data exposure.
            -   You can now configure any user or user group field on a record to provide additional access beyond what is defined in the EBA configuration.
        -   Bulk Risk Assessment
            -   The Bulk Risk Assessment feature enables product owners to assess the regulatory and operational risks of multiple AI use cases in a unified workflow. Instead of reviewing and responding to risk questionnaires one by one, the system groups AI use cases with similar characteristics \(such as model type, data sensitivity, and business impact\) and presents a consolidated risk assessment form.
        -   Integration with unified content accelerator
            -   A new unified content interface shows the sequence of steps for importing related content and reviewing the selected content. This provides a step-by-step process for importing content into the product.
    -   Changed:
        -   Introduced an 'Active flag' in the GRC Choice table; updates to these flags are now reflected in the AI risk and compliance management application
        -   Implemented the impacts of Citation to control mapping feature across the dashabords and overview pages.
    -   Fixed:
        -   Resolved a security vulnerability that allowed unintended edits to read-only fields.
        -   Replaced hard-coded admin role dependencies with granular roles to improve security and align with least privilege principles.
-   **Version 21.0.1 - August 2025**
    -   New:
        -   Deliver system level AI risk score aggregation and visualization
            -   Provide aggregated AI system-level risk scoring by integrating heatmaps and residual risk score widgets directly within AI asset overview records. These visual tools help surface cumulative risk exposure and enable users to track residual risks effectively across the entire AI asset inventory. This capability supports proactive risk management by offering clear, data-driven insights into the overall AI system risk posture.
        -   Filter the risk heatmap by Risk Assessment Methodology for targeted risk analysis
            -   From the AI risk and compliance home page, apply the Risk Assessment Methodology ﬁlter to customize the display of the risk heatmap based on speciﬁc risk evaluation frameworks. This capability enables you to segment and analyze AI risks according to the assessment of models your organization adopts, such as internal standards, regulatory frameworks, or industry benchmarks. By narrowing the view to a particular methodology, you can better understand how different risk factors are identified, scored, and distributed, facilitating more informed decision-making. This targeted analysis supports the development of precise mitigation plans aligned with the organization's risk governance strategy.
        -   Grouping control attestations
            -   Control attestations can be grouped based on predeﬁned criteria such as control objectives, frameworks, or assessment cycles. This grouping functionality enables more efﬁcient management and review of attestations, reduces redundancy, and improves visibility into compliance status across related controls for AI Risk and Compliance team. It also supports better planning and execution of control assurance activities by organizing attestations in a logical, structured manner.
    -   Changed:
        -   The Risk and compliance tab features dedicated Risk overview and Compliance overview sections to support continuous monitoring of the risk and compliance posture of AI assets.
        -   The Risk overview section provides a ﬁltered view of AI assets based on inherent and residual risk levels, enabling informed risk evaluation. The Compliance overview section displays the regulatory risk classiﬁcation of AI systems, models, and datasets using donut charts.
-   **Version 20.2.0 - June 2025**

    Fixed: Added query-range ACLs for AI system and AI system tasks.

-   **Version 20.1.3 - May 2025**

    AI Risk and Compliance involves a strategic framework designed to identify, assess, and mitigate the inherent risks associated with the development and deployment of AI technologies. As organizations increasingly rely on AI systems, it becomes essential to navigate the complexities of compliance with global regulations such as the GDPR and the EU's AI Act. This framework includes a comprehensive risk assessment process to evaluate potential challenges such as, algorithmic bias, data privacy, and transparency. It ensures that AI systems are developed and used in an ethical and responsible manner. Engaging diverse stakeholders, including ethicists and legal experts, improves the organization's ability to address the social and ethical implications of AI technologies while fostering a culture of accountability.


