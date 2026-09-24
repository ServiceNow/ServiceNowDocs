---
title: Combined Advanced Risk release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Advanced Risk from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-advancedrisk-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Advanced Risk release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Advanced Risk from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Advanced Risk release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Advanced Risk to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Advanced Risk.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Worst case aggregation rollup for risk scoring](https://www.servicenow.com/docs/access?context=risk-assessment-methodology-form&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.2, use the worst case aggregation rollup method that derives all scores from a single risk record based on the highest residual risk. You can configure this option on the Risk Assessment Methodology \(RAM\) form. By using a single risk record as the source, this method keeps all rolled-up scores aligned to a real risk scenario, supporting traceability, audit requirements, and enterprise governance.

-   **[Hide Not applicable option in control and residual assessments](https://www.servicenow.com/docs/access?context=control-assessment-form&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.2, configure the Risk Assessment Methodology \(RAM\) to hide the Not applicable check box in control effectiveness and residual assessment sections by using the **Hide assessment not applicable** option. This change reduces calculation errors and improves the reliability of assessment results.

-   **[Parallel review and feedback for Risk assessment project](https://www.servicenow.com/docs/access?context=integrate-advanced-risk-with-parallel-review-feedback&family=australia&ft:locale=en-US)**

Parallel review and feedback is now enabled by default on the risk assessment project record page and the project assessment page, in both stacked view and grid view. You can use collaborative review workflows without manual configuration, which removes the setup overhead previously required by the custom page structure of risk assessment projects.

-   **Redirect GRC notification links to the appropriate workspace**

After upgrading to version 22.3.2, redirect to the appropriate workspace when accessing GRC records from email notifications, based on the access and role. This feature improves usability, reduces confusion, and supports adoption of workspace-based workflows.

-   **[Template versioning for Risk Identification](https://www.servicenow.com/docs/access?context=template-versioning&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.2, Risk Identification supports smart assessment template versioning. New versions can be created from existing templates without creating a new template, and assessments use the latest published version.

-   **[Audit entry field on Risk Assessment Project](https://www.servicenow.com/docs/access?context=create-risk-assessment-project&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.2, Risk Assessment Projects support audit entries to track changes and activity history. An audit entry framework separates audit-specific \(third-line\) records from operational \(second-line\) records and controls visibility.

**Note:** This option is available if Audit Management and Audit Workspace are installed. Assign the sn\_audit\_ws.third\_line\_manager role to a user to use this feature.


 -   **[Risk Suggestion AI Agent enhancements](https://www.servicenow.com/docs/access?context=identify-risks-for-entity&family=australia&ft:locale=en-US)**

After upgrading the ServiceNow Otto for Integrated Risk Management \(IRM\) application to version 22.x, the Risk Suggestion AI Agent supports a more context‑aware and conversational workflow. After selecting risk types, you can provide additional context to refine search results, with the agent dynamically asking follow‑up questions when needed. Before adding risks to the suggested risk section, you can review and modify suggested risks by updating descriptions, renaming risks, or removing items from the list.


 -   **[Risk event response template enhancements](https://www.servicenow.com/docs/access?context=create-risk-event-response-template&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.x, users with the Risk Manager \[sn\_risk.manager\] or Risk Admin \[sn\_risk.admin\] role can configure risk event response templates using dynamic, entity‑driven assignments. These changes enable assignments to be derived from entity data alongside existing static user or group selection.

You can select user fields defined on the entity \(such as Owner or Sub-owner\) or entity stakeholder personas when configuring:

    -   Risk event owner assignment
    -   Issue creation and assignment
    -   Risk event approvers
-   **[Control Objective workflow](https://www.servicenow.com/docs/access?context=create-control-objective-ws&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.x, you can use a defined workflow to update control objectives. Changes can be drafted and reviewed without changing the current active version, which helps avoid unintended changes to related controls, and risk records. Only approved updates become active. The workflow also sets clear responsibility for making updates and helps keep control objective information consistent and up to date.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Advanced Risk features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Risk event enhancements](https://www.servicenow.com/docs/access?context=manage-risk-events&family=australia&ft:locale=en-US)**

Risk event administrators can manage the entire risk event workflow. This update grants permissions aligned with the Risk Manager role, including the ability to reopen closed risk events.

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Advanced Risk features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Advanced Risk features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Advanced Risk.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**

Install Advanced Risk by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Important:** Advanced Risk is available in the ServiceNow Store. For details, see the Activation information section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Advanced Risk we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Advanced Risk we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Advanced Risk, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Advanced Risk we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Advanced Risk we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   Introduces a rollup method that derives all risk scores from a single risk record based on the highest residual risk, improving traceability and alignment.
-   Eliminate inconsistent risk assessment inputs by allowing administrators to hide the Not applicable option in control and residual assessments, improving calculation accuracy and reliability.
-   Assign risk event owners, issue owners, and risk event approvers based on entity fields, in addition to static user or group selection.
-   Use the Risk Suggestion AI Agent to refine and confirm risks, by providing additional context and reviewing, updating, renaming, or removing suggested risks before they’re added.
-   Use a structured workflow to draft, review, and approve control objective updates before making them active.

 [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

 Review the updated AI experience with three licensing tiers.

 See [Advanced Risk Assessment](https://www.servicenow.com/docs/access?context=advanced-risk-assessment&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

