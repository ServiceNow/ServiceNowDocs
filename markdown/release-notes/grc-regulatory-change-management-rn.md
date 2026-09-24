---
title: Regulatory Change Management release notes
description: The ServiceNow Regulatory Change Management application enables you to check upcoming regulatory changes, assess their impact, and implement risk and compliance-related changes. Regulatory Change Management was enhanced and updated in the Brazil release.Regulatory Change Management version 23.0.3 extends AI alert summarization to every state, adds AI Data Explorer to widgets on the RCM home page, traces regulatory action tasks to their impacted area records, and offers filters to scope entity selection when initiating risk assessments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/grc-regulatory-change-management-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [regulatory change management, ai data explorer, risk assessment, action tasks, alert summarization]
breadcrumb: [Governance, Risk, and Compliance release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Regulatory Change Management release notes

The ServiceNow® Regulatory Change Management application enables you to check upcoming regulatory changes, assess their impact, and implement risk and compliance-related changes. Regulatory Change Management was enhanced and updated in the Brazil release.

## About Regulatory Change Management

-   Identify and triage regulatory alerts from third-party providers or RSS feeds.
-   Map incoming regulatory content to your organization's internal regulatory taxonomy.
-   Assess the impact of a regulatory change and the inherent legal, reputational, financial, and business risk on an entity.
-   Create and track action tasks to implement a regulatory change.
-   Streamline regulatory alert analysis, summarization, and impact assessment with ServiceNow Otto skills and agentic workflows in Regulatory Change Management.

See [Regulatory Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/reg-change-mgmt-landing-page.md) for more information.

## Activation and other requirements

**Note:** Regulatory Change Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Regulatory Change Management and ServiceNow Otto for IRM by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/grc-rn-landing.md)

## Version 23.0.3

Regulatory Change Management version 23.0.3 extends AI alert summarization to every state, adds AI Data Explorer to widgets on the RCM home page, traces regulatory action tasks to their impacted area records, and offers filters to scope entity selection when initiating risk assessments.

### What's changed

-   **[Entity filtering in the risk assessment modal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/impact-assessment-tasks.md)**

    When you initiate a risk assessment from a regulatory alert, the Evaluate risk impact dialog box includes a **Filter by** drop-down. Use **Entities by Impacted Areas** or **Entities by Recommendations** to scope your entity selection.

-   **[Regulatory alert summarization in all regulatory alert states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/regulatory-alert-summarization.md)**

    Generate a regulatory alert summary in any state. The AI-generated summary includes new sections such as alert overview, scope, actions and outcomes, and velocity analysis. Select **Share to alert summary** to save the summary to the alert record.

-   **[Enhanced input data for regulatory alert summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/input-data-rcm-skill.md)**

    The regulatory alert summarization skill uses additional input data to generate a summary. New input fields include enriched insights, coordinator details, functional domain, and alert type, among others. The skill also incorporates data from the impacted areas and regulatory change tasks related lists.

-   **[Regulatory alert number on the Details tab of an alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/reg-feed-overview-in-ws.md)**

    The regulatory alert number is displayed on the Details tab of a regulatory alert.

-   **[New column on regulatory assessment tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/respond-to-a-regulatory-assessment.md)**

    The Regulatory assessments tab in **GRC Tasks** displays the regulatory alert for an assessment in the Record column.

-   **[Compliance library items traced to their corresponding regulatory action tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/action-tasks.md)**

    Compliance library records, including citations, control objectives, controls, and policies, feature a Regulatory action tasks tab that links the action tasks linked to these records. This enables you to navigate from the impacted area record in the compliance library directly to its action task in RCM. Similarly, from the Action tasks tab of a regulatory alert, you can navigate to the impacted citations, control objectives, controls, or policies.

-   **[Email notification redirection to workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/email-notifications-in-rcm.md)**

    Email notification links for RCM records redirect users to the Compliance Workspace instead of the classic environment.


### What's deprecated or removed

-   **Now LLM service deprecation**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


### Plugin information

-   **New plugins**

    AI Data Explorer \(sn\_pa\_ai\_canvas\): Install the plugin to enable regulatory change managers and users to analyze regulatory data using natural language queries. On the Regulatory Change Management dashboard of the Compliance Workspace, select the Explore with AI icon \[Omitted image "icon-otto-outline-24.svg"\] on the widgets to open AI Data Explorer and gather insights about underlying regulatory data. For information on installing, configuring and using it, see [Use AI to explore data with AI Data Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/ai-data-explorer.md).


