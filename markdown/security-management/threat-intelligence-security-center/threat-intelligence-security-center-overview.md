---
title: Explore
description: Threat Intelligence Security Center \(TISC\) enables you to collaborate with threat intelligence teams by collecting, processing, and analyzing threat intelligence feeds in a centralized workspace.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-04-07"
reading_time_minutes: 5
breadcrumb: [Threat Intelligence Security Center, Security Operations]
---

# Explore

Threat Intelligence Security Center \(TISC\) enables you to collaborate with threat intelligence teams by collecting, processing, and analyzing threat intelligence feeds in a centralized workspace.

TISC manages data collection and processing, including deduplication, normalization, and aggregation. It analyzes and disseminates threat intelligence and provides an administration workspace Threat Intelligence Security Center.

Watch an overview about the Threat Intelligence Security Center application.

Threat Intelligence Security Center \(TISC\) Overview 

## Key features

Threat Intelligence Security Center \(TISC\) key features:

**Threat intelligence management:**

-   **Curated Catalog of OSINT Threat Feeds**: Provides access to a broad selection of popular open-source threat intelligence feeds, providing wide coverage.
-   **Premium Feed Integration**: Enhances the quality of threat intelligence by integrating premium feeds.
-   **Automated Observable Extraction**: Automatically identifies and extracts the commonly used observable types from uploaded files, streamlining the threat data ingestion process.
-   **Diverse Data Aggregation**: Supports multiple data formats including STIX, MISP, JSON, and others, enabling seamless feed consolidation.
-   **Enrichment Capabilities &amp; Validation**: Provides enrichment and validation capabilities by removing false positives, assigning confidence scores, validating indicators, and adding contextual information.

**Integration capabilities:**

-   Enrich observables with threat intelligence using Threat Lookup, Sighting Search, and Observable Enrichment to assess whether an observable is malicious.
-   CrowdStrike Falcon EDR: Supports continuous monitoring and real time alerting.
-   Security tools integrations: Orchestrates security tools including SIEMs, EDRs, and firewalls.
-   Correlation Rules Engine: Automatically establishes relationships between intelligence records, enabling deeper insight into threat patterns.

**Threat Intelligence Analysis and operations:**

-   Customizable Threat Scoring: Enables fine-tuning of threat scores for more nuanced and accurate threat assessment.
-   Internal Intelligence integration: Enables integration of internal intelligence sources, including Vulnerability Response \(VR\), Security Incident Response \(SIR\), and Configuration Management Database \(CMDB\).
-   User-Specific Dashboards: Tailors visualizations and data views according to Threat Intelligence personas, improving user experience and relevance.
-   Graphical Visualization Tools: Provides intuitive graphical visualizations such as relationship graphs and interactive investigation canvases to simplify analysis of complex threat intelligence data.
-   Dedicated Analyst Workspace: Provides a dedicated, streamlined Threat Intelligence Analyst workspace that enables threat intelligence analysts to focus on investigation and analysis.
-   Threat Case Management: Supports investigative workflows with task tracking and case handling.
-   MITRE-ATT&amp;CK Integration: Enables users to link case records with MITRE-ATT&amp;CK framework data for enhanced kill chain analysis.
-   Seamless SIR Integration: Provides a smooth data migration and interoperability between Security Incident Response and Threat Intelligence Security Center applications.
-   Notification &amp; Alert Rules: Establishes trigger alerts to notify teams based on evolving threat intelligence.
-   Data Retention &amp; Cleanup Policies: Enables organizations to define data management rules to maintain application performance and conformance.
-   Reporting &amp; Collaboration: Generates comprehensive status reports and investigation summaries using rich-text editors and customizable templates.
-   Domain Separation for MSSPs: Supports multitenant environments, enabling Managed Security Service Providers \(MSSPs\) to segregate customer data securely.
-   Extensive API integration: Offers TISC API for seamless connectivity with other security tools and platforms.

## Threat Intelligence Security Center users and roles

<table id="table_bnq_m45_v3c"><thead><tr><th>

User

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Administrator

</td><td>

Administers and configures the initial setup and ongoing maintenance of the Threat Intelligence Security Center, including configuring data sources and managing settings.

</td><td>

-   sn\_sec\_tisc.admin
-   sn\_sec\_tisc.read

</td></tr><tr><td>

Analyst

</td><td>

Threat Intelligence Analysts conduct analysis and research tasks requested by the team. They can import ad hoc intelligence to support their work and use the system's tools for analysis, collaboration, and managing the intelligence library.

</td><td>

-   sn\_sec\_tisc.analyst
-   sn\_sec\_tisc.read

</td></tr></tbody>
</table>## Threat Intelligence Security Center benefits

The following table describes the key features and benefits of Threat Intelligence Security Center.

<table id="table_ftc_dwt_z3c"><thead><tr><th>

Feature

</th><th>

Benefit

</th><th>

Users

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Dashboards/Home page

</td><td>

Threat Intelligence Security Center home page provides high-level visibility into an organization's threat intelligence, data feeds overview, intelligence sharing and security posture.

</td><td>

-   Administrators
-   Analysts

</td><td>

-   sn\_sec\_tisc.read
-   sn\_sec\_tisc.analyst
-   sn\_sec\_tisc.admin

</td></tr><tr><td>

Threat Intel Library

</td><td>

TISC threat library is a collection of organized objects and entities that provides structured and unstructured security threat information. Threat information is available as feeds from sources such as STIX, MISP, and others.

</td><td>

-   Administrators
-   Analysts

</td><td>

-   sn\_sec\_tisc.read
-   sn\_sec\_tisc.analyst
-   sn\_sec\_tisc.admin

</td></tr><tr><td>

Integrations

</td><td>

TISC integrations module centrally manages and configures all Threat Intelligence feed sources and enrichment integrations from a single location, enabling automated and scheduled ingestion of Threat Intelligence data.

</td><td>

-   Administrators
-   Analysts

</td><td>

-   sn\_sec\_tisc.read
-   sn\_sec\_tisc.analyst
-   sn\_sec\_tisc.admin

</td></tr><tr><td>

Administration

</td><td>

TISC Administration module centrally configures and manages all aspects of TISC data administration. This includes filtering and approval rules, threat scoring, security control lists, taxonomies, notifications, and report templates.

</td><td>

Administrators

</td><td>

-   sn\_sec\_tisc.read
-   sn\_sec\_tisc.admin

</td></tr><tr><td>

Imports/Exports

</td><td>

-   TISC Imports module: Flexibly import Threat Intelligence data from multiple sources and formats including structured files, standard formats such as STIX and MISP, raw text, and unstructured files. Track import jobs and approvals in a single view.
-   TISC Exports module: Export observables, indicators, and cases individually or in bulk in recommended formats such as CSV and STIX 2.1.

</td><td>

-   Administrators
-   Analysts

</td><td>

-   sn\_sec\_tisc.read
-   sn\_sec\_tisc.analyst
-   sn\_sec\_tisc.admin

</td></tr><tr><td>

Threat Analyst Workbench

</td><td>

Manage end-to-end threat investigations from a single workspace to create and track cases and case tasks. Collect internal intelligence records such as observables, threat actors, and campaigns, and visualize complex relationships using the Investigation Canvas.Accelerate analysis by adding artifacts, running enrichment actions, generating investigation and executive summary reports, and creating security incidents directly from cases.

</td><td>

-   Administrators
-   Analysts

</td><td>

-   sn\_sec\_tisc.read
-   sn\_sec\_tisc.analyst
-   sn\_sec\_tisc.admin

</td></tr><tr><td>

Threat Intelligence Sharing

</td><td>

Securely share threat intelligence within and across organizations using automated and manual sharing workflows. Control what is shared through customizable templates, redaction capabilities, and configurable approval rules for both inbound and outbound intelligence.Maintain conformance and traceability through comprehensive audit logging, data retention policies, and bi-directional TISC - to - TISC exchange, while managing TAXII user and group access for secure, governed data sharing.

</td><td>

-   Administrators
-   Analysts

</td><td>

-   sn\_sec\_tisc.read
-   sn\_sec\_tisc.analyst
-   sn\_sec\_tisc.admin

</td></tr></tbody>
</table>-   **[TISC Key terminology](tisc-key-terminology.md)**  
Key terms and definitions used in TISC to help you understand threat intelligence concepts and navigate the interface effectively.
-   **[TISC Workspace](../task/view-threat-intelligence-security-center-homepage.md)**  
View a centralized dashboard of threat intelligence data including feeds overview, trending threats, and intelligence sharing metrics. Monitor your security posture with trending intelligence data.

**Related topics**  


[Configuring Threat Intelligence Security Center](../concept/tisc-configure.md)

[Download TISC application from ServiceNow Store](tisc-download-app-first-time.md)

[Set up Threat Intelligence Security Center](set-up-threat-intelligence-security-center.md)

