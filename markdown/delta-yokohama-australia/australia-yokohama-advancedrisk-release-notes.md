---
title: Combined Advanced Risk release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Advanced Risk from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-advancedrisk-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 9
breadcrumb: [Products combined by family]
---

# Combined Advanced Risk release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Advanced Risk from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Advanced Risk release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Advanced Risk to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Yokohama

</td><td>

-   **[Generative AI risk assessment summarization](https://www.servicenow.com/docs/access?context=generate-risk-assessment-summary-genai&family=yokohama&ft:locale=en-US)**

Generate a risk assessment summary from your inherent, residual, target risks, and control effectiveness data using the ServiceNow Otto for IRM application. The summary highlights key insights to help your approvers quickly understand the context before approving the risk assessments. You can also analyze details such as open issues, risk response tasks, action items, and calculated risk scores to support your approval decision. Check your entitlements to confirm whether you have access to risk assessment summarization.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Grid based risk and control assessment](https://www.servicenow.com/docs/access?context=perform-assessment-risk-assessment-project-grid-view&family=zurich&ft:locale=en-US)**

Gain efficient control over risk assessments with the new grid-based Risk and Control Self Assessment \(RCSA\). Quickly compare, edit, and prioritize risks and controls using the flexible, spreadsheet-style interface. Use side-by-side views and bulk editing to complete assessments faster.

-   **[Matrix report in Risk Workspace](https://www.servicenow.com/docs/access?context=matrix-report-in-risk-workspace&family=zurich&ft:locale=en-US)**

Access and analyze the risk posture of your organization using entity-related data, such as risks, controls, KRIs, and events in a centralized, configurable grid-based view. This feature reduces time spent switching views and helps risk managers assess data more easily, leading to more proactive and streamlined risk management.

-   **[Support third party large language models](https://www.servicenow.com/docs/access?context=generate-risk-assessment-summary-genai&family=zurich&ft:locale=en-US)**

Risk assessment summarization and Risk event summarization support the LLMs from the third party providers, such as Anthropic Claude, Google Gemini, and OpenAI, in addition to Now LLM. This enhancement gives you greater flexibility to choose the model that best fits your organization’s needs for generating risk assessment and risk event summaries.


</td></tr><tr><td>

Australia

</td><td>

-   **[Risk Suggestion AI Agent enhancements](https://www.servicenow.com/docs/access?context=identify-risks-for-entity&family=australia&ft:locale=en-US)**

After upgrading the ServiceNow Otto for Integrated Risk Management \(IRM\) application to version 22.x, the Risk Suggestion AI Agent supports a more context‑aware and conversational workflow. After selecting risk types, you can provide additional context to refine search results, with the agent dynamically asking follow‑up questions when needed. Before adding risks to the suggested risk section, you can review and modify suggested risks by updating descriptions, renaming risks, or removing items from the list.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Advanced Risk features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=yokohama&ft:locale=en-US)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Zurich

</td><td>

-   **[Some generative AI skills, AI agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=zurich&ft:locale=en-US)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.

</td></tr><tr><td>

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


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Advanced Risk features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

To enhance the Risk Workspace home page load performance and reduce latency, the **Tasks** widget has been removed from the home page.

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

Yokohama

</td><td>

-   **Activation information**

Install Advanced Risk by requesting it from the ServiceNow Store. 


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Install Advanced Risk by requesting it from the ServiceNow Store. 


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install Advanced Risk by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Advanced Risk we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Accessibility information**
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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Yokohama

</td><td>

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.

-   Use generative AI to generate risk assessment summaries and highlight key insights for better context.
-   Reassess completed risk assessment projects to evaluate risks based on new insights or changing conditions.
-   Copy risk responses from a previous risk assessment during reassessment of a risk assessment project.
-   Reassign assessors for multiple risk assessment projects to optimize resource allocation.
-   Remove risks from a risk assessment project during the assessment to streamline focus on relevant risks.
-   Enable and manage the risk response task workflow from the Risk Assessment Methodology \(RAM\) form.

 See [Advanced Risk Assessment](https://www.servicenow.com/docs/access?context=advanced-risk-assessment&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Some generative AI skills, AI agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=zurich&ft:locale=en-US)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

