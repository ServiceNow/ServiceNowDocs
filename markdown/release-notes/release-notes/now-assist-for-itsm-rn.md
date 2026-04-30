---
title: Now Assist for IT Service Management \(ITSM\) release notes
description: The ServiceNow Now Assist for IT Service Management \(ITSM\) application brings agentic AI to IT Service Management. Now Assist for IT Service Management \(ITSM\) was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 15
---

# Now Assist for IT Service Management \(ITSM\) release notes

The ServiceNow® Now Assist for IT Service Management \(ITSM\) application brings agentic AI to IT Service Management. Now Assist for IT Service Management \(ITSM\) was enhanced and updated in the Zurich release.

## Now Assist for IT Service Management \(ITSM\) highlights for the Zurich release

[Zurich Patch 8](../quality/zurich-patch-8.md)

-   Answer incident-related questions with context-aware agents using the Incident assist agentic workflow.
-   Generate summaries for Request Management records.

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Submit a catalog item for an account unlock using the voice AI agent.
-   Generate automatic responses for requests and requested items.
-   Use the ITSM Conversational Analytics dashboard that provides usage adoption performance metrics in Now Assist in Virtual Agent.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Some Now Assist skills are now turned on by default.
-   Add self-service and deflection to your phone channel with Voice AI agents.
-   Edit the incident summarization skill prompts and inputs within the Now Assist Skill Kit \(NASK\).
-   Use the Now Assist context menu to create AI-powered generative text.
-   Use agentic workflows in Change Management to quickly link configuration items \(CIs\) to a change request, intuitively create change requests, and easily associate outages with a change request.
-   Empower service desk agents to diagnose and resolve incidents on DEX monitored devices quickly and efficiently by using the  DEX issue diagnosis and resolution agentic workflow.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Use the Assess conflicts for a change request agentic workflow to run conflict detection for change requests and assess conflicts, identify affected CIs, and view the list of impacted services.
-   Use the Schedule a change agentic workflow to schedule change requests by identifying the available schedule slots.
-   Use the Explain SLA agentic workflow to understand the breakdown of task assignment and ownership for the SLA relevant to a specific incident, problem, case, or change request. Gain insight into the potential causes of a breach or delays.
-   Use the Assess quality of a Change Request agentic workflow to assess the quality of a change request, analyze the information available in the fields, and generate suggestions to improve the information in the fields.
-   Use the Wrap-up and resolve incident agentic workflow to resolve incidents, create, or attach Knowledge Base \(KB\) articles, update duplicate incident information, and attach Known Error \(KE\) articles to the incident record.

See [Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US) for more information.

**Important:** Now Assist for IT Service Management \(ITSM\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Now Assist for IT Service Management \(ITSM\) to Zurich

When you upgrade to the Zurich Patch 4 release, any customizations you may have made to the Now Assist context menu \(NACM\) won’t be preserved. For more information, see the Community article [Upgrade information for the NACM support in Now Assist for ITSM](https://www.servicenow.com/community/itsm-articles/upgrade-scenario-for-resolution-notes-generation-skill-in-itsm/ta-p/3415789).

The Incident assist agentic workflow is active by default and includes all the capabilities of the \[DEPRECATED\] Incident assist skill, with enhancements. When you upgrade to the [Zurich Patch 8](../quality/zurich-patch-8.md) release, if you have the \[DEPRECATED\] Incident assist skill activated, consider deactivating it to avoid redundancy. For more information, see [Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

## New in the Zurich release

-   **[Incident assist agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Answer incident-related questions using context-aware agents. Handle queries about incident details and get information about related records.

-   **[Enhancements to the Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    The features in the \[DEPRECATED\] Incident assist skill is available in the Incident assist agentic workflow. You may turn off this skill and use the agentic workflow that has enhanced capabilities.

-   **[Configure summaries for Request Management records](https://www.servicenow.com/docs/access?context=cust-now-assist-request-summarization-skill&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    As an admin, you can configure the following Request Management skills:

    -   Request summarization
    -   Requested item summarization
    -   Catalog task summarization
-   **[Summarize Request Management records](https://www.servicenow.com/docs/access?context=summarize-request-related-activity-response-generation&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    View an aggregate of all relevant updates and progress indicators in a single, dynamic summary.


-   **[Creating a catalog item for unlocking accounts using the voice AI agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Use the demo Submit account unlock catalog with the voice AI agent to create a catalog item to unlock the specified account when a user calls the help desk.

-   **[Enhancements to Troubleshoot Outlook issue with voice AI agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Email relevant troubleshooting articles and instructions to users when you troubleshoot Outlook issues for them.

-   **[ITSM Conversational analytics dashboard](https://www.servicenow.com/docs/access?context=using-itsm-conversational-analytics-dashboard&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Get insights into virtual agent adoption, usage trends, and track metrics in Now Assist in Virtual Agent.

-   **[Generate a response to request activity](https://www.servicenow.com/docs/access?context=summarize-request-related-activity-response-generation&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Automatically generate a response in record activity streams using the activity response generation skills for requests and requested items.

-   **[DEX issue diagnosis and resolution agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-dex-diagnosis-resolution-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Service desk agents can diagnose and resolve Zoom call quality issues using the DEX issue diagnosis and resolution agentic workflow, which integrates Zoom-specific diagnostics that correlate device, network, and application data.

-   **[AI-powered root cause analysis for Zoom call quality issues](https://www.servicenow.com/docs/access?context=investigate-and-resolve-zoom-call-issues&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Use Now Assist for Zoom call issues to identify the root cause of call quality degradation and review the supporting metric evidence for deeper insight. The analysis highlights the contributing device and network factors directly in the Zoom call quality view. Get the real-time guidance, including device ready remedial actions, contextual self-help instructions, and relevant Knowledge articles to help resolve the issue efficiently.

-   **[Get AI driven insights for boot time performance](https://www.servicenow.com/docs/access?context=investigate-and-resolve-boot-time-issues&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Monitor device boot time to identify slow start-up issues and use Now Assist to investigate the root cause and get suggested resolutions, including remedial actions, self-help instructions, and Knowledge articles to resolve boot performance problems quickly.


-   **[Adding self-service and deflection to phone channels using Voice AI agents](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Enhance employee productivity with Voice AI agents by adding self-service and deflection to their phone channel.

-   **[Getting password reset instructions using an AI agent](https://www.servicenow.com/docs/access?context=itsm-va-ai-agents&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    The **DEMO Password reset agent** is a demo AI agent that provides requesters with password reset instructions for the account that they need help with.

-   **[Editing the incident summarization skill prompts and inputs using the Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-record-summ-skill&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    You can edit the prompts and inputs for the incident summarization skill within the Now Assist Skill Kit \(NASK\) and test the updates you've made.

-   **[Expanding attachment summarization capabilities to include additional document formats and language](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-record-summ-skill&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    You can now summarize, analyze, and extract data from attachments in additional formats and languages.

-   **[Creating a knowledge article in any incident state](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-skill&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Create knowledge articles from any incident state by configuring a system property for the required states.

-   **[Edit a knowledge article when one article is attached to an incident](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-SOW-itsm&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    You can edit a knowledge article if your administrator has enabled the system property to display the **Edit knowledge** button and if you have only one article attached to the incident.

-   **[Enhancing the efficiency of the Investigate and resolve ITSM incidents agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-incident-resolver-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    For better efficiency, the ITSM incident resolution investigation AI agent and Find catalog item AI agent have been combined into one agent. This agent is called the ITSM incident resolution plan investigation AI agent.

-   **[Enhancing the efficiency of the Triage and categorize ITSM incidents agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-catincidents-usecase&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    For better efficiency, the Link major incident AI agent and the Link incident to problem AI agent have been combined into one agent. This agent is called the Link major incident or problem AI agent.

-   **[Enhancing the efficiency of the Generate change request plans agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-change-planner-usecase&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    For better efficiency, the existing six agents in the change request plans agentic workflow have been combined into one agent. This agent is called the Change request plans AI agent.

-   **[Display the risk factors sources that contribute to the calculation of a change risk explanation](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-change-risk-skill&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    When a change risk is calculated, Now Assist for ITSM provides the list of the change requests that were used to identify the potential risks for the change risk explanation so that you can understand which risk factors contributed to the calculated risk.

-   **[Generating resolution notes using the Now Assist context menu](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-gen-resolution-notes-skill&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    As an admin, you can view and configure the Now Assist context menu \(NACM\) to generate resolution notes using the **Resolution notes generation** skill.

-   **[Generating an activity response using the Now Assist context menu](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-activity-response-skill&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    As an admin, you can view and configure the Now Assist context menu \(NACM\) for an activity response using the **Incident activity response generation** skill.

-   **[Selecting the desired knowledge base and template for creating knowledge articles using the new interface](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-SOW-itsm&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    With this new interface, you can select the desired knowledge base and the template to create the article in Service Operations Workspace or Core UI.

-   **[Masking roles for controlled access to agentic workflows, AI agents, and skills](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-itsm&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Mask roles to restrict access to agentic workflows, AI Agents, and skills, ensuring that users receive only the necessary permissions.

-   **[Suggest configuration items for a change request agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-suggest-configuration-items-for-a-change-request&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Find and link applicable configuration items \(CIs\) to a change request from the Now Assist panel in a conversational and intuitive way using the Suggest configuration items for a change request agentic workflow.

-   **[Create outages for a change request agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-create-outages-for-a-change-request&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Associate outages with a change request in a conversational and intuitive way from the Now Assist panel using the Create outages for a change request agentic workflow.

-   **[Create standard change request agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-create-change-request-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Create a standard, normal, or emergency change request in a conversational and intuitive way from the Now Assist panel using the Create standard change request agentic workflow.

-   **[Create standard change template proposal agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-create-standard-change-template-proposal&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Create a change template proposal record based on similar change requests in a conversational and intuitive way from the Now Assist panel using the Create standard change template proposal agentic workflow.

-   **[DEX issue diagnosis and resolution agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-dex-diagnosis-resolution-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Diagnose and resolve issues on DEX monitored devices through a structured process that includes diagnosis of the cause, a resolution plan with actionable steps, and documenting the resolution in the incident record.

-   **[Generate comprehensive release notes for a release in Digital Product Release](https://www.servicenow.com/docs/access?context=dpr-generate-release-notes&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Automatically generate structured release notes for a release using the Generate Release Notes skill. This AI-driven capability compiles enhancements, features, incidents, and change records into structured notes with an executive summary and scope of work sections, reducing manual effort and ensuring consistency. You can edit the AI-generated draft as needed, then publish and share via link or PDF download.


-   **[Classify service and CI AI agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-catincidents-usecase&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Automatically assign the related service, service offering, and configuration item \(CI\) to an incident using the Classify service and CI AI agent in the Triage and categorize ITSM incidents agentic workflow.

-   **[Wrap-up and resolve incident agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-wrap-up-resolve-incident-aw&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Generate resolution notes including root cause and resolution steps to resolve an incident, create or attach Knowledge Base \(KB\) articles, update duplicate incident information to the incident record. Attach Known Error \(KE\) articles when the resolution code is a known error. The agentic workflow has the following AI Agents:

    -   Incident resolution details AI agent
    -   Incident knowledge article AI agent
    -   Incident known error article AI agent
-   **[IT Service Management AI agent collection assess conflicts for a change request agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-assess-conflicts-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Autonomously identify conflict types and summarize the impacted schedules, CIs and services related to the change request using the Change conflict assessor AI agent.

-   **[IT Service Management AI agent collection assess quality of a change request agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-assess-quality-change-request-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Assess the quality of a change request and generate suggestions to improve the quality as needed using the Change quality assessor AI agent.

-   **[IT Service Management AI agent collection explain SLA agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-explain-sla-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    View the detailed breakdown of the assignment and ownership relevant to the SLA for an incident, problem, case, or change request using the Explain SLA AI agent.

-   **[IT Service Management AI agent collection schedule a change agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-schedule-change-agentic-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Find and schedule the optimum slots for change requests using the Schedule Change Request AI agent.

-   **[Setting the AI user as the Run as user in the Triage and categorize incidents agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-catincidents-usecase&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Create AI users for the identity type **AI agent** and assign roles to the AI user based on your needs. Run the agentic workflow as the AI user that determines the data access defined by the role.

-   **[Matching flow action access control roles with the agent roles for the Notify users with Twilio agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-twilio-text-usecase&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    When you update the agent role for the Notify users with Twilio agentic workflow, you must also update the corresponding access controls with those roles.

-   **[Matching flow action access control roles with the agent roles for the Manage Microsoft 365 group members agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-O365-groupmembers-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    When you update the agent role for the Manage Microsoft 365 group members agentic workflow, you must also update the corresponding access controls with those roles.

-   **[Using the itil role to add or update work notes in the Now Assist panel](https://www.servicenow.com/docs/access?context=request-gen-ai-capabilities-itsm-now-assist-panel&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    To add or update work notes in the Now Assist panel, the logged-in user must have the itil role.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Zurich Patch 4](../quality/zurich-patch-4.md)[Changing the password reset topic to an AI agent](https://www.servicenow.com/docs/access?context=itsm-va-ai-agents&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    The Virtual Agent **Password reset** topic has been changed to a Virtual Agent AI agent. The agent guides the users with instructions to reset passwords using KB articles in their self-service portal.


## Changed in this release

-   **[Renaming the Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    The Incident assist skill has been renamed to **\[DEPRECATED\] Incident assist**.

-   **[Renaming demo voice AI agents](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    The voice AI demo agents have been renamed as primers.

-   **[Editing change request skills using Now Assist Skill Kit \(NASK\)](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-change-risk-skill&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Easily edit the change request risk explanation and change request summarization skill prompts and inputs directly in the Now Assist Skill Kit \(NASK\).

-   **[Role masking for change risk explanation skill](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-itsm&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Enhance security for the change request risk explanation skill by enabling admins to limit roles that are inherited by the user.


-   **[Skills activated by default in Now Assist for ITSM](https://www.servicenow.com/docs/access?context=using-now-assist-for-itsm&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    For new Now Assist for IT Service Management \(ITSM\) users, the following skills are activated by default:

    -   Resolution notes generation
    -   Knowledge generation
    -   Chat reply recommendation
-   **[Virtual agent topics available as demo data](https://www.servicenow.com/docs/access?context=itsm-va-prebuilt-topics&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    The Virtual Agent topics listed in this table have been renamed and are now available as demo data.

    |Existing name|Updated name|
    |-------------|------------|
    |Add Comment To Incident|\(DEMO\) Add Comment To Incident-LLM|
    |Approve Sysapproval Approver|\(DEMO\) Approve Sysapproval Approver-LLM|
    |Change Password|\(DEMO\) Change Password \(Template\) - LLM|
    |Check IT Ticket Status|\(DEMO\) Check IT Ticket Status \(Template\)|
    |Close Incident|\(DEMO\) Close Incident-LLM|
    |Explain change risk|\(DEMO\) Explain change risk|
    |Mark Incident Unresolved|\(DEMO\) Mark Incident Unresolved-LLM|
    |Open IT Ticket|\(DEMO\) Open IT Ticket \(Template\)-LLM|
    |Reject Sysapproval Approver|\(DEMO\) Reject Sysapproval Approver-LLM|
    |Reset Password|\(DEMO\) Reset Password \(Template\) - LLM|
    |Resolve Incident|\(DEMO\) Resolve Incident-LLM|
    |Unlock Account|\(DEMO\) Unlock Account \(Template\) - LLM|
    |View And Add Comments|\(DEMO\) View And Add Comments-LLM|

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Configuration item details for suggest configuration items for a change request workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-suggest-configuration-items-for-a-change-request&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Provide details such as class, location, and environment to find configuration items \(CIs\) relevant to a change request while using the suggest configuration items for a change request agentic workflow from the Now Assist panel.


-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Skills activated by default in Now Assist for ITSM](https://www.servicenow.com/docs/access?context=using-now-assist-for-itsm&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    For new Now Assist for IT Service Management \(ITSM\) users, the following skills are activated by default:

    -   Incident summarization
    -   Change request summarization
    -   Chat summarization

## Deprecations

The Escalate IT Ticket core ITSM Virtual Agent topic is being deprecated in this release. The topic is renamed to **\(Deprecated\) Escalate IT Ticket**. This capability will be available in the Platform Request Status AI agent in a future release.

## Activation information

Install Now Assist for IT Service Management \(ITSM\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Admin console for quick and effortless access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use this conversational interface in ServiceNow® Service Operations Workspace to summarize a chat, an incident, or resolution notes so that you can get the context of this information more quickly.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the ServiceNow® Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

