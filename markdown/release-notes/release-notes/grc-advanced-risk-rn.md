---
title: Advanced Risk release notes
description: The ServiceNow Advanced Risk application enables you to identify, analyze, evaluate, treat, and monitor risks that could impact your organization in achieving its business objectives. Advanced Risk was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
---

# Advanced Risk release notes

The ServiceNow® Advanced Risk application enables you to identify, analyze, evaluate, treat, and monitor risks that could impact your organization in achieving its business objectives. Advanced Risk was enhanced and updated in the Australia release.

## Advanced Risk highlights for the Australia release

-   Introduces a rollup method that derives all risk scores from a single risk record based on the highest residual risk, improving traceability and alignment.
-   Eliminate inconsistent risk assessment inputs by allowing administrators to hide the Not applicable option in control and residual assessments, improving calculation accuracy and reliability.
-   Assign risk event owners, issue owners, and risk event approvers based on entity fields, in addition to static user or group selection.
-   Use the Risk Suggestion AI Agent to refine and confirm risks, by providing additional context and reviewing, updating, renaming, or removing suggested risks before they’re added.
-   Use a structured workflow to draft, review, and approve control objective updates before making them active.

[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)

Review the updated AI experience with three licensing tiers.

See [Advanced Risk Assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/advanced-risk-assessment.md) for more information.

**Important:** Advanced Risk is available in the ServiceNow Store. For details, see the Activation information section of these release notes.

## New in the Australia release

-   **[Worst case aggregation rollup for risk scoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/risk-assessment-methodology-form.md)**

    After upgrading to version 22.3.2, use the worst case aggregation rollup method that derives all scores from a single risk record based on the highest residual risk. You can configure this option on the Risk Assessment Methodology \(RAM\) form. By using a single risk record as the source, this method keeps all rolled-up scores aligned to a real risk scenario, supporting traceability, audit requirements, and enterprise governance.

-   **[Hide Not applicable option in control and residual assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/control-assessment-form.md)**

    After upgrading to version 22.3.2, configure the Risk Assessment Methodology \(RAM\) to hide the Not applicable check box in control effectiveness and residual assessment sections by using the **Hide assessment not applicable** option. This change reduces calculation errors and improves the reliability of assessment results.

-   **[Parallel review and feedback for Risk assessment project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/integrate-advanced-risk-with-parallel-review-feedback.md)**

    Parallel review and feedback is now enabled by default on the risk assessment project record page and the project assessment page, in both stacked view and grid view. You can use collaborative review workflows without manual configuration, which removes the setup overhead previously required by the custom page structure of risk assessment projects.

-   **Redirect GRC notification links to the appropriate workspace**

    After upgrading to version 22.3.2, redirect to the appropriate workspace when accessing GRC records from email notifications, based on the access and role. This feature improves usability, reduces confusion, and supports adoption of workspace-based workflows.

-   **[Template versioning for Risk Identification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/template-versioning.md)**

    After upgrading to version 22.3.2, Risk Identification supports smart assessment template versioning. New versions can be created from existing templates without creating a new template, and assessments use the latest published version.

-   **[Audit entry field on Risk Assessment Project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-risk-assessment-project.md)**

    After upgrading to version 22.3.2, Risk Assessment Projects support audit entries to track changes and activity history. An audit entry framework separates audit-specific \(third-line\) records from operational \(second-line\) records and controls visibility.

    **Note:** This option is available if Audit Management and Audit Workspace are installed. Assign the sn\_audit\_ws.third\_line\_manager role to a user to use this feature.

-   **[Risk event response template enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-risk-event-response-template.md)**

    After upgrading to version 22.0.x, users with the Risk Manager \[sn\_risk.manager\] or Risk Admin \[sn\_risk.admin\] role can configure risk event response templates using dynamic, entity‑driven assignments. These changes enable assignments to be derived from entity data alongside existing static user or group selection.

    You can select user fields defined on the entity \(such as Owner or Sub-owner\) or entity stakeholder personas when configuring:

    -   Risk event owner assignment
    -   Issue creation and assignment
    -   Risk event approvers
-   **[Risk Suggestion AI Agent enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/identify-risks-for-entity.md)**

    After upgrading the Now Assist for Integrated Risk Management \(IRM\) application to version 22.x, the Risk Suggestion AI Agent supports a more context‑aware and conversational workflow. After selecting risk types, you can provide additional context to refine search results, with the agent dynamically asking follow‑up questions when needed. Before adding risks to the suggested risk section, you can review and modify suggested risks by updating descriptions, renaming risks, or removing items from the list.

-   **[Control Objective workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-control-objective-ws.md)**

    After upgrading to version 22.0.x, you can use a defined workflow to update control objectives. Changes can be drafted and reviewed without changing the current active version, which helps avoid unintended changes to related controls, and risk records. Only approved updates become active. The workflow also sets clear responsibility for making updates and helps keep control objective information consistent and up to date.


## Changed in this release

-   **[Risk event enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/manage-risk-events.md)**

    Risk event administrators can manage the entire risk event workflow. This update grants permissions aligned with the Risk Manager role, including the ability to reopen closed risk events.

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
    Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


## Activation information

Install Advanced Risk by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[GRC Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-risk-overview.md)**

    Use the Risk Management application with the ServiceNow® Advanced Risk application to identify and monitor high-impact risks, improve your risk-based decision-making, and reduce reaction time.

-   **[GRC Risk Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/risk-workspace.md)**

    Using Risk Workspace with the ServiceNow® Advanced Risk application provides a simplified user experience with a single-pane view for all your risk-related activities.


**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/grc-rn-landing.md)

