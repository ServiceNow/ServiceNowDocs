---
title: Combined Advanced Risk release notes for upgrades from Xanadu to Zurich
description: Consolidated page of all release notes for Advanced Risk from Xanadu to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-xanadu-zurich/zurich-xanadu-advancedrisk-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 15
breadcrumb: [Products combined by family]
---

# Combined Advanced Risk release notes for upgrades from Xanadu to Zurich

Consolidated page of all release notes for Advanced Risk from Xanadu to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Advanced Risk release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Advanced Risk to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

-   **[Create multidimensional entities](https://servicenow-staging.fluidtopics.net/access?context=create-composite-entity-ws&family=xanadu&ft:locale=en-US)**

Create multidimensional entities by combining two or more entities from different entity classes using the Composite Entity Management application. You can create multidimensional entity classes with a composite entity structure, such as Company \| Department \| Business Process. After defining the composite entity class, you can create composite entity that operates as a standalone entity. This feature enables you to manage risk and compliance workflows at the composite entity level, providing visibility into the combined risk and compliance posture.

**Note:** Composite entity classes can be created in both the classic UI and the Risk Workspace. The creation of composite entities is supported only in Risk Workspace.

-   **[Assess multiple risks and controls simultaneously](https://servicenow-staging.fluidtopics.net/access?context=risk-assessment-project&family=xanadu&ft:locale=en-US)**

Create a risk assessment project to perform bulk assessments on multiple risks and controls, enabling assessors to evaluate them in a single project. This approach reduces time and effort, confirms consistency across multiple assessments, and provides a more comprehensive view of risks and controls within the same project. You can scope multiple risks related to the assessable entity within the project and perform assessments.

**Note:** Assessment of multiple risks and controls is supported only in Risk Workspace.

-   **[Addition of new roles](https://servicenow-staging.fluidtopics.net/access?context=risk-assessment-project&family=xanadu&ft:locale=en-US)**

The following roles related to risk assessment project were added:

    -   Risk assessment project reader \[sn\_risk\_advanced.risk\_asmt\_project\_reader\]: Provides read only access to the risk assessment projects.
    -   Risk assessment project user \[sn\_risk\_advanced.risk\_asmt\_project\_user\]: Provides the ability to create risk assessment projects and update or delete only the projects created by the user.
    -   Risk assessment project manager \[sn\_risk\_advanced.risk\_asmt\_project\_manager\]: Provides the ability to create, update, and delete any risk assessment projects.
-   **[Enhanced risk response workflow](https://servicenow-staging.fluidtopics.net/access?context=workflow-of-risk-response-task&family=xanadu&ft:locale=en-US)**

Streamline your risk response workflow with the following enhancements:

    -   Use a uniform workflow for all types of risk response tasks. A standardized workflow for risk response tasks enhances the management of all types of risk response tasks, promotes consistency, and reduces the need for customization.
    -   Configure multiple levels of approvals for the risk response tasks using the approval configurator. By default, a single level of approval is enabled for all types of risk response tasks, where the risk owner can approve the tasks. These approvals can be configured based on requirements.
    -   Reject a risk response task and move it to the work in progress state without closing it. This feature helps the risk response task owner to modify the response strategy if the approver is unsatisfied with the response.
    -   Create action items with an independent workflow and link them to the risk response tasks when they are in the Draft or Work in progress state.

**Note:** You can create risk response action items for all types of risk responses except for Risk acceptance tasks.

    -   Copy risk response plans from the previous risk assessment to the current risk assessment while reassessing.
    -   Link an open risk response task from the previous assessment to the current risk assessment while reassessing. You can also edit or remove an existing risk response task.
-   **[Issue linking with risk assessments](https://servicenow-staging.fluidtopics.net/access?context=perform-ara-workspace&family=xanadu&ft:locale=en-US)**

Streamline your risk assessments with the following enhancements:

    -   Enable the issue linking option on the Risk Assessment Methodology \(RAM\) form to create an issue or link an existing open issue with the risk assessment.
    -   View issue details from the configurable issue card available on the risk assessment.
    -   Identify newly created issues from existing linked issues with a visual differentiator on the issue card.
    -   Edit or remove issues.
-   **[Enhanced risk event task workflow](https://servicenow-staging.fluidtopics.net/access?context=manage-risk-events&family=xanadu&ft:locale=en-US)**

Streamline your risk event workflow with the following enhancements:

    -   Use a uniform and enhanced workflow for the risk event tasks. A standardized workflow enhances the management of risk event tasks.
    -   Configure multiple levels of approvals for the risk event tasks using the approval configurator.
    -   Reject a risk event task and move it to the work in progress state without closing it. This feature helps the risk event task owner to modify the risk event if the approver is unsatisfied.
-   **[Improved user experience for risk identification questionnaire using Smart Assessment Engine](https://servicenow-staging.fluidtopics.net/access?context=configure-risk-identification-form&family=xanadu&ft:locale=en-US)**

Respond to the risk identification questionnaires from the [Assessment Workspace](https://servicenow-staging.fluidtopics.net/access?context=sae-asmnt-workspace&family=xanadu&ft:locale=en-US) with an interactive and intuitive user experience. Risk admin can select between classic and smart assessment questionnaire in the risk identification configuration without making it a forced behavior. You can migrate an existing risk identification template to the Smart Assessment Engine application. You can also create risk identification templates in the [Assessment Workspace](https://servicenow-staging.fluidtopics.net/access?context=sae-asmnt-workspace&family=xanadu&ft:locale=en-US).

**Note:** Only published assessment templates with a Risk Identification category are available for selection on the Risk Identification Configuration form.

-   **[Configuring currency conversion dates](https://servicenow-staging.fluidtopics.net/access?context=advanced-risk-properties&family=xanadu&ft:locale=en-US)**

Define currency conversion dates for the risk event entries in the system properties. This feature enhances the accuracy of net loss calculations by enabling you to select specific dates for currency conversion rather than relying solely on the date of impact. You can select a currency conversion date at the system property level from the following options:

    -   Risk event entry date
    -   First loss entry date
    -   Last loss entry date
    -   First recovery entry date
    -   Last recovery entry date
    -   Custom date
**Note:** You can also override the defined currency conversion dates in the risk response template configuration. These changes apply to both new and ongoing risk event workflows.

-   **[Reopen closed risk events](https://servicenow-staging.fluidtopics.net/access?context=reopen-a-risk-event&family=xanadu&ft:locale=en-US)**

Reopen closed risk events to update existing risk events with new discoveries, losses, or relevant information without creating new risk events. This feature saves time and effort, offering flexibility and boosting efficiency in managing risk events. You can reopen a risk event individually or in bulk.

-   **Miscellaneous enhancements and improvements**

Streamline your processes with the following enhancements:

    -   Notify the risk assessor with a notification email when a risk assessment is approved or rejected.
    -   Define a specific group as the respondent type in the Feedback Integration Configuration form when the target record doesn't have a user or group. For more information, see [Configure a feedback integration](https://servicenow-staging.fluidtopics.net/access?context=configure-feedback-integration&family=xanadu&ft:locale=en-US).
    -   Configure a single currency mode for advanced risk assessments. This feature displays all financial values in the selected single currency, confirming consistency and clarity in all fields. For more information, see [Single-currency mode](https://servicenow-staging.fluidtopics.net/access?context=single-currency-mode&family=xanadu&ft:locale=en-US).
    -   View the completion date of the most recent risk identification in the new field **Last completed date**, added to the Risk Identification form. For more information, see [Set up risk identification integration](https://servicenow-staging.fluidtopics.net/access?context=configure-risk-identification-form&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

-   The Risk portal has been deprecated, and a navigation link has been added to access the new Risk portal.

</td></tr><tr><td>

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

Xanadu

</td><td>

Install Advanced Risk by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

-   Create multidimensional entities by combining two or more entities from different entity classes and manage risks and controls for such composite entities.
-   Perform assessment on multiple risks and controls by creating a risk assessment project.
-   Use a uniform workflow for all types of risk response strategies, enable dynamic approvals using GRC: Approver Configurator, and create multiple strategies with various action items for each risk response plan.
-   Link the open risk response tasks or copy the tasks along with the risk response strategy from the previous assessment when reassessing the risk.
-   Create an issue or link an existing open issue as an outcome of the risk assessment.
-   Respond to risk identification questionnaires with an improved user experience using Smart Assessment Engine.
-   Reopen closed risk events to identify and address overlooked or underestimated risks, updating existing risk events instead of creating new risk events.

 See [Advanced Risk Assessment](https://servicenow-staging.fluidtopics.net/access?context=advanced-risk-assessment&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-xanadu-zurich/rn-combined-intro.md)

