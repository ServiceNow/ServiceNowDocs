---
title: ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) release notes
description: The ServiceNow ServiceNow Otto for TMT application enriches purpose-built industry workflows with generative AI to supercharge insights, actions, and self-service experiences. ServiceNow Otto for TMT was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
---

# ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) release notes

The ServiceNow® ServiceNow Otto for TMT application enriches purpose-built industry workflows with generative AI to supercharge insights, actions, and self-service experiences. ServiceNow Otto for TMT was enhanced and updated in the Yokohama release.

## ServiceNow Otto for TMT highlights for the Yokohama release

[Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Address voice quality issues and validate tickets with RADCOM.
-   Summarize the risk signal and issues records along with respective risk solution and occurrence records.

Yokohama Patch 6

-   Manage and resolve billing inquiry case requests using a team of AI agents.
-   Analyze network incidents, correlate associated cases, and provide resolutions.
-   Summarize Knowledge Graph service details, success initiatives, internal plays, customer plays, and Zoom meeting details.
-   Analyze account health, trigger renewal flows, schedule, and manage touchpoint meetings.
-   Use agentic AI to quickly create consumer registrations.

Yokohama Patch 3

-   Monitor engagement health score and provide a trend analysis.
-   Monitor risks on a predefined schedule and provide common resolutions.

Yokohama Patch 1

-   Proactively identify service problems, diagnose, test, and resolve customer issues autonomously using the ServiceNow Otto for TMT AI agent collection.

Yokohama Early Availability

-   Summarize onboarding cases, engagements, and touchpoints by using agentic AI.
-   Enhance test summarization with metric descriptions and contextual notes.
-   Consolidate the information from multiple similar cases into a Knowledge article.
-   Dynamically configure prompts for case summarization.
-   Automate transformation mapping between provider and consumer instances in Service Exchange.

See [ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-spmc.md) for more information.

**Important:** ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Address voice quality issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-customer-voice.md)**

    Collect customer details about the voice quality issue, open a service ticket with RADCOM \([https://radcom.com/](https://radcom.com/)\), and generate a resolution plan.

-   **[Risk signals and issues summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-summarize-risk-signals-issues.md)**

    Generate summary details including the record and associated risk solutions and risk occurrences for risk signal and issues records.


-   **[Help remediate bill issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/billissue-remediation-usecase.md)**

    Handle billing inquiry case requests, analyze customer invoices, and recommend better plans based on customer usage patterns.

-   **[Analyze network incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/network-incident-analysis-usecase.md)**

    Identify historic incidents and determine resolution plans. The AI agent also has the capabilities to identify field values, estimate resolution time, and create actionable tasks.

-   **[Support renewals and expansion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-renewal-analyzer.md)**

    Streamline customer success management by automatically assessing account health, value realization, and adoption trends. Deliver timely, data-driven insights that guide renewal planning and play recommendations.

-   **[Trigger risk mitigation touchpoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-touchpoint-meeting-scheduler.md)**

    Enable customer success agents to optimize meeting schedules within the customer success workflow by creating and managing meetings. Create and manage meetings based on key details such as invitees, agenda, meeting type, and scheduling preferences.

-   **[Success summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-summarize-plays.md)**

    Generate summary details including overview, current status, and open tasks for success initiatives, internal plays, and customer plays. Enhance Zoom meeting summaries by updating key notes, and enabling sentiment tracking.

-   **[Analyze metric data trend](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-analyze-metric-trend.md)**

    Collect and analyze metric data for engagements, identify patterns, and generate a trend chart.

-   **[Service summary generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-summarize-knowledge-graph.md)**

    Generate a service summary for a product inventory.

-   **[Knowledge graph schema generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-create-knowledge-graph.md)**

    Use the Knowledge Graph \(KG\) to create Knowledge Graph schema.

-   **[Customize a summary card for service summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/customize-uib-builder-service-summary.md)**

    Customize the summary card of the service summary and UI actions according to your needs.

-   **[Register consumers using Agentic AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-register-consumer-users-sb.md)**

    Initiate the consumer registration process using agentic AI to receive step-by-step guidance, including error checks during registration and support for resolving those errors.

-   **Configure ACLs for AI agents and agentic workflows**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **[Monitor engagement health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-resolve-risk.md)**

    Monitor the health score of all engagements, create trend charts, and generate risk signals when a decline is detected.

-   **[Analyze risk signals and recommend solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-monitor-health.md)**

    Retrieve unaddressed risk signals and identify appropriate success plays based on a back-end decision table.


-   **[Using Telecommunications, Media, and Technology AI agent collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/using-aiagents-usecases.md)**

    Use ServiceNow Otto for TMT AI agents to troubleshoot and autonomously resolve customer issues.

    |AI agent agentic workflow|Description|
    |-------------------------|-----------|
    |Test and repair telecom service issues|Use AI agents to handle task requests that require troubleshooting, diagnosis, and resolution of a case task.|


-   **[Dynamic prompt configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-customize.md)**

    Use the ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) application to provide concise, context-driven summaries that are specific to each case. Your agents can ensure that critical case details are captured and can provide personalized and informed resolutions.

-   **[Enhanced test summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-summarize-test.md)**

    Use AI-generated test summaries that include the metric descriptions and contextual notes from cases. Your agents can focus on high-priority issues and make better informed decisions that enhance the product quality and performance.

-   **[Resolution notes generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-generate-resolution.md)**

    Generate resolution notes and then shorten or elaborate the content by using the Now Assist context menu in the resolution notes field of the case form in both the Core UI and Workspace.

-   **[Knowledge article generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-generate-knowledge-article.md)**

    Select and gather insights and data from multiple similar cases to create an article by using ServiceNow Otto for TMT. Use the Now Assist icon \(\[Omitted image "icon-ai-sparkle.png"\] Alt text: Now Assist icon.\), which is accessible as an inline capability to create and refine Knowledge articles.

-   **[Account onboarding case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-summarize-onboard-case.md)**

    Generate a concise account onboarding case summary that enables your agents to get a quick overview of the case details.

-   **[Engagement summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-summarize-engagement.md)**

    Generate a high-level summary with a list of the key items about an engagement.

-   **[Touchpoint summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-summarize-touchpoint.md)**

    Generate a quick summary of the various touchpoints in the engagement life cycle. Your agents can get a quick summary of all meetings and emails exchanged between the different stakeholders and any follow-up activities.

-   **[Transform mapping assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-tmt-generate-transform-maps.md)**

    While using the Service Exchange for a provider's application, use the Transform Mapping Assist feature to generate transform mappings between provider and consumer tables automatically. This skill enables you to streamline the transformation mapping process by reducing errors and improving overall efficiency.


## Changed in this release

-   **Changes to Now Assist usage measurement**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **Some Now Assist skills are turned on by default**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **Configure ACLs for AI agents and agentic workflows**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


## Activation information

Now Assist features are available with activation of the ServiceNow Otto for TMT plugin. For more information, see .

## Related ServiceNow applications and features

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   ****

    Use the AI Admin Hub console to provide you with quick and effortless access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   ****

    Use this conversational interface in CSM Configurable Workspace to summarize a chat, a case, or resolution notes so that you can get the context of this information more quickly.

-   ****

    Use the Now Assist products to provide agentic AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-assist-rn-landing.md)

**Parent Topic:**[Telecommunications, Media, and Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/technology-industry-rn-landing.md)

