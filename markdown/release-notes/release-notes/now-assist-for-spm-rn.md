---
title: Now Assist for Strategic Portfolio Management \(SPM\) release notes
description: The ServiceNow Now Assist for Strategic Portfolio Management \(SPM\) application introduces generative AI skills into Strategic Portfolio Management. You can summarize feedback or content in Docs, create stories from epics, generate concise project summaries, create demands through conversations, quickly gain insights into projects, and refine planning item descriptions to enhance clarity and ensure alignment with project goals. Now Assist for Strategic Portfolio Management \(SPM\) is updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
---

# Now Assist for Strategic Portfolio Management \(SPM\) release notes

The ServiceNow® Now Assist for Strategic Portfolio Management \(SPM\) application introduces generative AI skills into Strategic Portfolio Management. You can summarize feedback or content in Docs, create stories from epics, generate concise project summaries, create demands through conversations, quickly gain insights into projects, and refine planning item descriptions to enhance clarity and ensure alignment with project goals. Now Assist for Strategic Portfolio Management \(SPM\) is updated in the Yokohama release.

## Now Assist for SPM highlights for the Yokohama release

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Generate measurable targets from goals information and optional context with the target generation skill.
-   Use the identify similar records skill to find similar demands based on contextual similarity.
-   Enable the project task monitor AI agent to autonomously monitor project tasks on the critical path of a project.
-   Use the **Send preview** button to share a project insights email instantly.

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Use a decorative loader to elevate visual interest during content loading in Strategic Planning.
-   Refine the planning item text descriptions by enabling AI assistance.
-   Use Now Assist for SPM AI agents to help optimize workflows, improve productivity, and automate your tasks.

See [Now Assist for Strategic Portfolio Management \(SPM\)](https://www.servicenow.com/docs/access?context=now-assist-spm&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US) for more information.

## New in the Yokohama release

-   **[Identify similar records using Now Assist](https://www.servicenow.com/docs/access?context=identify-similar-demand-records&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Detect similar existing demand records when creating or editing a demand using the identify similar records skill. The skill compares the **Name**, **Description**, and **Business Case** fields for contextual similarity.

-   **[Accelerate target creation with the target generation skill](https://www.servicenow.com/docs/access?context=generate-targets-for-goal&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Generate measurable targets from goals information and optional context with the target generation skill. The skill automatically populates key fields in the target creation form, helping teams define clear, measurable outcomes and create targets quickly.

-   **[Schedule project insights email](https://www.servicenow.com/docs/access?context=email-project-summary-skill-pw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   Schedule project insights email in the Configure project insights modal. The project email is emailed to the project managers and users and continues on the selected schedule that you select until the project is inactive or paused.
    -   Schedule and instantly send the project insights email to your project managers by selecting the **Send preview** button.
    -   Track important updates such as the delayed end dates, the status turning red, or the state updates of your projects and receive project insights email on the schedule that you select.
    -   Select the email frequency that works for you: weekly, bi-weekly or monthly.
    -   Monitor critical elements such as milestones, resources, projects, and project tasks.
    -   Receive proactive, AI-based notifications when project milestones or critical tasks could lead to delays using Monitor project task agent. Use the Enable critical task alerts option from planning page to enable the project task monitor AI agent.
    -   Choose the recipients to whom you want to send the project insights email.

-   **[New third-party AI model provider options available for Now Assist](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Google Gemini 2.0 Flash, Google Gemini 2.5 Pro, and AWS Claude 3.7 Sonnet are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI GPT-4.1 and GPT-4.1 mini.

-   **[Write planning item skill](https://www.servicenow.com/docs/access?context=using-now-assist-for-spm&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   Use this skill to improve record quality and user satisfaction by enabling AI assistance in the Description field across all Strategic Planning Workspace forms, including product idea, demand, epic, project, capability, feature, and story.
    -   Enable text refinement with the **Elaborate** and **Shorten** options on planning items to support product managers and agile team members in creating and editing content more effectively.

## UI changes

-   **[More actions context menu UI enhancements](https://www.servicenow.com/docs/access?context=email-project-summary-skill-pw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   Email project summary option has been renamed to Configure project insights.
    -   Enable critical task alerts option has been added.
    -   Disable critical task alerts option has been added.
-   **[Configure project insights modal UI enhancements](https://www.servicenow.com/docs/access?context=email-project-summary-skill-pw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   Email project summary modal has been renamed to Configure project insights modal.
    -   **Disable email summary** check box has been renamed to **Pause cadence** check box.
    -   Choose topics, personalize content, and set frequency setup have been added.
    -   **Project tasks**, **Milestones**, and **Resources** check boxes have been added.
    -   **Include critical path task changes** check box has been removed.
    -   **Schedule and send** button has been renamed to **Schedule** button.
    -   **Send preview** button has been added to send an email instantly.
-   **[Skill name updates](https://www.servicenow.com/docs/access?context=email-project-summary-skill-pw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    The email project summary skill has been renamed to the project insights generation skill.

-   **[Demand Management UI changes](https://www.servicenow.com/docs/access?context=identify-similar-demand-records&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   The **Identify similar demands** button has been added to the demand form to identify and view any similar demands with the identify similar demands skill.
    -   The Similar Demands related list has been added, which displays the list of similar demand records identified by Now Assist.
-   **[UI enhancements](https://www.servicenow.com/docs/access?context=now-assist-spm&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    The following UI enhancements were made:

    -   Added hover animation for the Now Assist \(![now-assist-icon.](../../product/now-assist-spm/images/now-assist-icon-spm.png)\) icon.
    -   Added a loader for the Now Assist side panel for a more engaging loading experience.
-   **[Skill name updates](https://www.servicenow.com/docs/access?context=now-assist-spm&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   Renamed the Project Gen AI Docs skill to the Project doc summarization \(Project Workspace\) skill.
    -   Renamed the Planning item Gen AI Docs skill to the Planning item doc summarization \(Strategic Planning\) skill.
    -   Renamed the EAP Teams Gen AI Docs skill to the EAP doc summarization \(Enterprise Agile Planning\) skill.
    -   Renamed the Story generation skill to Agile story generation \(Enterprise Agile Planning\).
    -   Added the Write planning items skill in Strategic Planning.
-   **[Animation support for Now assist buttons and icons](https://www.servicenow.com/docs/access?context=now-assist-spm&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   Added hover animation in the Now Assist \(![summarize-button.](../../product/spw-product-feedback/image/summarize-na-button.png)\) icon for the **Summarize** button on the feedback list and Docs.
    -   Added the Now Assist \(![email-project-summary-button.](../../product/project-workspace/image/email-project-summary-na-button.png)\) icon in the Email project summary button.
    -   Added hover animation in the Now Assist \(![summarize-button-on-docs-page.](../../product/spw-product-feedback/image/summarize-docs-page-button.png)\) icon for the Now Assist button in the Docs page.

## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


## Activation information

Now Assist features are available with activation of the [Now Assist for Strategic Portfolio Management \(SPM\)](https://www.servicenow.com/docs/access?context=now-assist-spm&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US) plugin. The Now Assist for SPM application requires a Strategic Portfolio Management \(SPM\) Pro plus license. For more information, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    ServiceNow® Now Assist uses generative AI to help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The Now Assist Admin console provides you with quick and easy access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use this conversational interface in the EAP workspace to get story recommendations, split or combine stories, and create stories for your epics with the help of generative AI.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Now Assist products provide generative AI skills that are tailored to meet the needs of users in different workflows, including feedback summarization, content summarization in Docs, demand creation, and epic to story generation.


**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

**Parent Topic:**[Strategic Portfolio Management release notes](it-business-management-rn-landing.md)

