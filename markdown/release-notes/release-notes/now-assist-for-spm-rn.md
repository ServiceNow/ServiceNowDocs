---
title: Now Assist for Strategic Portfolio Management \(SPM\) release notes
description: The ServiceNow Now Assist for Strategic Portfolio Management \(SPM\) application introduces generative AI skills into Strategic Portfolio Management. You can summarize feedback or content in Docs, create stories for epics, generate project insights, create demands through conversations, and quickly gain updates into projects. Now Assist for Strategic Portfolio Management \(SPM\) was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
keywords: [Now Assist for SPM, Now Assist, AI agents, Agentic AI]
---

# Now Assist for Strategic Portfolio Management \(SPM\) release notes

The ServiceNow® Now Assist for Strategic Portfolio Management \(SPM\) application introduces generative AI skills into Strategic Portfolio Management. You can summarize feedback or content in Docs, create stories for epics, generate project insights, create demands through conversations, and quickly gain updates into projects. Now Assist for Strategic Portfolio Management \(SPM\) was enhanced and updated in the Zurich release.

## Now Assist for SPM highlights for the Zurich release

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   All Now Assist for SPM skills are activated by default.
-   Use the identify similar records skill to find similar demands based on contextual similarity.
-   Enable the project task monitor AI agent to autonomously monitor project tasks on the critical path of a project.
-   Use the **Send preview** button to share a project insights email instantly.
-   Generate measurable targets from goals information and optional context with the target generation skill.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

See [Now Assist for Strategic Portfolio Management \(SPM\)](https://www.servicenow.com/docs/access?context=now-assist-spm&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US) for more information.

## New in the Zurich release

-   **[Schedule project insights email](https://www.servicenow.com/docs/access?context=email-project-summary-skill-pw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Schedule project insights email in the Configure project insights modal. The project email is emailed to the project managers and users and continues on the selected schedule that you select until the project is inactive or paused.
    -   Schedule and instantly send the project insights email to your project managers by selecting the **Send preview** button.
    -   Track important updates such as the delayed end dates, the status turning red, or the state updates of your projects and receive project insights email on the schedule that you select.
    -   Select the email frequency that works for you: weekly, bi-weekly or monthly.
    -   Monitor critical elements such as milestones, resources, projects, and project tasks.
    -   Receive proactive, AI-based notifications when project milestones or critical tasks could lead to delays using Monitor project task agent. Use the Enable critical task alerts option from planning page to enable the project task monitor AI agent.
    -   Choose the recipients to whom you want to send the project insights email.
-   **[Identify similar records using Now Assist](https://www.servicenow.com/docs/access?context=identify-similar-demand-records&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Detect similar existing demand records when creating or editing a demand using the identify similar records skill. The skill compares the **Name**, **Description**, and **Business Case** fields for contextual similarity.

-   **[Accelerate target creation with the target generation skill](https://www.servicenow.com/docs/access?context=generate-targets-for-goal&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Generate measurable targets from goals information and optional context with the target generation skill. The skill automatically populates key fields in the target creation form, helping teams define clear, measurable outcomes and create targets quickly.

-   **[Generate acceptance criteria for stories](https://www.servicenow.com/docs/access?context=eap-generate-acceptance-criteria-for-stories&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Generate clear, consistent acceptance criteria for user stories with the acceptance criteria generation skill. By leveraging story context and predefined templates, the skill helps you align with requirements.

-   **[Enhancements to Story generation](https://www.servicenow.com/docs/access?context=generate-stories-from-epics-now-assist-eap&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Use the upgraded agile story generation skill to convert epics into actionable user stories quickly. Powered by an agentic workflow, the skill analyzes epic details to recommend the optimal number of stories, enables adjustments, refines story content, and creates story records.


-   **[Improve efficiency and quality using refine records skill with Now Assist Context Menu](https://www.servicenow.com/docs/access?context=refine-text-with-write-planning-item-skill&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Simplify record creation and updates by using the refine records skill with Now Assist context menu. Improve record quality by enabling AI-assisted text refinement in the text fields of Product idea, Demand, Epic, Projects, Capability, Feature, Stories, Project tasks, Risks, Strategic priorities, Goals, Targets, Initiatives, Feedback, Milestones, and Story forms.


-   **[Configure ACLs for custom roles](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Update the ACLs for custom roles that require access to Now Assist skills.

-   **[Generate and improve Docs content](https://www.servicenow.com/docs/access?context=generate-summarize-and-refine-content-of-docs-with-now-assist-spm&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Help improve your content and productivity with the ability to enter custom prompts directly in the Docs, alongside the Summarize, Elaborate, and Shorten options.

    Generate content with Now Assist for SPM directly in your Docs. In addition, summarize existing sections, elaborate where needed, and refine drafts to help improve your productivity.

    You can interact with Now Assist directly in your Doc to create content, add context, or improve existing sections.


-   **[New third-party AI model provider options available for Now Assist](https://www.servicenow.com/docs/access?context=ai-model-providers&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Google Gemini 2.0 Flash, Google Gemini 2.5 Pro, and AWS Claude 3.7 Sonnet are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI GPT-4.1 and GPT-4.1 mini.


## UI changes

-   **[More actions context menu UI enhancements](https://www.servicenow.com/docs/access?context=email-project-summary-skill-pw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Email project summary option has been renamed to Configure project insights.
    -   Enable critical task alerts option has been added.
    -   Disable critical task alerts option has been added.
-   **[Configure project insights modal UI enhancements](https://www.servicenow.com/docs/access?context=email-project-summary-skill-pw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Email project summary modal has been renamed to Configure project insights modal.
    -   **Disable email summary** check box has been renamed to **Pause cadence** check box.
    -   Choose topics, personalize content, and set frequency setup have been added.
    -   **Project tasks**, **Milestones**, and **Resources** check boxes have been added.
    -   **Include critical path task changes** check box has been removed.
    -   **Schedule and send** button has been renamed to **Schedule** button.
    -   **Send preview** button has been added to send an email instantly.
-   **[Skill name updates](https://www.servicenow.com/docs/access?context=email-project-summary-skill-pw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    The email project summary skill has been renamed to the project insights generation skill.

-   **[Demand Management UI changes](https://www.servicenow.com/docs/access?context=identify-similar-demand-records&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   The **Identify similar demands** button has been added to the demand form to identify and view any similar demands with the identify similar demands skill.
    -   The Similar Demands related list has been added, which displays the list of similar demand records identified by Now Assist.
-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Email project summary modal UI changes](https://www.servicenow.com/docs/access?context=configure-agents-project-task-monitoring&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   The **Enable AI Agents to monitor task changes on the critical path** check box has been added.
    -   The **Users** option has been added under Recipients to add recipients or users for the project summary email.

## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.

-   **[ppm.ai\_project\_manager\_agent user role](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The agentic workflow, agents, and scheduled jobs are configured to run under the new ppm.ai\_project\_manager\_agent user role instead of the administrator account.


## Activation information

Now Assist features are available with activation of the [Now Assist for Strategic Portfolio Management \(SPM\)](https://www.servicenow.com/docs/access?context=now-assist-spm&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US) plugin. For more information, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    ServiceNow® Now Assist uses generative AI to help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Overview tab in Now Assist Admin](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The Now Assist Admin console provides you with quick and easy access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist panel conversational interface in the Enterprise Agile Planning workspace to get story recommendations, split or combine stories, and create stories for your epics with the help of generative AI.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Now Assist products provide generative AI skills that are tailored to meet the needs of users in different workflows, including feedback summarization, content summarization in Docs, demand creation, and epic to story generation.


**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

**Parent Topic:**[Strategic Portfolio Management release notes](it-business-management-rn-landing.md)

