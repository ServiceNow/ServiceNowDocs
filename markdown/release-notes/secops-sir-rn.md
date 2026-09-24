---
title: Security Incident Response release notes
description: The ServiceNow Security Incident Response \(SIR\) application helps your organization connect security and IT teams, respond faster and more efficiently to threats, and gain insight into your organization's security posture. See the following sections for release notes by release.This release adds MITRE ATLAS threat detection to help you investigate and respond to security incidents faster. ServiceNow Otto for Security Incident Response \(SIR\) introduces conversational data analysis, value realization dashboard, and quality assessment reporting enhancements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/secops-sir-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [Security Incident Response, SIR Workspace 2.0, MITRE ATLAS, MITRE ATT&amp;CK, Process Mining, com.sn\_sir\_process\_mining\_cp]
breadcrumb: [Security Operations release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Security Incident Response release notes

The ServiceNow® Security Incident Response \(SIR\) application helps your organization connect security and IT teams, respond faster and more efficiently to threats, and gain insight into your organization's security posture. See the following sections for release notes by release.

## About Security Incident Response

-   Connect security and IT teams to respond faster and more efficiently to security threats.
-   Gain insight into your organization's security posture.
-   Automatically create and enrich security incidents by integrating with third-party detection and SIEM sources such as CrowdStrike Next-Gen SIEM and Microsoft Defender.
-   Rapidly build new integrations using Now Assist LLM-powered auto-code generation.
-   Visualize attack-defense relationships using MITRE-ATT&amp;CK and MITRE D3FEND data directly within a security incident.

See [Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sir-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Security Incident Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

    Install ServiceNow Otto for Security Incident Response \(SIR\) to use the AI features.

-   **Additional requirements**

    The Security Support Common plugin is activated automatically when any of the plugins for the main Security Operations applications are activated. These applications include Security Incident Response, Vulnerability Response, Threat Intelligence, and Configuration Compliance.


**Parent Topic:**[Security Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/security-operations-rn-landing.md)

## Brazil Early Availability

This release adds MITRE ATLAS threat detection to help you investigate and respond to security incidents faster. ServiceNow Otto for Security Incident Response \(SIR\) introduces conversational data analysis, value realization dashboard, and quality assessment reporting enhancements.

### What's new

-   **[MITRE ATLAS framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/about-mitre-atlas.md)**

    Detect, classify, and respond to AI- and ML-specific threats — such as prompt injection, model poisoning, data extraction, and adversarial attacks — using the MITRE ATLAS framework alongside MITRE-ATT&amp;CK. ATLAS techniques associated with a security incident appear in the MITRE node map, incident timeline, and MITRE info card with a distinct icon. This lets you tell MITRE-ATT&amp;CK and ATLAS techniques apart at a glance. Administrators can configure ATLAS-related properties on the Threat Intelligence Properties page.

-   ****
-   **[Analyze security incident data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/analyze-data-sir.md)**

    Ask questions about your security incident data in a conversational language, without writing queries or knowing how reports are structured. Ask follow-up questions in the same session or move to a different question. AI-generated responses include insights and recommendations rather than only direct answers.

-   **[Review Security Incident AI ROI Summary dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/ai-roi-summary-dashboard.md)**

    Track the value your team realizes from the AI features under Security Incident Response Management. The metrics include time saved per capability, total assists consumed, assists per resolved incident, and daily unique users, so you can see which capabilities are adopted.

-   **[Map incident fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/pan-cortex-xsiam-mapping.md)**

    Build Cortex XSIAM field mappings from a known incident. Select the Incident ID ingestion method and enter an ID in the XSIAM Incident ID field to retrieve its actual field values.

-   **[Automate incident updates and closures](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/pan-xsiam-automate-inc-updates.md)**

    Map Security Incident fields to Cortex XSIAM on the new **SIR to XSIAM Mapping** panel using drag-and-drop, override, and transformation scripts. When the check box is selected, any new or updated data from SIR Incident will automatically sync with the corresponding fields in the XSIAM portal.


### What's changed

-   **[Exploring Security incident quality assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/na-sir-quality-assessment.md)**

    Customize or regenerate entire draft reports or specific sections within it, before you share it with stakeholders.


### What's deprecated or removed

-   **Now LLM service deprecation**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


### Plugin information

-   **Deprecated plugins**

    Security Incident Response Process Mining Content Pack \(com.sn\_sir\_process\_mining\_cp\): This plugin is deprecated and replaced by the core Process Mining Content Pack application, which is automatically installed for Security Incident Response. No action is required.


