---
title: Now Assist for Telecommunications, Media and Technology \(TMT\) release notes
description: The ServiceNow Now Assist for TMT application enriches purpose-built industry workflows with generative AI to supercharge insights, actions, and self-service experiences. Now Assist for TMT was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
---

# Now Assist for Telecommunications, Media and Technology \(TMT\) release notes

The ServiceNow® Now Assist for TMT application enriches purpose-built industry workflows with generative AI to supercharge insights, actions, and self-service experiences. Now Assist for TMT was enhanced and updated in the Yokohama release.

## Now Assist for TMT highlights for the Yokohama release

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

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

-   Proactively identify service problems, diagnose, test, and resolve customer issues autonomously using the Now Assist for TMT AI agent collection.

Yokohama Early Availability

-   Summarize onboarding cases, engagements, and touchpoints by using agentic AI.
-   Enhance test summarization with metric descriptions and contextual notes.
-   Consolidate the information from multiple similar cases into a Knowledge article.
-   Dynamically configure prompts for case summarization.
-   Automate transformation mapping between provider and consumer instances in Service Exchange.

See [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://www.servicenow.com/docs/access?context=now-assist-spmc&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US) for more information.

**Important:** Now Assist for Telecommunications, Media and Technology \(TMT\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Address voice quality issues](https://www.servicenow.com/docs/access?context=now-assist-customer-voice&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    Collect customer details about the voice quality issue, open a service ticket with RADCOM \([https://radcom.com/](https://radcom.com/)\), and generate a resolution plan.

-   **[Risk signals and issues summarization](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-risk-signals-issues&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    Generate summary details including the record and associated risk solutions and risk occurrences for risk signal and issues records.


-   **[Help remediate bill issues](https://www.servicenow.com/docs/access?context=billissue-remediation-usecase&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    Handle billing inquiry case requests, analyze customer invoices, and recommend better plans based on customer usage patterns.

-   **[Analyze network incidents](https://www.servicenow.com/docs/access?context=network-incident-analysis-usecase&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    Identify historic incidents and determine resolution plans. The AI agent also has the capabilities to identify field values, estimate resolution time, and create actionable tasks.

-   **[Support renewals and expansion](https://www.servicenow.com/docs/access?context=now-assist-tmt-renewal-analyzer&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    Streamline customer success management by automatically assessing account health, value realization, and adoption trends. Deliver timely, data-driven insights that guide renewal planning and play recommendations.

-   **[Trigger risk mitigation touchpoint](https://www.servicenow.com/docs/access?context=now-assist-tmt-touchpoint-meeting-scheduler&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    Enable customer success agents to optimize meeting schedules within the customer success workflow by creating and managing meetings. Create and manage meetings based on key details such as invitees, agenda, meeting type, and scheduling preferences.

-   **[Success summarization](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-plays&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    Generate summary details including overview, current status, and open tasks for success initiatives, internal plays, and customer plays. Enhance Zoom meeting summaries by updating key notes, and enabling sentiment tracking.

-   **[Analyze metric data trend](https://www.servicenow.com/docs/access?context=now-assist-tmt-analyze-metric-trend&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    Collect and analyze metric data for engagements, identify patterns, and generate a trend chart.

-   **[Service summary generation](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-knowledge-graph&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    Generate a service summary for a product inventory.

-   **[Knowledge graph schema generation](https://www.servicenow.com/docs/access?context=now-assist-tmt-create-knowledge-graph&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    Use the Knowledge Graph \(KG\) to create Knowledge Graph schema.

-   **[Customize a summary card for service summary](https://www.servicenow.com/docs/access?context=customize-uib-builder-service-summary&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    Customize the summary card of the service summary and UI actions according to your needs.

-   **[Register consumers using Agentic AI](https://www.servicenow.com/docs/access?context=now-assist-tmt-register-consumer-users-sb&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    Initiate the consumer registration process using agentic AI to receive step-by-step guidance, including error checks during registration and support for resolving those errors.

-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **[Monitor engagement health](https://www.servicenow.com/docs/access?context=now-assist-tmt-resolve-risk&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    Monitor the health score of all engagements, create trend charts, and generate risk signals when a decline is detected.

-   **[Analyze risk signals and recommend solutions](https://www.servicenow.com/docs/access?context=now-assist-tmt-monitor-health&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    Retrieve unaddressed risk signals and identify appropriate success plays based on a back-end decision table.


-   **[Using Telecommunications, Media, and Technology AI agent collection](https://www.servicenow.com/docs/access?context=using-aiagents-usecases&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    Use Now Assist for TMT AI agents to troubleshoot and autonomously resolve customer issues.

    |AI agent agentic workflow|Description|
    |-------------------------|-----------|
    |Test and repair telecom service issues|Use AI agents to handle task requests that require troubleshooting, diagnosis, and resolution of a case task.|


-   **[Dynamic prompt configuration](https://www.servicenow.com/docs/access?context=now-assist-tmt-customize&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    Use the Now Assist for Telecommunications, Media and Technology \(TMT\) application to provide concise, context-driven summaries that are specific to each case. Your agents can ensure that critical case details are captured and can provide personalized and informed resolutions.

-   **[Enhanced test summarization](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-test&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    Use AI-generated test summaries that include the metric descriptions and contextual notes from cases. Your agents can focus on high-priority issues and make better informed decisions that enhance the product quality and performance.

-   **[Resolution notes generation](https://www.servicenow.com/docs/access?context=now-assist-tmt-generate-resolution&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    Generate resolution notes and then shorten or elaborate the content by using the Now Assist context menu in the resolution notes field of the case form in both the Core UI and Workspace.

-   **[Knowledge article generation](https://www.servicenow.com/docs/access?context=now-assist-tmt-generate-knowledge-article&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    Select and gather insights and data from multiple similar cases to create an article by using Now Assist for TMT. Use the Now Assist icon \(![Now Assist icon.](../../common/image/icon-ai-sparkle.png)\), which is accessible as an inline capability to create and refine Knowledge articles.

-   **[Account onboarding case summarization](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-onboard-case&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    Generate a concise account onboarding case summary that enables your agents to get a quick overview of the case details.

-   **[Engagement summarization](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-engagement&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    Generate a high-level summary with a list of the key items about an engagement.

-   **[Touchpoint summarization](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-touchpoint&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    Generate a quick summary of the various touchpoints in the engagement life cycle. Your agents can get a quick summary of all meetings and emails exchanged between the different stakeholders and any follow-up activities.

-   **[Transform mapping assist](https://www.servicenow.com/docs/access?context=now-assist-tmt-generate-transform-maps&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)**

    While using the Service Exchange for a provider's application, use the Transform Mapping Assist feature to generate transform mappings between provider and consumer tables automatically. This skill enables you to streamline the transformation mapping process by reducing errors and improving overall efficiency.


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

Now Assist features are available with activation of the Now Assist for TMT plugin. For more information, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Admin console to provide you with quick and effortless access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use this conversational interface in CSM Configurable Workspace to summarize a chat, a case, or resolution notes so that you can get the context of this information more quickly.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist products to provide agentic AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

**Parent Topic:**[Telecommunications, Media, and Technology release notes](technology-industry-rn-landing.md)

