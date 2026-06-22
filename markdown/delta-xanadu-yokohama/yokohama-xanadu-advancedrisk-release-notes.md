---
title: Combined Advanced Risk release notes for upgrades from Xanadu to Yokohama
description: Consolidated page of all release notes for Advanced Risk from Xanadu to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-xanadu-yokohama/yokohama-xanadu-advancedrisk-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 11
breadcrumb: [Products combined by family]
---

# Combined Advanced Risk release notes for upgrades from Xanadu to Yokohama

Consolidated page of all release notes for Advanced Risk from Xanadu to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Advanced Risk release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Advanced Risk to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Advanced Risk.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Create multidimensional entities](https://www.servicenow.com/docs/access?context=create-composite-entity-ws&family=xanadu&ft:locale=en-US)**

Create multidimensional entities by combining two or more entities from different entity classes using the Composite Entity Management application. You can create multidimensional entity classes with a composite entity structure, such as Company \| Department \| Business Process. After defining the composite entity class, you can create composite entity that operates as a standalone entity. This feature enables you to manage risk and compliance workflows at the composite entity level, providing visibility into the combined risk and compliance posture.

**Note:** Composite entity classes can be created in both the classic UI and the Risk Workspace. The creation of composite entities is supported only in Risk Workspace.

-   **[Assess multiple risks and controls simultaneously](https://www.servicenow.com/docs/access?context=risk-assessment-project&family=xanadu&ft:locale=en-US)**

Create a risk assessment project to perform bulk assessments on multiple risks and controls, enabling assessors to evaluate them in a single project. This approach reduces time and effort, confirms consistency across multiple assessments, and provides a more comprehensive view of risks and controls within the same project. You can scope multiple risks related to the assessable entity within the project and perform assessments.

**Note:** Assessment of multiple risks and controls is supported only in Risk Workspace.

-   **[Addition of new roles](https://www.servicenow.com/docs/access?context=risk-assessment-project&family=xanadu&ft:locale=en-US)**

The following roles related to risk assessment project were added:

    -   Risk assessment project reader \[sn\_risk\_advanced.risk\_asmt\_project\_reader\]: Provides read only access to the risk assessment projects.
    -   Risk assessment project user \[sn\_risk\_advanced.risk\_asmt\_project\_user\]: Provides the ability to create risk assessment projects and update or delete only the projects created by the user.
    -   Risk assessment project manager \[sn\_risk\_advanced.risk\_asmt\_project\_manager\]: Provides the ability to create, update, and delete any risk assessment projects.
-   **[Enhanced risk response workflow](https://www.servicenow.com/docs/access?context=workflow-of-risk-response-task&family=xanadu&ft:locale=en-US)**

Streamline your risk response workflow with the following enhancements:

    -   Use a uniform workflow for all types of risk response tasks. A standardized workflow for risk response tasks enhances the management of all types of risk response tasks, promotes consistency, and reduces the need for customization.
    -   Configure multiple levels of approvals for the risk response tasks using the approval configurator. By default, a single level of approval is enabled for all types of risk response tasks, where the risk owner can approve the tasks. These approvals can be configured based on requirements.
    -   Reject a risk response task and move it to the work in progress state without closing it. This feature helps the risk response task owner to modify the response strategy if the approver is unsatisfied with the response.
    -   Create action items with an independent workflow and link them to the risk response tasks when they are in the Draft or Work in progress state.

**Note:** You can create risk response action items for all types of risk responses except for Risk acceptance tasks.

    -   Copy risk response plans from the previous risk assessment to the current risk assessment while reassessing.
    -   Link an open risk response task from the previous assessment to the current risk assessment while reassessing. You can also edit or remove an existing risk response task.
-   **[Issue linking with risk assessments](https://www.servicenow.com/docs/access?context=perform-ara-workspace&family=xanadu&ft:locale=en-US)**

Streamline your risk assessments with the following enhancements:

    -   Enable the issue linking option on the Risk Assessment Methodology \(RAM\) form to create an issue or link an existing open issue with the risk assessment.
    -   View issue details from the configurable issue card available on the risk assessment.
    -   Identify newly created issues from existing linked issues with a visual differentiator on the issue card.
    -   Edit or remove issues.
-   **[Enhanced risk event task workflow](https://www.servicenow.com/docs/access?context=manage-risk-events&family=xanadu&ft:locale=en-US)**

Streamline your risk event workflow with the following enhancements:

    -   Use a uniform and enhanced workflow for the risk event tasks. A standardized workflow enhances the management of risk event tasks.
    -   Configure multiple levels of approvals for the risk event tasks using the approval configurator.
    -   Reject a risk event task and move it to the work in progress state without closing it. This feature helps the risk event task owner to modify the risk event if the approver is unsatisfied.
-   **[Improved user experience for risk identification questionnaire using Smart Assessment Engine](https://www.servicenow.com/docs/access?context=configure-risk-identification-form&family=xanadu&ft:locale=en-US)**

Respond to the risk identification questionnaires from the [Assessment Workspace](https://www.servicenow.com/docs/access?context=sae-asmnt-workspace&family=xanadu&ft:locale=en-US) with an interactive and intuitive user experience. Risk admin can select between classic and smart assessment questionnaire in the risk identification configuration without making it a forced behavior. You can migrate an existing risk identification template to the Smart Assessment Engine application. You can also create risk identification templates in the [Assessment Workspace](https://www.servicenow.com/docs/access?context=sae-asmnt-workspace&family=xanadu&ft:locale=en-US).

**Note:** Only published assessment templates with a Risk Identification category are available for selection on the Risk Identification Configuration form.

-   **[Configuring currency conversion dates](https://www.servicenow.com/docs/access?context=advanced-risk-properties&family=xanadu&ft:locale=en-US)**

Define currency conversion dates for the risk event entries in the system properties. This feature enhances the accuracy of net loss calculations by enabling you to select specific dates for currency conversion rather than relying solely on the date of impact. You can select a currency conversion date at the system property level from the following options:

    -   Risk event entry date
    -   First loss entry date
    -   Last loss entry date
    -   First recovery entry date
    -   Last recovery entry date
    -   Custom date
**Note:** You can also override the defined currency conversion dates in the risk response template configuration. These changes apply to both new and ongoing risk event workflows.

-   **[Reopen closed risk events](https://www.servicenow.com/docs/access?context=reopen-a-risk-event&family=xanadu&ft:locale=en-US)**

Reopen closed risk events to update existing risk events with new discoveries, losses, or relevant information without creating new risk events. This feature saves time and effort, offering flexibility and boosting efficiency in managing risk events. You can reopen a risk event individually or in bulk.

-   **Miscellaneous enhancements and improvements**

Streamline your processes with the following enhancements:

    -   Notify the risk assessor with a notification email when a risk assessment is approved or rejected.
    -   Define a specific group as the respondent type in the Feedback Integration Configuration form when the target record doesn't have a user or group. For more information, see [Configure a feedback integration](https://www.servicenow.com/docs/access?context=configure-feedback-integration&family=xanadu&ft:locale=en-US).
    -   Configure a single currency mode for advanced risk assessments. This feature displays all financial values in the selected single currency, confirming consistency and clarity in all fields. For more information, see [Single-currency mode](https://www.servicenow.com/docs/access?context=single-currency-mode&family=xanadu&ft:locale=en-US).
    -   View the completion date of the most recent risk identification in the new field **Last completed date**, added to the Risk Identification form. For more information, see [Set up risk identification integration](https://www.servicenow.com/docs/access?context=configure-risk-identification-form&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Generative AI risk assessment summarization](https://www.servicenow.com/docs/access?context=generate-risk-assessment-summary-genai&family=yokohama&ft:locale=en-US)**

Generate a risk assessment summary from your inherent, residual, target risks, and control effectiveness data using the Now Assist for IRM application. The summary highlights key insights to help your approvers quickly understand the context before approving the risk assessments. You can also analyze details such as open issues, risk response tasks, action items, and calculated risk scores to support your approval decision. Check your entitlements to confirm whether you have access to risk assessment summarization.

-   **[Reassess a risk assessment project](https://www.servicenow.com/docs/access?context=reassess-risk-assessment-project&family=yokohama&ft:locale=en-US)**

Review completed risk assessment projects to reflect new insights or changing conditions. All previously assessed risks in this project are automatically carried over and reassigned to the designated assessor. Confirm continuity, minimize manual effort, and enhance efficiency in your risk management process.

-   **[Copy risk responses from the previous assessment](https://www.servicenow.com/docs/access?context=perform-assessment-on-risk-assessment-project&family=yokohama&ft:locale=en-US)**

Copy responses from a previous risk assessment during the reassessment of a risk assessment project to streamline the assessment process. All prior responses are automatically copied, saving time and maintaining consistency.

-   **[Remove risks from assessment](https://www.servicenow.com/docs/access?context=perform-assessment-on-risk-assessment-project&family=yokohama&ft:locale=en-US)**

As a risk assessor, you can remove risks from the risk assessment project while performing the assessment, which also removes all responses associated with that risk. Removed scoped risks remain part of the project but are marked as not applicable for reporting purposes. However, removed ad hoc risks are completely deleted.

-   **[Manage risk response task workflow](https://www.servicenow.com/docs/access?context=configure-ram&family=yokohama&ft:locale=en-US)**

Manage and enable the risk response task workflow from the RAM form to enable users to create, delete, remove, edit, and link risk response tasks within an assessment.

-   **[Reassign assessor for a risk assessment project](https://www.servicenow.com/docs/access?context=reassign-assessor-for-risk-assessment-project&family=yokohama&ft:locale=en-US)**

Reassign assessors for multiple in-progress risk assessment projects simultaneously to minimize disruptions during stakeholder transitions.

-   **[Configure risk color styles for the Next Experience](https://www.servicenow.com/docs/access?context=create-risk-color-style&family=yokohama&ft:locale=en-US)**

Define and preview colors for the risk and advanced risk components in the Next Experience through a configurable system rather than having to use hex codes. The transition has been made from a hex code color management system to a configurable system that supports the highlighted value component colors. This feature addresses theming and accessibility issues. You can define the color and variant, and preview them using the Next Experience color styles tab on the Risk color style form.

**Note:** The default color for the customized risk color style is set to Critical, with the variant set to Primary. You can manually change the color and variant based on the requirement.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Advanced Risk features.

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
-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=yokohama&ft:locale=en-US)**




</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Advanced Risk features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Advanced Risk features or functionality were deprecated.

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

Install Advanced Risk by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

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

 See [Advanced Risk Assessment](https://www.servicenow.com/docs/access?context=advanced-risk-assessment&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Some Now Assist skills, agents, and agentic workflows are now turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

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

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-xanadu-yokohama/rn-combined-intro.md)

