---
title: Now Assist for Security Incident Response release notes
description: The ServiceNow Now Assist for Security Incident Response application can help your security analysts resolve security incidents autonomously with intelligent workflows and generative AI skills. Now Assist for Security Incident Response was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2026-01-30"
reading_time_minutes: 9
---

# Now Assist for Security Incident Response release notes

The ServiceNow® Now Assist for Security Incident Response application can help your security analysts resolve security incidents autonomously with intelligent workflows and generative AI skills. Now Assist for Security Incident Response was enhanced and updated in the Yokohama release.

## Now Assist for Security Incident Response highlights for the Yokohama release

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Use generative AI to create a quality assessment report of a security incident.

-   Yokohama Patch 6

    Help analysts to add security incidents details to the Shift Handover report by chatting with AI agents in the Now Assist panel.

    -   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Yokohama Patch 3

    Help your analysts to gain insight into security incident record metrics with an agentic workflow. Chat with AI agents in natural language from the Now Assist panel.

    Help your analysts to resolve security incidents by chatting with AI agents in the Now Assist panel where the AI agent provides a resolution plan.

-   Yokohama Patch 1

    Help your analysts to close security incidents more efficiently by chatting with AI agents in natural language from the Now Assist panel.

-   Yokohama early availability

    -   Triage security incidents with long activity streams by reviewing work notes and contextual information quickly in a concise, easy-to-read format.
    -   Automatically generate resolution notes for security incidents by using generative AI.
    -   Generate recommended actions to resolve security incidents.
    -   Generate a post-incident analysis.
    -   Generate correlation insights to help you connect current incidents to past events. By identifying the affected users, configuration items \(CIs\), or observables \(IP addresses and file hashes\) from existing incidents, you can help to triage new security incidents.
    For more information, see [Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=now-assist-security-incident-landing&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US).


**Important:** Now Assist for Security Incident Response is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Now Assist for Security Incident Response to Yokohama

For more information about required applications for Now Assist for Security Incident Response, see [Supporting information for Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-security-incident&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US).

**Note:**

Upgrading the Now Assist plugins activate any designated skills that were previously untouched by the customer.

-   If you have the plugins installed but never touched the configuration \(never activated the skill nor adjusted associated roles\) of a skill, any Default On skill will be activated on a per skill basis upon upgrading.
-   If you have previously toggled a skill from active and then back to inactive or have updated any roles for that skill, that skill remains inactive upon upgrading.
-   You maintain full control over deactivating individual skills at any time after activation.

Starting with version 2.0.1, the name of the Now Assist for Security Operations application in ServiceNow® Store and in your ServiceNow AI Platform® instance has changed to Now Assist for Security Incident Response. You must upgrade to version 2.0.1 to access the following features:

-   Generate resolution notes in the Now Assist context menu.
-   Generate correlation insights for a security incident investigation from the Now Assist panel.

The AI Search application must be enabled so that the recommended actions skill works for security incidents. To verify that AI Search is enabled on your instance, navigate to **All** &gt; **AI Search** &gt; **AI Search Status**. Contact support if the page indicates that AI Search is not enabled.

## New in the Yokohama release

-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add.

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Generate a quality assessment report](https://www.servicenow.com/docs/access?context=na-sir-quality-assessment&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Use generative AI to create a quality assessment report of a security incident. The reports are generated using a predefined, natural language rule set. The report provides an overall assessment summary followed by the detailed assessment for all the rules.


-   **[Generate SIR Shift Handover Report](https://www.servicenow.com/docs/access?context=add-incidents-shifthandover-ai-agent&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    The AI Agent helps add security incident details to a shift handover report. The agent populates the different sections of the shift handover with appropriate content by identifying the relevant details from the security incident. The AI agent can fetch details of the security incident and identify if the analyst has access to the shift handover record. The AI agent can generate content for each section of the shift handover record and asks for analysts feedback on the content. The AI agent refines the content based on the feedback and saves the content to the records on approval.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


-   **[Using AI agentic workflows in Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=using-now-assist-ai-agents-sir&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    The Analyze security operations metrics agentic workflow enables security managers to analyze their teams' performance.

    -   Generate metrics for Security Incident Response \(SIR\) records for case volume, mean time to assign \(MTTA\), and mean time to resolve \(MTTR\) for a date range of your choosing.
    -   Request suggestions for how to improve MTTR, MTTA, and volume based on your metrics.
-   **[Enhancements to correlation insights in Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=generating-insights-for-now-assist-for-security&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    You can generate and view results for correlation insights in the Security Incident Response Workspace.

    -   Correlation insights are not limited to the primary configuration item \(CI\) or affected users associated with a security incident. You can base your correlation insights on any CI or affected user for a security incident.
    -   You can generate correlation insights from the **Investigation** tab for a security incident in any state in the Security Incident Response Workspace.
    -   You can generate insights for multiple items simultaneously for Associated Observables, Configuration items, and Affected Users.
    -   Results are displayed in a modeless dialog that you can size and move.
-   **[Using Security incident resolution agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-sir-resolve-incident-ai-workflow&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Use the Security incident resolution agentic workflow to close your security incidents. Analysts can chat with the AI agents in natural language to resolve the security incidents. The AI agent analyzes the incident details, existing runbooks, knowledge articles, and past similar security incidents as inputs, and provides a resolution plan. The AI agent also assists the analysts to resolve the security incident.


-   **[Using Security Incident Response AI agents](https://www.servicenow.com/docs/access?context=using-now-assist-ai-agents-sir&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Yokohama Patch 1: Use the Close security incident use case to close your security incidents:

    -   Analysts can chat with the AI agents in natural language to close the security incidents. The AI agent can cancel the associated response tasks, generate resolution notes, close code, or close notes and post incident analysis \(PIA\) during incident closure. Analysts can provide feedback on the content and the AI agent can refine the content​ based on the feedback.
    -   Analysts can also close false positive security incidents with minimal user intervention.
-   **[Yokohama Early Availability](https://www.servicenow.com/docs/access?context=now-assist-security-incident-landing&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**
    -   [Generate correlation insights](https://www.servicenow.com/docs/access?context=generate-correlation-insights-now-assist-for-security&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)

        Generate correlation insights to connect current security incidents to past events. You can identify the affected users, configuration items \(CI\)s, or observables \(IP addresses and file hashes\) from existing incidents and records to help you more quickly triage your new security incidents. Correlation insights are supported in Workspace, the Core UI, and from the Now Assist panel.

    -   Enhancements to [closure \(resolution\) notes](https://www.servicenow.com/docs/access?context=generate-closure-notes-si-now-assist-sec-incident&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) and [post incident analysis](https://www.servicenow.com/docs/access?context=generate-pia-report-now-assist-security-incident&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) generation

        Generate resolution notes from the Close the security incident modal or the Now Assist context menu on a security incident record \(SIR\). You can also generate resolution notes from the Now Assist panel. If you choose the Now Assist context menu, you have the following options to help you refine the generated text:

        -   **Shorten**: Select the text to remove details.
        -   **Elaborate**: Generate more details about the context of a security incident.
        **Note:** Generating resolution notes is supported in Workspace and Core UI. Generating a post incident analysis is supported from the Close the security incident modal in Workspace.


## UI changes

Yokohama Patch 3

-   **[Generate recommended actions for a security incident with Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=generate-recommended-actions-now-assist-for-security&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Introduced a new UI card **Show More** to enhance the visibility of recommended actions. As a security analyst, you can now access additional context along with further recommended steps to assist in the analysis and investigation of security incidents.


-   **[Now Assist for Security Incident Response application name change](https://www.servicenow.com/docs/access?context=activate-skills-for-now-assist-security-incident&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Starting with version 2.0.1, the Now Assist for Security Operations application in the ServiceNow® Store and in your ServiceNow AI Platform® instance has changed to the Now Assist for Security Incident Response application.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are now turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The following Now Assist skills for Now Assist for Security Incident Response and Now Assist for Vulnerability Response are activated by default.

    -   Security incident summarization \(SIR\)
    -   Resolution notes generation \(SIR\)
    -   Post incident analysis \(SIR\)
    -   Security incident recommended actions \(SIR\)
    -   Correlation insights generation \(SIR\)
    -   Security incident quality assessment \(SIR\)
    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


## Activation information

Install Now Assist for Security Incident Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

**Parent Topic:**[Security Operations release notes](security-operations-rn-landing.md)

