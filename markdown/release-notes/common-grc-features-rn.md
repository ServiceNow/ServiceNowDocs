---
title: Common Governance, Risk, and Compliance features release notes
description: Common Governance, Risk, and Compliance features provide shared capabilities for governance, access controls, workflows, regulatory resources, integrations, reporting, and user experiences across ServiceNow Governance, Risk, and Compliance applications. See the following sections for release notes by version.This release enhances issue management with configurable workflows, approval flows, and issue grouping. It also improves entity governance with entity change reviews and automatic entity owner and class updates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/common-grc-features-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Governance, Risk, and Compliance release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Common Governance, Risk, and Compliance features release notes

Common Governance, Risk, and Compliance features provide shared capabilities for governance, access controls, workflows, regulatory resources, integrations, reporting, and user experiences across ServiceNow Governance, Risk, and Compliance applications. See the following sections for release notes by version.

## About Common Governance, Risk, and Compliance features

-   Streamline Governance, Risk, and Compliance programs with shared capabilities used across ServiceNow GRC applications.
-   Control access to Governance, Risk, and Compliance data with shared security, domain separation, entity-based access, and user hierarchy capabilities.
-   Accelerate adoption with shared regulatory resources, content packs, recommendation frameworks, and use case accelerators.
-   Improve efficiency with common workflows, approvals, notifications, and workspace experiences.
-   Extend Governance, Risk, and Compliance processes with integrations, reporting, dashboards, and automation capabilities.

See [Common Governance, Risk, and Compliance features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/common-grc-features.md) for more information.

## Activation and other requirements

-   **Activation information**

    Common Governance, Risk, and Compliance features are available through supported Integrated Risk Management applications and licensing tiers. Activate the applicable Integrated Risk Management application and assign the required roles to access these shared Governance, Risk, and Compliance capabilities.


**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/grc-rn-landing.md)

## September 2026

This release enhances issue management with configurable workflows, approval flows, and issue grouping. It also improves entity governance with entity change reviews and automatic entity owner and class updates.

### What's new

-   **[Issue workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/issue-workflows.md)**

    With GRC Issue Management version 23.0.5, you can configure issue-specific workflows with custom lifecycle states, layouts, guided activities, trigger conditions, approval requirements, and routing rules. Use different workflows for different categories of issues without customizing the issue table.

-   **[Issue approval flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/issue-approval-flows.md)**

    With GRC Issue Management version 23.0.5, you can add an approval checkpoint before an issue or remediation task advances. This applies to state changes or due date extensions. Track approval requests, decisions, and approval history directly on the associated record.

-   **[Entity lifecycle management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/entity-change-management.md)**

    With GRC Profiles version 23.0.7, you can review the impact of proposed entity changes on associated risks and controls before applying the changes. Accept the changes or modify the entity filter to help prevent unintended changes.


### What's changed

-   **[Automatic entity owner and class updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/what-is-an-entity-filter.md)**

    With GRC Profiles version 23.0.7, the system automatically re-evaluates and updates entity owner and entity class when source record data or entity-filter membership changes. This change keeps entity ownership and classification aligned with the applicable entity-filter configuration.

-   **[Issue grouping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/issue-grouping-in-workspaces.md)**

    With GRC Issue Management version 23.0.5, you can add existing standalone issues directly from the Child Issues related list when grouping issues. You can group issues that use different workflows, and each child issue continues to follow its own workflow.


### What's deprecated or removed

-   **Now LLM Service**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


### Plugin information

-   **New plugins**

    GRC: Issue Management \(sn\_grc\_issue\_mgmt\): Activate the plugin to enable a redesigned issue management experience with configurable workflows, custom state models, issue approvals, and centralized administration


