---
title: Configure ServiceNow Otto for HRSD skills
description: Learn which AI skills are auto-activated and which require you to activate and configure. Alternatively, you can duplicate a generative AI skill to experiment with skill settings and configure the skill to fit your business needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/now-assist-for-hrsd/customize-nahr-skill.html
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: concept
last_updated: "2026-10-19"
reading_time_minutes: 7
breadcrumb: [Configure, ServiceNow Otto for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Configure ServiceNow Otto for HRSD skills

Learn which AI skills are auto-activated and which require you to activate and configure. Alternatively, you can duplicate a generative AI skill to experiment with skill settings and configure the skill to fit your business needs.

## ServiceNow Otto for HRSD skills

Use the AI Admin Hub to activate and configure ServiceNow Otto for HR Service Delivery \(HRSD\) generative AI skills.

The following list contains skills that are available with the ServiceNow Otto for HRSD plugin. Some skills require additional plugins to be installed.

Some skills are automatically activated with the ServiceNow Otto for HR Service Delivery \(HRSD\) plugin. For all other skills, an admin must activate the skills to make them available for HR agents and managers to use.

|Skill|Description|Additional plugin required?|Activation required?|
|-----|-----------|---------------------------|--------------------|
|Activity Response Generation for HR Case|Generates a suggested response for an activity on an HR case, so agents can reply to employees faster.|None|Yes, see [Configure Activity Response Generation for HR Case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-activity.md)|
|Case summarization|Summarizes an HR case, including key details, actions taken, and current status, so agents can get up to speed quickly.|None|Auto-activated|
|Chat reply recommendation|Suggests a reply for the agent to send during a live chat with an employee, based on the conversation so far.|None|Auto-activated|
|Chat summarization|Summarizes a live chat conversation between an agent and an employee, so the agent can review or hand off the interaction.|None|Auto-activated|
|Email recommendation|Drafts a suggested email response for an HR case, based on the case details and the email thread.|None|Auto-activated|
|KB generation|Creates a draft knowledge article from a resolved HR case, so agents can share solutions with other employees.|None|Yes|
|Resolution notes generation|Writes resolution notes for an HR case from its details and activity, so agents can close cases with less manual effort.|None|Auto-activated|
|Sentiment analysis for HR Case|Analyzes the tone of an HR case and its related communications to show how the employee is feeling.|None|Yes|
|Sentiment analysis for HR Task|Analyzes the tone of an HR task and its related communications to show how the employee is feeling.|None|Yes|
|Sidebar discussion summarization|Summarizes the sidebar discussion on an HR case, so agents can quickly catch up on collaboration between team members.|None|Auto-activated|
|Job description skill relevance|Identifies which skills are most relevant to a job description, so HR teams can match roles to the right skills.|Journey designer|Yes|
|Journey generation for managers|Generates a journey for managers, such as an onboarding plan, from details about the employee and the role.|Journey designer|Yes|
|Journey Relevant Catalog Items|Recommends catalog items that fit a journey, so managers can add the right requests and resources to it.|Journey designer|Yes|
|Journey summarization for managers|Summarizes the progress and status of an employee journey, so managers can see what is done and what is pending.|Journey designer|Yes|
|Knowledge transfer document grouper|Groups related documents into logical sets, so departing employees can hand off knowledge in an organized way.|Journey designer|Yes|
|Interview note skill relevance|Identifies which skills are most relevant to interview notes, so hiring teams can assess how well a candidate fits a role.|Journey designer|Yes|
|Resume Skill Extraction|Extracts skills from a resume, so HR teams can match candidates and employees to roles.|Journey designer|Yes|
|Skill keyword extractor|Extracts skill-related keywords from text, such as job descriptions or notes, so they can be mapped to a skills taxonomy.|Journey designer|Yes|
|Employee information summarization|Summarizes key information about an employee, so agents and managers can see the context they need without searching multiple records.|Talent|Yes|
|Generate talking points|Creates talking points for a manager to use in a conversation with an employee.|Talent|Yes|
|Manager insights|Provides managers with a summary of insights about their team, helping them spot trends and decide what to do next.|Talent|Yes, see [Configure manager insights for ServiceNow Otto for HRSD](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/config-manager-insights.md)|

## Skill components

Each skill has its own configuration process, depending on the components. Common configuration components include the following:

-   **Trigger:** Allows you to configure the circumstances in which a skill is generated. For example, chat summarizations can be configured to generate when the chat handoff is done from a live agent to a live agent.
-   **Input:** Configure the data used to create the information generated by the skill. For example, resolution notes information is generated from the description, short description, work notes, and the additional comments fields of existing case notes.
-   **Availability:** Customize how and when the skill capability is active and accessible. For example, email reply recommendations can be configured to be available, or defined using the condition builder to determine whether a user can activate the skill.
-   **Access:** Determine who can access this skill. By selecting specific roles, you control who can use it. The roles you choose are also available in the next step, **Select display**.
-   **Display:** Determine where the skill appears. For example, the call summarization skill can be configured to display on forms and workspaces or in the ServiceNow Otto panel.

For more information on the inputs and triggers for each skill, see [Skill inputs and triggers for ServiceNow Otto for HRSD](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-skill-inputs.md).

## Customize skills

The skills that come with the ServiceNow Otto applications have default configurations that are optimized to serve the most common use cases. The base system skills can be tailored to meet specific business requirements. Customization ensures that skills align with your organization's workflows, data sources, and user roles. There are two main ways to customize:

-   Using AI Admin Hub: Modify base system skills, input configurations, and display settings. Make a copy of the skill as you cannot directly modify the base system skill. For more information, see [Make a copy of an AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/make-a-copy-of-a-now-assist-skill.md).
-   Using AI Skill Kit: Build and publish custom skills for advanced use cases by customizing inputs and prompts, and then publish it. You can also use the AI Skill Kit to clone base system skills. For more information, see [Using AI Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/using-now-assist-skill-kit.md).

Unified Admin Experience for GenAI Skills:

-   Previously, skills cloned in AI Admin Hub console supported only prompt configuration in AI Skill Kit. Input configuration could not be edited in AI Skill Kit, creating a fragmented setup process. With the new unified admin experience, users can manage GenAI skills seamlessly in AI Skill Kit. This includes adding necessary headers as input, configuring or editing prompts, and maintaining all settings in a single location.
-   The unification migrates the AI Admin Hub console setup experience to AI Skill Kit for all configured skills in ServiceNow Otto for HRSD.

-   **[Activate skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/activate-skills.md)**  
Enable HR Service Delivery skills to give managers and HR agents generative AI capabilities.
-   **[Configure Activity Response Generation for HR Case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-activity.md)**  
Set up the activity response generation skill in the AI Admin Hub console to enable automated responses in comments and work notes of an HR case.
-   **[Configure attachment summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/configue-attachment-summary.md)**  
Customize the case summarization skill in ServiceNow Otto for HRSD to include summaries of case attachments.
-   **[Configure manager insights for ServiceNow Otto for HRSD](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/config-manager-insights.md)**  
Configure the manager insights skill in ServiceNow Otto for HRSD to generate a summary of team data in Manager Hub.
-   **[Configure resolution notes generation for ServiceNow Otto for HRSD](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/resolution-notes-nacm-config.md)**  
Configure the resolution notes generation skill to create concise summaries of case resolutions and enable agents to use the ServiceNow Otto context menu to elaborate or shorten the notes.
-   **[Restrict ServiceNow Otto capabilities for employee relations cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/restrict-now-assist-skills-er-cases.md)**  
Restrict the ServiceNow Otto capabilities for your employee relations cases and define the availability.
-   **[Skill inputs and triggers for ServiceNow Otto for HRSD](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-skill-inputs.md)**  
Get a quick overview of the skill inputs and triggers for ServiceNow Otto for HR Service Delivery \(HRSD\). By configuring the inputs or triggers for a skill, you can determine how and when a skill is used.

**Parent Topic:**[Configure ServiceNow Otto for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/configure-now-assist-hr.md)

