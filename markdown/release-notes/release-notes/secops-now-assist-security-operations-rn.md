---
title: Now Assist for Security Incident Response \(SIR\) release notes
description: The ServiceNow Now Assist for Security Incident Response application helps your security analysts resolve security incidents autonomously with intelligent workflows and generative AI skills. Now Assist for Security Incident Response was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-01-28"
reading_time_minutes: 7
---

# Now Assist for Security Incident Response \(SIR\)release notes

The ServiceNow® Now Assist for Security Incident Response application helps your security analysts resolve security incidents autonomously with intelligent workflows and generative AI skills. Now Assist for Security Incident Response was enhanced and updated in the Zurich release.

## Now Assist for Security Incident Response highlights for the Zurich release

[Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)

-   Help enhance incident resolution plan generation by adding your existing runbooks to the AI runbooks section within the Security incident resolution plan skill. The existing runbooks provide additional context to the skill.
-   Use the Sightings search and Isolate host capabilities in the Resolve security incident workflow to help resolve security incidents.

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Some Now Assist skills are now turned on by default.
-   Use generative AI to create a quality assessment report of a security incident.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   Help analysts to add security incidents details to the Shift Handover report by chatting with AI agents in the Now Assist panel.

Zurich Early Availability

-   Help your analysts to gain insight into security incident record metrics with an agentic workflow. Chat with AI agents in natural language from the Now Assist panel.
-   Help your analysts to resolve security incidents by chatting with AI agents in the Now Assist panel where the AI agent can assist in providing a resolution plan.

**Important:** Now Assist for Security Incident Response is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Now Assist for Security Incident Response to Zurich

**Note:** The following Now Assist skills, agents, and agentic workflows for Now Assist for Security Incident Response are activated by default:

Skills

-   Security incident summarization
-   Resolution notes generation
-   Post incident analysis
-   Security incident recommended actions
-   Correlation insights generation
-   Security incident quality assessment
-   Natural language condition evaluator
-   Generate content for shift handover
-   Quality assessment report NACM
-   Security incident resolution plan
-   Security operations metrics analysis

Agentic workflows

-   Wrap up security incident
-   Resolve security incident
-   Generate SIR shift handover report
-   Analyze security operations metrics

Agents

-   EDR AI agent
-   Exchange online integration handling AI agent
-   Observable analysis AI agent
-   Security incident activities handling AI agent
-   Security incident resolution AI agent
-   Security incident retrieval AI agent
-   Security incident shift handover AI agent
-   Security incident wrap up generator AI agent
-   Security metrics analysis AI agent

For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)

**Note:** Upgrading the Now Assist plugins activates any designated skills that were previously untouched by the customer.

-   If you installed the plugins for a skill but never configured it, meaning you never activated it nor adjusted associated roles, any skill on by default is activated on a per skill basis when upgrade.
-   If you previously toggled a skill from active and then back to inactive, or updated any roles for that skill, that skill remains inactive when upgrading.
-   You maintain full control over deactivating individual skills at any time after activation.

When you update the Now Assist for Security Incident Response \(SIR\) application, the dependency applications are automatically updated.

For more information about required applications for Now Assist for Security Incident Response, see [Supporting information for Now Assist for Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/supporting-information-now-assist-security-incident.md).

The AI Search application must be enabled so that the recommended actions skill works for security incidents with Now Assist for Security Incident Response. To verify that AI Search is enabled on your instance, navigate to **All** &gt; **AI Search** &gt; **AI Search Status**. Contact support if the page indicates that AI Search isn’t enabled.

## New in the Zurich release

-   **[Resolve a security incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-sir-resolve-incident-ai-workflow.md)**

    Help enhance incident resolution plan generation by adding your existing runbooks to the AI runbooks section within the Security incident resolution plan skill. The existing runbooks provide additional context to the skill.


-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

    Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.

-   **[Exploring Security incident quality assessment with Now Assist for Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/na-sir-quality-assessment.md)**

    Use generative AI to create a quality assessment report of a security incident. The reports are generated using a predefined, natural language rule set. The report provides an overall assessment summary followed by the detailed assessment for all the rules.


-   **[Generate SIR Shift Handover Report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/add-incidents-shifthandover-ai-agent.md)**

    The AI agent helps add security incident details to a shift handover report. The agent populates the different sections of the shift handover with appropriate content by identifying the relevant details from the security incident. The AI agent can fetch details of the security incident and identify if the analyst has access to the shift handover record. The AI agent can generate content for each section of the shift handover record and asks for analysts feedback on the content. The AI agent refines the content based on the feedback and saves the content to the records on approval.


-   **[Using agentic AI workflows in Now Assist for Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/using-now-assist-ai-agents-sir.md)**

    The analyze security operations metrics agentic workflow helps security managers to analyze their teams' performance.

    -   Generate metrics for Security Incident Response \(SIR\) records for case volume, mean time to assign \(MTTA\), and mean time to resolve \(MTTR\) for a date range of your choosing.
    -   Request suggestions for how to improve MTTR, MTTA, and volume based on your metrics.
-   **[Enhancements to correlation insights in Now Assist for Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/generating-insights-for-now-assist-for-security.md)**

    You can generate and view results for correlation insights in the Security Incident Response Workspace.

    -   Correlation insights aren’t limited to the primary configuration item \(CI\) or affected users associated with a security incident. You can base your correlation insights on any CI or affected user for a security incident.
    -   You can generate correlation insights from the **Investigation** tab for a security incident in any state in the Security Incident Response Workspace.
    -   You can generate insights for multiple items simultaneously for Associated Observables, Configuration items, and Affected Users.
    -   Results are displayed in a modeless dialog that you can size and move.
-   **[Using the security incident resolution agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-sir-resolve-incident-ai-workflow.md)**

    Use the security incident resolution agentic workflow to close your security incidents. Analysts can chat with AI agents in natural language to resolve the security incidents. The AI agent analyzes the incident details, existing runbooks, Knowledge articles, and past similar security incidents as inputs, and provides a resolution plan. The AI agent also assists the analysts to resolve the security incident.


## UI changes

-   **[Generate recommended actions for a security incident with Now Assist for Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/generate-recommended-actions-now-assist-for-security.md)**

    A new **Show More** UI card has been introduced to enhance the visibility of recommended actions. As a security analyst, you can now access additional context along with further recommended steps to assist in the analysis and investigation of security incidents.


## Changed in this release

-   **[Resolve a security incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-sir-resolve-incident-ai-workflow.md)**

    Use the Sightings search and Isolate host capabilities in the Resolve security incident workflow to help resolve security incidents.


## Activation information

Install Now Assist for Security Incident Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)

**Parent Topic:**[Security Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/security-operations-rn-landing.md)

