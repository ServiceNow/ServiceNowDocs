---
title: Enterprise Architecture release notes
description: The ServiceNow Enterprise Architecture application unites strategic and operational teams, enabling organizations to achieve their business objectives. See the following sections for release notes by version.This release makes MCP for Enterprise Architecture generally available and extends the query agent to infrastructure impact analysis. You can also associate AI systems with business applications independently of Enterprise Architecture Workspace.This release adds configurable technical debt criteria, persistent technical debt states, and domain separation for AI Control Tower integration. It also enhances Technology Reference Model \(TRM\) product and lifecycle request workflows in the Enterprise Architecture Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/enterprise-architecture-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 7
keywords: [enterprise architecture, application portfolio management, EA workspace, business capabilities, technology portfolio, MCP for Enterprise Architecture, Enterprise Architecture for AICT, AI Control Tower, business application insights, infrastructure impact analysis, technical debt, technical debt, AI Control Tower, domain separation, TRM product request, Business Planner]
breadcrumb: [Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Enterprise Architecture release notes

The ServiceNow® Enterprise Architecture application unites strategic and operational teams, enabling organizations to achieve their business objectives. See the following sections for release notes by version.

## About Enterprise Architecture

-   Unite strategic and operational teams around a single enterprise architecture practice for managing business capabilities, application portfolios, information portfolios, and technology portfolios.
-   Decide whether to invest in, sustain, or replace business applications based on business need and organizational goals, using indicators such as cost, risk, value, and technical debt.
-   Model, visualize, and analyze your architecture using industry-aligned standards such as CSDM, ArchiMate, and AWS, and explore relationships and dependencies using Architecture Analyzer.
-   Work from a single Enterprise Architecture Workspace home page with role-based views for enterprise architects, administrators, and analysts, including portfolio insights, tasks that need your attention, and portfolio health.
-   Ensure the accuracy, completeness, and reliability of enterprise architecture data with configurable Data Certification policies.

See [Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/ea-workspace.md) for more information.

## Activation and other requirements

-   **Activation information**

    Enterprise Architecture is available with activation of the Enterprise Architecture \(com.snc.apm\) plugin, which requires a separate subscription.

-   **Additional requirements**

    ServiceNow Otto features are available with activation of the ServiceNow Otto for Enterprise Architecture \(EA\) plugin. For more information, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).


**Parent Topic:**[Features and changes by product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/new-features-changes.md)

## Brazil Patch 1

This release makes MCP for Enterprise Architecture generally available and extends the query agent to infrastructure impact analysis. You can also associate AI systems with business applications independently of Enterprise Architecture Workspace.

### What's new

-   **[MCP for Enterprise Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/exploring-ea-mcp-server.md)**

    Query business application insights, capability mappings, architectural relationships, and rationalization data from your AI assistant, without opening your ServiceNow instance.

-   **[Enterprise Architecture for AICT plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-aict.md)**

    -   Associate AI systems with business applications whether you use Enterprise Architecture Workspace. The new Enterprise Architecture for AICT plugin stores these associations in its own data model and installs automatically as a dependency of AI Control Tower Core \(app-ai-governance\) application.
    -   Select business applications while creating an AI system in AI Control Tower. View AI adoption across your business application portfolio on the new **Business portfolio** tab in the AI Control Tower workspace homepage.
    Before you upgrade, review [Enterprise Architecture for AICT plugin installation and upgrade considerations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-ea-common-upgrade-considerations.md).

-   **[Migrate BA Product Model Map from EA Workspace job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-run-migrate-ba-product-model-map-job.md)**

    Use the new **Migrate BA Product Model Map from EA Workspace** scheduled job to move existing AI system-to-business application associations to the Enterprise Architecture for AICT plugin's data model. If you activated the AI Control Tower integration on an Enterprise Architecture Workspace version earlier than 10.1.3, run this job after you upgrade.


### What's changed

-   **[Business application insights trigger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/generate-insights-into-ba.md)**

    Choose how the ServiceNow Otto Business application insights skill is triggered on the **Define trigger** tab in the AI Admin Hub. With the **Automatic** option selected, business application insights are generated when you open a business application record page, and the side panel in the application rationalization bubble chart opens on the **Insights** tab.

    With the **User trigger** option selected, business application insights are generated only when you select **Generate insights**, and the side panel opens on the **Details** tab.

-   **[Enterprise Architecture query agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/ea-qna-overview.md)**

    Ask the Enterprise Architecture query agent about the impact of an infrastructure configuration item \(CI\), such as a database, database instance, server, or storage device. The agent follows CMDB relationships from the CI to the application services, business applications, and business capabilities that depend on it. You can also ask which infrastructure a business application or application service depends on.

-   **[ServiceNow Otto for Enterprise Architecture skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/exploring-now-assist-for-ea.md)**

    Use the Gemma 4 model with ServiceNow Otto for Enterprise Architecture skills that run on the Now LLM Service.

-   **[Technical debt list and form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/view-trm-tech-debt.md)**

    View the new **Number** field in the technical debt list and form. Select a value in the **Number** column in the Technology Portfolio page to open the technical debt record.


### Plugin information

-   **New plugins**

    Enterprise Architecture for AICT \(com.sn\_ea\_aict\): Provides the shared data model that connects AI systems and business applications, independently of the Enterprise Architecture Workspace plugin. Installs automatically as a dependency of AI Control Tower Core \(app-ai-governance\) application.


## Brazil Early Availability

This release adds configurable technical debt criteria, persistent technical debt states, and domain separation for AI Control Tower integration. It also enhances Technology Reference Model \(TRM\) product and lifecycle request workflows in the Enterprise Architecture Workspace.

### What's new

-   **[Technical debt settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-setup-tech-debt.md)**

    Control which server and reason criteria the **Populate TRM technical debts in the EA Workspace** scheduled job uses to create Technology Reference Model \(TRM\) technical debt records. Choose whether the job creates one technical debt record per server or a single record per software product regardless of how many servers it runs on, and select which of the standard reasons the job evaluates.

-   **[Persistent technical debt states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-manage-trm-technical-debt.md)**

    Technical debt records now persist across scheduled job runs instead of being deleted and re-created. Each record moves between **Active**, **Resolved**, and **Archived** states as the underlying discovered technology or technical debt configuration changes, preserving history for reporting and trend analysis.

-   **[Governing TRM product fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-trm-governing-fields.md)**

    View the TRM product and product lifecycle that govern a discovered technology's obsolescence status directly on the TPM Technology Lifecycle record. The **Governing TRM Product** and **Governing TRM Product Lifecycle** fields update automatically as matches change on later scheduled job runs.

-   **[Run a scheduled job to update the TCO score range](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-run-job-update-score-range-indicator-score.md)**

    Starting with this release, the **Business applications by TCO score** widget on the **Portfolio TCO** tab reads the TCO score band from a **Score range** field on the **Indicator Score** record instead of from a database view. If you're upgrading from a previous release, your existing **Indicator Score** records don't have this field populated, and the widget shows **\(empty\)** as the X-axis label instead of the TCO score bands. Run the new **Update Score Range in Indicator Score Table** scheduled job to populate the field on your existing records. This is a one-time, on-demand job that's inactive by default. New installations aren't affected, because the field is populated automatically as indicator scores are generated.


### What's changed

-   **[Domain separation for AI Control Tower integration with business applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-aict.md)**

    Enterprise Architecture Workspace now supports domain separation for AI system associations with business applications. On domain-separated instances, the business applications available for association reflect the domain hierarchy: you can associate applications in the global domain and in your current domain, and viewing the association from a parent domain shows the AI system associations created in that domain and in all of its child domains.

-   **Technical debt list and form**
    -   New **State** field shows whether the record is **Active**, **Resolved**, or **Archived**.
    -   New **Edition** field shows the software edition when the technical debt is created from a TRM product lifecycle that matches on both version and edition. The edition is part of the record's identity: a technical debt for version X, edition A is a separate record from a technical debt for version X, edition B.
    -   On the technical debt record page, the new **Discovered Technology** related list shows the TLM discovered technology records that generated the technical debt. It can be used as a starting point for the technical debt remediation.
    -   Select a value in the **Reason** column of the technical debt list to open the technical debt record directly.
-   **TRM product and lifecycle requests**
    -   A single TRM product request or product lifecycle request can now include multiple lifecycle records. It can support up to 5 version-and-edition combinations or 5 hardware models, with up to 10 phases each. This applies both in the Enterprise Architecture Workspace and when requesting from the service catalog.
    -   A standalone TRM product lifecycle request can include multiple child lifecycle records in a single bulk request. Approving or rejecting the parent request determines the outcome for all associated child records.
    -   Approvers can review requested and existing lifecycle records side by side using the new **Requested Lifecycles** and **Existing Lifecycles** tabs before approving or rejecting a request. Approvers can edit request details without triggering an approval decision.
-   **TLM Technology Lifecycle data**

    When multiple sources contribute lifecycle phase dates for the same product, the source with the highest configured rank now takes precedence, and phase dates are validated to stay in chronological order.


### Deprecated features

-   ****

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


### Plugin information

-   **Plugins planned for deprecation**

    Business Planner \(com.snc.apm.business\_planner\): Planned for deprecation in the D release. There is no replacement for this plugin.


