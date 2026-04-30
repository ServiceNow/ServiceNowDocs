---
title: Advanced Risk release notes
description: The ServiceNow Advanced Risk application enables you to identify, analyze, evaluate, treat, and monitor risks that could impact your organization in achieving its business objectives. Advanced Risk was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
---

# Advanced Risk release notes

The ServiceNow® Advanced Risk application enables you to identify, analyze, evaluate, treat, and monitor risks that could impact your organization in achieving its business objectives. Advanced Risk was enhanced and updated in the Yokohama release.

## Advanced Risk highlights for the Yokohama release

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.

-   Use generative AI to generate risk assessment summaries and highlight key insights for better context.
-   Reassess completed risk assessment projects to evaluate risks based on new insights or changing conditions.
-   Copy risk responses from a previous risk assessment during reassessment of a risk assessment project.
-   Reassign assessors for multiple risk assessment projects to optimize resource allocation.
-   Remove risks from a risk assessment project during the assessment to streamline focus on relevant risks.
-   Enable and manage the risk response task workflow from the Risk Assessment Methodology \(RAM\) form.

See [Advanced Risk Assessment](https://www.servicenow.com/docs/access?context=advanced-risk-assessment&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** Advanced Risk is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Generative AI risk assessment summarization](https://www.servicenow.com/docs/access?context=generate-risk-assessment-summary-genai&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Generate a risk assessment summary from your inherent, residual, target risks, and control effectiveness data using the Now Assist for IRM application. The summary highlights key insights to help your approvers quickly understand the context before approving the risk assessments. You can also analyze details such as open issues, risk response tasks, action items, and calculated risk scores to support your approval decision. Check your entitlements to confirm whether you have access to risk assessment summarization.

-   **[Reassess a risk assessment project](https://www.servicenow.com/docs/access?context=reassess-risk-assessment-project&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Review completed risk assessment projects to reflect new insights or changing conditions. All previously assessed risks in this project are automatically carried over and reassigned to the designated assessor. Confirm continuity, minimize manual effort, and enhance efficiency in your risk management process.

-   **[Copy risk responses from the previous assessment](https://www.servicenow.com/docs/access?context=perform-assessment-on-risk-assessment-project&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Copy responses from a previous risk assessment during the reassessment of a risk assessment project to streamline the assessment process. All prior responses are automatically copied, saving time and maintaining consistency.

-   **[Remove risks from assessment](https://www.servicenow.com/docs/access?context=perform-assessment-on-risk-assessment-project&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    As a risk assessor, you can remove risks from the risk assessment project while performing the assessment, which also removes all responses associated with that risk. Removed scoped risks remain part of the project but are marked as not applicable for reporting purposes. However, removed ad hoc risks are completely deleted.

-   **[Manage risk response task workflow](https://www.servicenow.com/docs/access?context=configure-ram&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Manage and enable the risk response task workflow from the RAM form to enable users to create, delete, remove, edit, and link risk response tasks within an assessment.

-   **[Reassign assessor for a risk assessment project](https://www.servicenow.com/docs/access?context=reassign-assessor-for-risk-assessment-project&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Reassign assessors for multiple in-progress risk assessment projects simultaneously to minimize disruptions during stakeholder transitions.

-   **[Configure risk color styles for the Next Experience](https://www.servicenow.com/docs/access?context=create-risk-color-style&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Define and preview colors for the risk and advanced risk components in the Next Experience through a configurable system rather than having to use hex codes. The transition has been made from a hex code color management system to a configurable system that supports the highlighted value component colors. This feature addresses theming and accessibility issues. You can define the color and variant, and preview them using the Next Experience color styles tab on the Risk color style form.

    **Note:** The default color for the customized risk color style is set to Critical, with the variant set to Primary. You can manually change the color and variant based on the requirement.


## Changed in this release

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


## Activation information

Install Advanced Risk by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[GRC Risk Management](https://www.servicenow.com/docs/access?context=grc-risk-overview&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Use the Risk Management application with the ServiceNow® Advanced Risk application to identify and monitor high-impact risks, improve your risk-based decision-making, and reduce reaction time.

-   **[GRC Risk Workspace](https://www.servicenow.com/docs/access?context=risk-workspace&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Using Risk Workspace with the ServiceNow® Advanced Risk application provides a simplified user experience with a single-pane view for all your risk-related activities.


**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

