---
title: AI Risk and Compliance Management release notes
description: Version history for the AI Risk and Compliance Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-ai-risk-compliance-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# AI Risk and Compliance Management release notes

Version history for the AI Risk and Compliance Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

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


