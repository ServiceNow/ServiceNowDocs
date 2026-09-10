---
title: ITOM - Advanced release notes
description: Version history for the ServiceNow ITOM - Advanced application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-advanced.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - IT Operations Management version history release notes, ServiceNow Store version history release notes]
---

# ITOM - Advanced release notes

Version history for the ServiceNow® ITOM - Advanced application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.1.5 - September 2026**
    -   New:
        -   LEAP
            -   Multi-taxonomy automation projectsLEAP can be configured to ingest and analyze incidents from multiple taxonomies to produce clusters and automation opportunities for all configured taxonomies. Existing single-taxonomy deployments are unaffected. Multi-taxonomy can be configured by admins using LEAP Properties.
            -   Generate LEAP knowledge base articlesWhen creating a KB article from a LEAP automation opportunity, users are prompted to select a knowledge base and category before the article is published, with the author field and article metadata auto-populated from the opportunity record. Admins can configure an list of eligible knowledge bases in LEAP Properties to control which options appear in the modal.
            -   LEAP MCP ServerLEAP skills are now accessible to external clients through MCP tools, enabling integration with third-party systems and workflows.
        -   AI Agents for Discovery
            -   Pattern diagnostic agentic workflow displays error codes when root causes are classified and provides enhanced remediation suggestions when the Error Framework plugin is active with mapped remediations.
            -   Pattern diagnostic agentic workflow log analysis covers the last five days and automatically expands to 30 days when no results are found in the initial period.
        -   ITOM URL Discovery
            -   You can now limit the number of URLs discovered through Broad URL Monitoring by using the new \[sn\_acc\_vis\_content.full\_url\_discovery\_daily\_max\_rows\] system property.
    -   Changed:
        -   LEAP
            -   Hide archived automation opportunitiesAutomation opportunities \(AOs\) from an earlier GAF \(Global Automation Framework\) run are now hidden by default. Previously, old AOs with resolution steps remained visible in the workspace after remapping. It was difficult to distinguish actionable AOs from old ones. After a GAF re-run, the old AOs are archived and no longer appear on the homepage. The artifacts of archived AOs are mapped to relevant new AOs.
            -   LEAP value dashboard expansionThe LEAP value dashboard now surfaces metrics for all automation outcome types along with existing playbook data. New sections display Ansible execution counts, agent-hours saved, and top playbooks by tickets resolved, KB article creation counts and top contributing clusters, and problem record \(PRB\) creation counts and top clusters. A summary at the top of the dashboard breaks total automation activity and savings attribution by outcome type such as LEAP playbooks, Ansible playbooks, KB articles, and PRBs, each with a trend indicator. The dashboard also displays ServiceNow Otto consumption data to track the consumed per action.
        -   AI Agents for Service Level Objective
            -   SLO Creator Agent now supports commitment-aware SLO generation and integrated risk calculation. The SLO Creator Agent operates with updated V2 instructions, enabling new skills for generating SLOs that account for commitments and utilizing a risk calculation tool. The implementation aligns with the SLO Gap Agent to ensure consistent behavior and parity.
    -   Fixed:
        -   AI Agents for Discovery
            -   Security defects in the Certificate Management Renewal AI Agent have been resolved.
        -   ITOM URL Discovery
            -   Navigation issues with bulk upload of the URLs are resolved.
    -   Removed:
        -   LEAP
            -   The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.
-   **Version 1.1.3 - August 2026**
    -   New:
        -   Cryptographic Asset Compliance
            -   Centralized cryptographic asset visibilityAssess the quantum safety of your certificates and cloud keys \(AWS KMS and Azure Key Vault\) discovered across on-premises and cloud environments from a centralized inventory, giving you a unified view of your organization's quantum safety posture.
            -   Policy-based risk indicatorsIdentify at-risk cryptographic assets, including risks like outdated algorithms, untrusted certificate authorities, and expiring certificates, helping you focus remediation efforts where they matter most.
            -   Post-quantum cryptography \(PQC\) compliance and quantum vulnerability dashboardsTrack PQC compliance status and quantum vulnerability through purpose-built dashboards. For example, certificates using RSA are automatically tagged as quantum-vulnerable, enabling data-driven migration planning toward quantum-resistant algorithms.
            -   Dependency graph for impact analysisVisualize where each cryptographic asset is used across your environment with an interactive dependency graph and assess downstream impact before initiating migration, reducing the risk of service disruption.
            -   AI-driven analysis and recommendationsGet AI-generated insights for each identified cryptographic asset, including recommended next steps to guide remediation and migration planning.
        -   AI Agents for Observability
            -   Extend alert analysis capabilities with the Azure Monitor MCP Agent and Gemini Cloud Assist A2A Investigation Agent in the analyze alert impact agentic workflow.
    -   Changed:
        -   AI Agents for Service Level Objective
            -   ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including AI agents for SLO. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.
        -   ITOM AI Agents for Service Mapping
            -   ServiceNow Otto is the new AI experience brand. This name change is reflected in ServiceNow products, including ITOM AI Agents For Service Mapping. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.
            -   The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.
        -   AI Agents for Observability
            -   ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including AI agents for Observability. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.
        -   LEAP
            -   Now Assist is renamed to ServiceNow Otto.All references to Now Assist are renamed and relevant images updated.
-   **Version 1.1.0 - July 2026**
    -   AI agent for Agent Client Collector \(ACC\) – Autonomously monitors ACC deployments across endpoints, ensuring agent health, version compliance, and seamless data collection without manual intervention, and provides guided troubleshooting experience.
    -   AI agent for Discovery – Proactively tracks and renews digital certificates enterprise-wide, eliminating outages by auto-detecting expirations and creating firewall rules.
    -   MID Guardian agent – Continuously monitors MID Server health and connectivity, providing guided troubleshooting of MID Server issues to resolve them seamlessly.
    -   ITOM AI agent for Service Mapping – Intelligently discovers application dependencies and maps services to infrastructure, autonomously resolving gaps to keep service maps accurate and business-ready.
    -   AI agent Topology Mapping – Discovery, classifies, and syncs AI agents deployed in cloud including the AI model metadata the agent deployed.
    -   AIOps Learning Enhanced Automation Playbooks - Amplifies efficiency by mining historical incident data to generate dynamic resolution playbooks, automate workflows, and reduce MTTR.
    -   ITOM URL Discovery - Discover URLs and SaaS applications from ITOM Browser Plugin .
-   **Version 1.0.10 - June 2026**
    -   New in ITOM - Advanced:
        -   Added AI agents to automate monitoring and remediation for Discovery, MID Servers, Certificate Management, Service Mapping, and LEAP.
        -   Added AI Agent Topology Mapping to provide governance and visibility to your AI estate.
        -   Added ITOM URL Discovery to surface shadow SaaS and unmanaged applications directly in the CMDB.
        -   Added ITOM Configuration Console to simplify onboarding for Discovery and Event Management with guided, best-practice setup.
        -   Added AIOps Learning Enhanced Automation Playbooks to turn historical incidents into dynamic, reusable resolution intelligence.
-   **Version 1.0.8 - May 2026**
    -   New:
        -   AI Agent Topology Mapping - Turn AI sprawl into a managed estate. As enterprises deploy agents, large language models, and prompts across AWS, Azure, and hybrid environments, most teams have no idea what's actually running, who owns it, or what data it touches. AI Agent Topology Mapping discovers and maps every AI agent, model, and prompt across your hyperscaler footprint and links them to the applications and services they support. The result is a single, authoritative view of your AI estate - the foundation for governance, cost control, security review, and responsible AI compliance.
        -   ITOM URL Discovery - Make shadow IT visible. Every browser session inside the enterprise carries signal about the SaaS apps, internal tools, and unmanaged services employees actually use - signal that today is invisible to IT. ITOM URL Discovery converts this browser activity into actionable intelligence, surfacing the applications and endpoints in real use across the organization and feeding them directly into the CMDB. The result is a closer-to-reality picture of the application landscape: faster discovery of unmanaged SaaS, sharper license optimization, earlier detection of risky or unsanctioned tools, and a CMDB that reflects how the business actually works rather than what was provisioned on paper.
        -   ITOM Configuration Console - ITOM Configuration Console introduces guided onboarding journeys for Discovery and Event Management, walking administrators step-by-step from installation to production deployment with built-in best-practice configuration.
-   **Version 1.0.7 - April 2026**
    -   The ITOM - Advanced app empowers entitled users to harness AI-driven automation across the most demanding IT operations challenges: from service mapping and cloud discovery to certificate management and firewall task automation.
    -   Purpose-built AI agents work autonomously in the background, eliminating manual toil and reducing operational risk with capabilities spanning LEAP Automation opportunity discovery, ACC health monitoring, and MID Guardian oversight, ITOM - Advanced transforms reactive IT ops into an intelligent, self-managing operation.

**Parent Topic:**[ServiceNow Store - IT Operations Management version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom.md)

