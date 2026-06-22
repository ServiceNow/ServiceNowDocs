---
title: Combined Advanced Risk release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Advanced Risk from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-advancedrisk-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined Advanced Risk release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Advanced Risk from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Advanced Risk release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Advanced Risk to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Advanced Risk.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Identify risks for an entity](https://www.servicenow.com/docs/access?context=suggest-potential-risks-workflow&family=zurich&ft:locale=en-US)**

If you’re a Workspace user with the sn\_grc\_sharegenai.risk\_suggestion\_aiagent\_user role, you can use the Risk Suggestion AI Agent to identify risks related to an entity. The AI agent analyzes the entity and suggests relevant risks from various sources, consolidating them into a reviewable list to verify for accuracy. Risk managers can then confirm and promote these risks to the risk register for further assessment. This feature automates risk discovery, helping identify potential risks and prepare for compliance requirements.

-   **[Reporting views from Risk Assessment Methodology](https://www.servicenow.com/docs/access?context=reporting-views-from-ram&family=zurich&ft:locale=en-US)**

The reporting view provides an overview of all assessments under a specific Risk Assessment Methodology \(RAM\). It consolidates assessment data such as factor responses, scores, issues, controls, and associated risks into a single structure. When a RAM is published, the system automatically creates this view, which you can use to review assessments and build custom reports. It simplifies report and dashboard creation for risk assessments.

**Note:** Automatic creation of Reporting views is not supported on Xanadu. For instructions on creating them manually, refer to [KB2547071](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2547071)

-   **[Risk event summarization](https://www.servicenow.com/docs/access?context=generate-risk-event-summary-in-the-risk-workspace&family=zurich&ft:locale=en-US)**

Generate risk event summary using the Now Assist for IRM application. Risk event summarisation is a Generative AI driven capability that generates clear and consistent summaries automatically. It reduces the need for manual effort, helps risk managers save time, and enables approvers to quickly understand the key details for faster decisions. Check your entitlements to confirm whether you have access to risk event summarization.

-   **[Grid based risk and control assessment](https://www.servicenow.com/docs/access?context=perform-assessment-risk-assessment-project-grid-view&family=zurich&ft:locale=en-US)**

Gain efficient control over risk assessments with the new grid-based Risk and Control Self Assessment \(RCSA\). Quickly compare, edit, and prioritize risks and controls using the flexible, spreadsheet-style interface. Use side-by-side views and bulk editing to complete assessments faster.

-   **[Matrix report in Risk Workspace](https://www.servicenow.com/docs/access?context=matrix-report-in-risk-workspace&family=zurich&ft:locale=en-US)**

Access and analyze the risk posture of your organization using entity-related data, such as risks, controls, KRIs, and events in a centralized, configurable grid-based view. This feature reduces time spent switching views and helps risk managers assess data more easily, leading to more proactive and streamlined risk management.

-   **[Support third party large language models](https://www.servicenow.com/docs/access?context=generate-risk-assessment-summary-genai&family=zurich&ft:locale=en-US)**

Risk assessment summarization and Risk event summarization support the LLMs from the third party providers, such as Anthropic Claude, Google Gemini, and OpenAI, in addition to Now LLM. This enhancement gives you greater flexibility to choose the model that best fits your organization’s needs for generating risk assessment and risk event summaries.


</td></tr><tr><td>

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

-   **[Risk event response template enhancements](https://www.servicenow.com/docs/access?context=create-risk-event-response-template&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.x, users with the Risk Manager \[sn\_risk.manager\] or Risk Admin \[sn\_risk.admin\] role can configure risk event response templates using dynamic, entity‑driven assignments. These changes enable assignments to be derived from entity data alongside existing static user or group selection.

You can select user fields defined on the entity \(such as Owner or Sub-owner\) or entity stakeholder personas when configuring:

    -   Risk event owner assignment
    -   Issue creation and assignment
    -   Risk event approvers
-   **[Risk Suggestion AI Agent enhancements](https://www.servicenow.com/docs/access?context=identify-risks-for-entity&family=australia&ft:locale=en-US)**

After upgrading the Now Assist for Integrated Risk Management \(IRM\) application to version 22.x, the Risk Suggestion AI Agent supports a more context‑aware and conversational workflow. After selecting risk types, you can provide additional context to refine search results, with the agent dynamically asking follow‑up questions when needed. Before adding risks to the suggested risk section, you can review and modify suggested risks by updating descriptions, renaming risks, or removing items from the list.

-   **[Control Objective workflow](https://www.servicenow.com/docs/access?context=create-control-objective-ws&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.x, you can use a defined workflow to update control objectives. Changes can be drafted and reviewed without changing the current active version, which helps avoid unintended changes to related controls, and risk records. Only approved updates become active. The workflow also sets clear responsibility for making updates and helps keep control objective information consistent and up to date.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Advanced Risk features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   ****

</td></tr><tr><td>

Australia

</td><td>

-   **[Risk event enhancements](https://www.servicenow.com/docs/access?context=manage-risk-events&family=australia&ft:locale=en-US)**

Risk event administrators can manage the entire risk event workflow. This update grants permissions aligned with the Risk Manager role, including the ability to reopen closed risk events.

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Advanced Risk features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

To enhance the Risk Workspace home page load performance and reduce latency, the **Tasks** widget has been removed from the home page.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Advanced Risk features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

Install Advanced Risk by requesting it from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

Install Advanced Risk by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Advanced Risk we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

-   **Reflow for Risk heatmap**

The Risk Heatmap component was updated to support reﬂow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations.


</td></tr><tr><td>

Australia

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=zurich&ft:locale=en-US)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.

-   Use the Risk Suggestion AI Agent to discover potential risks for an entity, giving risk managers better insights for informed decision-making.
-   Use the risk reporting view to view all assessments under a specific Risk Assessment Methodology \(RAM\), including factor responses, scores, issues, and risks.
-   Use generative AI to generate risk event summary to quickly understand the risk event key details for faster decisions.
-   Assess multiple risks and controls side-by-side, make bulk edits, and prioritize entries efficiently using the spreadsheet-style layout.
-   Use matrix report in the Risk Workspace to assess and analyze the risk posture of your organization.
-   Use large language models \(LLMs\) from the third party providers to generate the risk assessment summary.

 See [Advanced Risk Assessment](https://www.servicenow.com/docs/access?context=advanced-risk-assessment&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

