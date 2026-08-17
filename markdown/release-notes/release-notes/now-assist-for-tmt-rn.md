---
title: ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) release notes
description: The ServiceNow ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) application enriches purpose-built industry workflows with generative AI to supercharge insights, actions, and self-service experiences. ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
---

# ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) release notes

The ServiceNow® ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) application enriches purpose-built industry workflows with generative AI to supercharge insights, actions, and self-service experiences. ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) was enhanced and updated in the Zurich release.

## ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) highlights for the Zurich release

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Address voice quality issues and validate tickets with RADCOM.
-   Summarize the risk signal and issues records along with respective risk solution and occurrence records.
-   Additional role configuration required for agentic workflows and AI agents included with your applications.

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   Manage and resolve billing inquiry case requests using a team of AI agents.
-   Analyze network incidents, correlate associated cases, and provide resolutions.
-   Summarize Knowledge Graph service details, success initiatives, internal plays, customer plays, and Zoom meeting details.
-   Analyze account health, trigger renewal flows, schedule, and manage touchpoint meetings.
-   Use agentic AI to quickly create consumer registrations.

See [ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/now-assist-spmc.md) for more information.

**Important:** ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Address voice quality issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/now-assist-customer-voice.md)**

    Collect customer details about the voice quality issue, open a service ticket with RADCOM \([https://radcom.com/](https://radcom.com/)\), and generate a resolution plan.

-   **[Risk signals and issues summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/now-assist-tmt-summarize-risk-signals-issues.md)**

    Generate summary details including the record and associated risk solutions and risk occurrences for risk signal and issues records.


-   **[Help remediate bill issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/billissue-remediation-usecase.md)**

    Handle billing inquiry case requests, analyze customer invoices, and recommend better plans based on customer usage patterns.

-   **[Analyze network incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/network-incident-analysis-usecase.md)**

    Identify historic incidents and determine resolution plans. The AI agent also has the capabilities to identify field values, estimate resolution time, and create actionable tasks.

-   **[Support renewals and expansion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/now-assist-tmt-renewal-analyzer.md)**

    Streamline customer success management by automatically assessing account health, value realization, and adoption trends. Deliver timely, data-driven insights that guide renewal planning and play recommendations.

-   **[Trigger risk mitigation touchpoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/now-assist-tmt-touchpoint-meeting-scheduler.md)**

    Enable customer success agents to optimize meeting schedules within the customer success workflow by creating and managing meetings. Create and manage meetings based on key details such as invitees, agenda, meeting type, and scheduling preferences.

-   **[Success summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/now-assist-tmt-summarize-plays.md)**

    Generate summary details including overview, current status, and open tasks for success initiatives, internal plays, and customer plays. Enhance Zoom meeting summaries by updating key notes, and enabling sentiment tracking.

-   **[Analyze metric data trend](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/now-assist-tmt-analyze-metric-trend.md)**

    Collect and analyze metric data for engagements, identify patterns, and generate a trend chart.

-   **[Service summary generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/now-assist-tmt-summarize-knowledge-graph.md)**

    Generate a service summary for a product inventory.

-   **[Knowledge graph schema generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/now-assist-tmt-create-knowledge-graph.md)**

    Use the Knowledge Graph \(KG\) to create Knowledge Graph schema.

-   **[Customize a summary card for service summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/customize-uib-builder-service-summary.md)**

    Customize the summary card of the service summary and UI actions according to your needs.

-   **[Register consumers using Agentic AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/now-assist-tmt-register-consumer-users-sb.md)**

    Initiate the consumer registration process using agentic AI to receive step-by-step guidance, including error checks during registration and support for resolving those errors.

-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-security-implementation.md)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

    Agentic workflows and AI agents included with your applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. See the documentation for the agentic workflow or AI agent for the specific roles you must add.


## Activation information

Now Assist features are available with activation of the ServiceNow Otto for TMT plugin. For more information, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

## Related ServiceNow applications and features

-   **[AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-now-assist.md)**

    The AI Admin Hub console provides you with quick and effortless access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Use this conversational interface in CSM Configurable Workspace to summarize a chat, a case, or resolution notes so that you can get the context of this information more quickly.

-   **[Generative AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills.md)**

    Use the Now Assist products to provide agentic AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)

**Parent Topic:**[Telecommunications, Media, and Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/technology-industry-rn-landing.md)

