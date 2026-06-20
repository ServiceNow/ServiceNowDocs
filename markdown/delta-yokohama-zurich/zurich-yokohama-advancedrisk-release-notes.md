---
title: Combined Advanced Risk release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Advanced Risk from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-advancedrisk-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 9
breadcrumb: [Products combined by family]
---

# Combined Advanced Risk release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Advanced Risk from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Advanced Risk release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Advanced Risk to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Advanced Risk.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Generative AI risk assessment summarization](https://servicenow-staging.fluidtopics.net/access?context=generate-risk-assessment-summary-genai&family=yokohama&ft:locale=en-US)**

Generate a risk assessment summary from your inherent, residual, target risks, and control effectiveness data using the Now Assist for IRM application. The summary highlights key insights to help your approvers quickly understand the context before approving the risk assessments. You can also analyze details such as open issues, risk response tasks, action items, and calculated risk scores to support your approval decision. Check your entitlements to confirm whether you have access to risk assessment summarization.

-   **[Reassess a risk assessment project](https://servicenow-staging.fluidtopics.net/access?context=reassess-risk-assessment-project&family=yokohama&ft:locale=en-US)**

Review completed risk assessment projects to reflect new insights or changing conditions. All previously assessed risks in this project are automatically carried over and reassigned to the designated assessor. Confirm continuity, minimize manual effort, and enhance efficiency in your risk management process.

-   **[Copy risk responses from the previous assessment](https://servicenow-staging.fluidtopics.net/access?context=perform-assessment-on-risk-assessment-project&family=yokohama&ft:locale=en-US)**

Copy responses from a previous risk assessment during the reassessment of a risk assessment project to streamline the assessment process. All prior responses are automatically copied, saving time and maintaining consistency.

-   **[Remove risks from assessment](https://servicenow-staging.fluidtopics.net/access?context=perform-assessment-on-risk-assessment-project&family=yokohama&ft:locale=en-US)**

As a risk assessor, you can remove risks from the risk assessment project while performing the assessment, which also removes all responses associated with that risk. Removed scoped risks remain part of the project but are marked as not applicable for reporting purposes. However, removed ad hoc risks are completely deleted.

-   **[Manage risk response task workflow](https://servicenow-staging.fluidtopics.net/access?context=configure-ram&family=yokohama&ft:locale=en-US)**

Manage and enable the risk response task workflow from the RAM form to enable users to create, delete, remove, edit, and link risk response tasks within an assessment.

-   **[Reassign assessor for a risk assessment project](https://servicenow-staging.fluidtopics.net/access?context=reassign-assessor-for-risk-assessment-project&family=yokohama&ft:locale=en-US)**

Reassign assessors for multiple in-progress risk assessment projects simultaneously to minimize disruptions during stakeholder transitions.

-   **[Configure risk color styles for the Next Experience](https://servicenow-staging.fluidtopics.net/access?context=create-risk-color-style&family=yokohama&ft:locale=en-US)**

Define and preview colors for the risk and advanced risk components in the Next Experience through a configurable system rather than having to use hex codes. The transition has been made from a hex code color management system to a configurable system that supports the highlighted value component colors. This feature addresses theming and accessibility issues. You can define the color and variant, and preview them using the Next Experience color styles tab on the Risk color style form.

**Note:** The default color for the customized risk color style is set to Critical, with the variant set to Primary. You can manually change the color and variant based on the requirement.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Identify risks for an entity](https://servicenow-staging.fluidtopics.net/access?context=suggest-potential-risks-workflow&family=zurich&ft:locale=en-US)**

If you’re a Workspace user with the sn\_grc\_sharegenai.risk\_suggestion\_aiagent\_user role, you can use the Risk Suggestion AI Agent to identify risks related to an entity. The AI agent analyzes the entity and suggests relevant risks from various sources, consolidating them into a reviewable list to verify for accuracy. Risk managers can then confirm and promote these risks to the risk register for further assessment. This feature automates risk discovery, helping identify potential risks and prepare for compliance requirements.

-   **[Reporting views from Risk Assessment Methodology](https://servicenow-staging.fluidtopics.net/access?context=reporting-views-from-ram&family=zurich&ft:locale=en-US)**

The reporting view provides an overview of all assessments under a specific Risk Assessment Methodology \(RAM\). It consolidates assessment data such as factor responses, scores, issues, controls, and associated risks into a single structure. When a RAM is published, the system automatically creates this view, which you can use to review assessments and build custom reports. It simplifies report and dashboard creation for risk assessments.

**Note:** Automatic creation of Reporting views is not supported on Xanadu. For instructions on creating them manually, refer to [KB2547071](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2547071)

-   **[Risk event summarization](https://servicenow-staging.fluidtopics.net/access?context=generate-risk-event-summary-in-the-risk-workspace&family=zurich&ft:locale=en-US)**

Generate risk event summary using the Now Assist for IRM application. Risk event summarisation is a Generative AI driven capability that generates clear and consistent summaries automatically. It reduces the need for manual effort, helps risk managers save time, and enables approvers to quickly understand the key details for faster decisions. Check your entitlements to confirm whether you have access to risk event summarization.

-   **[Grid based risk and control assessment](https://servicenow-staging.fluidtopics.net/access?context=perform-assessment-risk-assessment-project-grid-view&family=zurich&ft:locale=en-US)**

Gain efficient control over risk assessments with the new grid-based Risk and Control Self Assessment \(RCSA\). Quickly compare, edit, and prioritize risks and controls using the flexible, spreadsheet-style interface. Use side-by-side views and bulk editing to complete assessments faster.

-   **[Matrix report in Risk Workspace](https://servicenow-staging.fluidtopics.net/access?context=matrix-report-in-risk-workspace&family=zurich&ft:locale=en-US)**

Access and analyze the risk posture of your organization using entity-related data, such as risks, controls, KRIs, and events in a centralized, configurable grid-based view. This feature reduces time spent switching views and helps risk managers assess data more easily, leading to more proactive and streamlined risk management.

-   **[Support third party large language models](https://servicenow-staging.fluidtopics.net/access?context=generate-risk-assessment-summary-genai&family=zurich&ft:locale=en-US)**

Risk assessment summarization and Risk event summarization support the LLMs from the third party providers, such as Anthropic Claude, Google Gemini, and OpenAI, in addition to Now LLM. This enhancement gives you greater flexibility to choose the model that best fits your organization’s needs for generating risk assessment and risk event summaries.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Advanced Risk features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   ****
-   **[Changes to Now Assist usage measurement](https://servicenow-staging.fluidtopics.net/access?context=monitoring-now-assist-usage&family=yokohama&ft:locale=en-US)**




</td></tr><tr><td>

Zurich

</td><td>

-   ****

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Advanced Risk features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Advanced Risk features or functionality were deprecated.

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

Install Advanced Risk by requesting it from the ServiceNow Store. 

</td></tr><tr><td>

Zurich

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

-   **Reflow for Risk heatmap**

The Risk Heatmap component was updated to support reﬂow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations.


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

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://servicenow-staging.fluidtopics.net/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.

-   Use generative AI to generate risk assessment summaries and highlight key insights for better context.
-   Reassess completed risk assessment projects to evaluate risks based on new insights or changing conditions.
-   Copy risk responses from a previous risk assessment during reassessment of a risk assessment project.
-   Reassign assessors for multiple risk assessment projects to optimize resource allocation.
-   Remove risks from a risk assessment project during the assessment to streamline focus on relevant risks.
-   Enable and manage the risk response task workflow from the Risk Assessment Methodology \(RAM\) form.

 See [Advanced Risk Assessment](https://servicenow-staging.fluidtopics.net/access?context=advanced-risk-assessment&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://servicenow-staging.fluidtopics.net/access?context=now-assist-skills-on-by-default&family=zurich&ft:locale=en-US)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.

-   Use the Risk Suggestion AI Agent to discover potential risks for an entity, giving risk managers better insights for informed decision-making.
-   Use the risk reporting view to view all assessments under a specific Risk Assessment Methodology \(RAM\), including factor responses, scores, issues, and risks.
-   Use generative AI to generate risk event summary to quickly understand the risk event key details for faster decisions.
-   Assess multiple risks and controls side-by-side, make bulk edits, and prioritize entries efficiently using the spreadsheet-style layout.
-   Use matrix report in the Risk Workspace to assess and analyze the risk posture of your organization.
-   Use large language models \(LLMs\) from the third party providers to generate the risk assessment summary.

 See [Advanced Risk Assessment](https://servicenow-staging.fluidtopics.net/access?context=advanced-risk-assessment&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

