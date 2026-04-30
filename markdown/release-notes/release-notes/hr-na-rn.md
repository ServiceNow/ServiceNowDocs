---
title: Now Assist for HR Service Delivery \(HRSD\) release notes
description: The ServiceNow Now Assist for HR Service Delivery \(HRSD\) application brings generative AI to HR Service Delivery. Summarize case and chat information, and generates reply recommendations so that agents can propose quick resolutions. Now Assist for HRSD was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 11
---

# Now Assist for HR Service Delivery \(HRSD\) release notes

The ServiceNow® Now Assist for HR Service Delivery \(HRSD\) application brings generative AI to HR Service Delivery. Summarize case and chat information, and generates reply recommendations so that agents can propose quick resolutions. Now Assist for HRSD was enhanced and updated in the Zurich release.

## Now Assist for HRSD highlights for the Zurich release

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Review an ER interview summary quickly by using the ER interview summarization skill from both Core UI and Agent Workspace for HR Case Management.
-   Streamline the interview scheduling process using the self-scheduling mechanism within the schedule interviews agentic workflow.
-   Preserve institutional knowledge during employee offboarding with AI agents that automate document discovery, organize content by category, and guide managers and employees through the transfer process.
-   View additional journey services \(catalogs and order guides\) recommended based on previous journeys and peer requests.
-   As a manager, review recommendations in Now Assist in Virtual Agent and add new tasks through a conversational interface.
-   As an admin, create reusable feedback templates using the ServiceNow AI Platform Surveys tool.
-   As a manager, select and preview feedback templates when requesting feedback.
-   As a manager, review a summarized view of an employee's recent feedback on the feedback page in Manager Hub.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Use AI voice agents to enable employees to use self-service tools and create HR cases over the phone.
-   Use AI agents to predict the relevant HR service for an HR case and automatically transfer the case to the predicted HR service.
-   Use AI agents to analyze criticality of an HR case and use existing knowledge articles and catalog items for resolving a noncritical case.
-   Use AI agents to assist with processing tuition reimbursement requests based on submitted course information and company policies found in knowledge articles.
-   Leverage AI agents to generate fulfillment plans for critical HR cases from both Core UI and Agent Workspace for HR Case Management.
-   Review ER case context quickly by using the ER case summarization skill from both Core UI and Agent Workspace for HR Case Management.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Implement security in Now Assist AI agents with access control lists \(ACLs\).
-   Use AI agents to place requests to the Human Capital Management \(HCM\) system.
-   Leverage an AI agent to generate a fulfillment plan in a series of steps for an HR case from both Core UI and Agent Workspace for HR Case Management.
-   Leverage AI agents to collect the necessary inputs from recruiters and schedule interviews seamlessly.
-   Simplify employee onboarding with AI agents that gather inputs, structure tasks, enable manager review, and deliver personalized onboarding plans.

Zurich Early Availability

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

See [Now Assist for HR Service Delivery \(HRSD\)](https://www.servicenow.com/docs/access?context=now-assist-hrsd&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

**Important:** Now Assist for HRSD is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   **[Some Now Assist skills are now turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

-   **[ER Interview Summarization](https://www.servicenow.com/docs/access?context=now-assist-hrsd-er-interview&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    Use the ER interview summarization skill to obtain summary of the ER case interview, which includes details such as quick recap, key assertions and responses.

-   **[Self-scheduling option in Schedule interviews agentic workflow](https://www.servicenow.com/docs/access?context=use-ai-agents-to-schedule-interviews&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    Recruiters and recruitment coordinators can now use self-scheduling to streamline interview scheduling by presenting applicants with available time slots to choose from. This option reduces the time to schedule in the absence of overlapping applicant-declared availability and minimizes the probability of manual handover to recruiter. The workflow recommends self-scheduling when beneficial, offers panelist-compatible slots sorted by confidence level, and automatically schedules interviews once applicants select their preferred time.

-   **[Offboarding knowledge transfer plan generation agentic workflow](https://www.servicenow.com/docs/access?context=offboarding-knowledge-x-agentic-wf&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    The offboarding knowledge transfer plan generation agentic workflow captures and organizes critical knowledge when employees leave. AI agents interact with managers to collect requirements, discover documents from the specified time period, categorize content into meaningful work areas, and facilitate employee review before sharing with successors.

-   **[Generate onboarding ramp-up plan](https://www.servicenow.com/docs/access?context=onboarding-ramp-up-plan-agentic-wf&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    The generate onboarding ramp-up plan workflow has been enhanced to create more relevant and personalized ramp-up plans for new hires. The workflow now recommends additional Journey services \(catalogs and order guides\) based on previously completed journeys and services requested by peers in similar roles. Managers can review these recommendations in Now Assist in Virtual Agent and add new services through a conversational experience.

-   **[Streamline feedback collection and review using the Employee feedback collection AI agent](https://www.servicenow.com/docs/access?context=employee-feedback-agent&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    As an admin, create reusable feedback templates using the Platform Surveys tool allowing managers to select and preview templates when requesting feedback, and help them quickly view a summarized snapshot of a reportee’s recent feedback with easy navigation to the feedback page in Manager Hub for detailed insights.


[Zurich Patch 4](../quality/zurich-patch-4.md)

-   **[Predict service and transfer HR cases agentic workflow](https://www.servicenow.com/docs/access?context=predict-transfer-hrcase&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    Analyze an HR case and automatically route it to the most appropriate HR service with the predict service and transfer HR cases agentic workflow.

-   **[Resolve noncritical HR cases agentic workflow](https://www.servicenow.com/docs/access?context=employee-issue-resolver-na&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    Use the resolve noncritical HR cases agentic workflow to assess the criticality of HR cases, and automatically respond to noncritical inquiries without human intervention. Human agent intervention is required when the request is identified as critical.

-   **[Resolve critical HR case agentic workflow](https://www.servicenow.com/docs/access?context=employee-issue-resolve-critical&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    Resolve critical HR requests efficiently with the resolve critical HR case agentic workflow. This workflow generates a tailored fulfillment plan for an HR case using fulfillment instructions, KB articles, or resolution notes of similar past cases. It helps accelerate the resolution process by providing planning support to HR agents.

-   **[Summarize an ER case using Now Assist for HRSD](https://www.servicenow.com/docs/access?context=now-assist-hrsd-summarize-er-case&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    Use the ER case summarization skill to obtain a comprehensive overview of the ER case, which includes key details, such as allegations, evidences, and interviews.

-   **[Help resolve tuition reimbursement requests agentic workflow](https://www.servicenow.com/docs/access?context=resolve-tuition-reimbursement-requests&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    Use the policy based HR evaluator skill to automatically compare employee tuition reimbursement submissions against company policies and return a decision of approval, denial, or request for additional information.

-   **[HR Voice AI agents](https://www.servicenow.com/docs/access?context=now-assist-hrsd-voice-ai-agents&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    Help employees handle self-service HR issues, such as creating cases, checking case status, and requesting time off, using real-time voice interactions with HR AI voice agents. With advanced speech-to-text and text-to-speech capabilities, configurable caller authentication, and seamless integration with Contact Center as a Service \(CCaaS\) providers, such as Twilio and Genesys, the agents can deliver an efficient and personalized experience for employees.


[Zurich Patch 2](../quality/zurich-patch-2.md)

-   **[Collect employee feedback with the help of an agent in Now Assist](https://www.servicenow.com/docs/access?context=employee-feedback-agent&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    As a manager, collect feedback from employees with the help from an agent in Now Assist. Identify which colleagues to request feedback from through Talent Development applications, journeys, and interaction patterns in Microsoft. Send, track, and manage feedback requests with built-in reminders. Leverage existing to-dos to send and manage feedback requests seamlessly.


-   **[Create a growth conversation with the help of an agent in Now Assist](https://www.servicenow.com/docs/access?context=agentic-wf-conversations-na-td&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    As a manager, use the growth conversations preparation AI agent to schedule and prepare for employee growth discussions. The agent provides a clear summary of employee activity and career journey as well as data-driven talking points for focused and impactful conversations.

    **Note:** This feature is available when you have both Now Assist for HR Service Delivery \(HRSD\), which installs Now Assist for Talent and HR Talent AI Agent Collection.


[Zurich Patch 1](../quality/zurich-patch-1.md)

-   **[Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Enable security settings to run AI agents and agentic workflows by using ACLs and user identities. You can configure and manage the ACLs in AI Agent Studio.

-   **[HCM AI agents](https://www.servicenow.com/docs/access?context=conversational-agents&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    Use AI agents to enable employees to place requests to the HCM system, such as apply for time off or update details.

-   **[Resolve HR cases agentic workflow](https://www.servicenow.com/docs/access?context=employee-issue-resolver-na&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    Generate a fulfillment plan in a series of steps for an HR case by selecting the **Generate Plan** button on the HR case. HR agents can add prompts to further refine the AI-generated fulfillment plan before the plan is published to the work notes of the case.

-   **[HR case sentiment analysis](https://www.servicenow.com/docs/access?context=analyze-sentiments-now-assist&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    Prioritize cases by the sentiment score and monitor sentiment trends over time. HR agents can review a brief summary to understand the reasoning for the sentiment score for each HR case.

-   **[Schedule interviews agentic workflow](https://www.servicenow.com/docs/access?context=use-ai-agents-to-schedule-interviews&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    Use AI agents to automate the interview scheduling process from the Now Assist panel and use the inputs from recruiters or recruitment coordinators to send out interview invites.


-   **[Generate onboarding ramp-up agentic workflow](https://www.servicenow.com/docs/access?context=onboarding-ramp-up-plan-agentic-wf&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    Accelerate onboarding with the generate onboarding ramp-up plan agentic workflow, which creates personalized and team-specific plans for every new hire. Powered by AI agents, it tailors learning paths, team tasks, and 1:1 introductions to help employees ramp up fast, build stronger connections, and reach productivity quickly.

-   **[Resolve noncritical HR cases agentic workflow](https://www.servicenow.com/docs/access?context=employee-issue-resolver-na&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    Evaluate case criticality and retrieve relevant knowledge articles to resolve HR cases, minimizing the need for agent intervention. Generate a fulfillment plan for an HR case, which helps resolve the HR case fast.


Zurich Early Availability

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[Use AI agents to create job requisition](https://www.servicenow.com/docs/access?context=use-ai-agents-to-create-job-req&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    Use AI agents to automate the process for creating a job requisition from the Virtual Agent chat window by using the inputs from your hiring managers.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Functional change](https://www.servicenow.com/docs/access?context=employee-issue-resolver-na&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    The resolve HR cases agentic workflow has been broken down into three agentic flows:

    -   [Predict service and transfer HR cases agentic workflow](https://www.servicenow.com/docs/access?context=predict-transfer-hrcase&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)
    -   [Resolve noncritical HR cases agentic workflow](https://www.servicenow.com/docs/access?context=employee-issue-resolver-na&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)
    -   [Resolve critical HR case agentic workflow](https://www.servicenow.com/docs/access?context=employee-issue-resolve-critical&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)

-   **[Flow name](https://www.servicenow.com/docs/access?context=employee-issue-resolver-na&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    The resolve noncritical HR cases workflow has been renamed to the resolve HR cases workflow.


## Activation information

Install Now Assist for HRSD by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Overview tab in Now Assist Admin](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Admin console to provide you with quick and easy access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the conversational interface in CSM Configurable Workspace to summarize a chat, a case, or resolution notes so that you can get the context of this information more quickly.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.

-   **[Agent Workspace for HR Case Management](https://www.servicenow.com/docs/access?context=agent-ws-hr-case-mgmt-landing-page&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    The Agent Workspace for HR Case Management application enables you to interact with employees, respond to inquiries, and resolve issues quickly.

-   **[Journey designer](https://www.servicenow.com/docs/access?context=jny-dsgnr-landing-page&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    The Journey designer application enables managers and employees to create and track journeys. Journeys include transition plans, such as promotions, offboarding, onboarding, and role changes for employees.


**Parent Topic:**[HR Service Delivery release notes](hr-service-delivery-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

