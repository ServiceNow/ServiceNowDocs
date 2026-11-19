---
title: Domain separation and Security Incident Response
description: Domain separation is supported in Security Incident Response\(SIR\). Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/security-management/security-incident-response/domain-separation-security-incident-response.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Understanding Security Incident Response, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Domain separation and Security Incident Response

Domain separation is supported in Security Incident Response\(SIR\). Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## Domain separation in SIR overview

In the Security Incident Response application, domain separation enables service providers \(SPs\) to standardize SOC \(Security Operations Center\) and SIR procedures. This is for the entire customer base they serve with lowered operational costs and a higher quality of service. Separate customer workspaces for workflows, dashboards, reports, and so forth, ensures that customer data is separated and never exposed to other customers.

Domain separation applies to all SIR application tables and to the shared Security Operations components that SIR is built on. SIR supports whatever domain separation the platform supports, and the standard visibility rules apply: a record in a parent domain can reference artifacts in a child domain, but a record in a child domain can't reference artifacts in a parent domain.

|Release|Support level|Notes|
|-------|-------------|-----|
|Brazil|Level 2 \(Data, Requestor, Fulfiller\)|All integrations reside across multiple domains.|
|Australia|Level 2 \(Data, Requestor, Fulfiller\)|All integrations reside across multiple domains.|
|Zurich|Level 2 \(Data, Requestor, Fulfiller\)|All integrations reside across multiple domains.|
|Geneva, Helsinki|No support|Initiation of data-level domain separation|
|Istanbul|Data only| |
|Jakarta|Level 2 \(Data, Requestor, Fulfiller\)|**New features**: 3rd-party Integrations support with Level 2 domain separation under a single instance of integration, including Threat Intelligence integrations|
|Kingston|Level 2 \(Data, Requestor, Fulfiller\)|**New features**: Sighting Search integration for SIR is enabled with multiple instances, but all instances still live under a single domain. Example: If two Splunk integrations are configured \(SplunkCLOUD and SplunkCORP\), both are used for incident response. They are used only in the domain where they were originally configured.|
|London|Level 2 \(Data, Requestor, Fulfiller\)|**New features**: All integrations reside across multiple domains|
|Madrid|Level 2 \(Data, Requestor, Fulfiller\)|All integrations can now reside across multiple domains. In the above example, SplunkCloud can be domain1 and SplunkCORP domain2.|
|New York|Level 2 \(Data, Requestor, Fulfiller\)|All integrations reside across multiple domains.|
|Orlando|Standard|All integrations reside across multiple domains.|
|Paris|Standard|All integrations reside across multiple domains.|

Domain separation for the Security Incident Response application covers the following product functionality:

-   Security alerts are directed to the appropriate domain of the user whose ID/ credential/ scope generates the incident and is registered as a Security Incident.
-   Observables extracted from alerts are stored in the domain of the security incident; security workflows in that domain orchestrate the response.
-   Integrations and capabilities are configured and activated per domain. These capabilities include:

    -   Threat Lookup
    -   Enrich Observable
    -   Enrich Configuration item
    -   Get Running Process
    -   Get Network Statistics
    -   Block Request
    -   Isolate Host
    -   Sighting Search
    -   Email Search and Delete
    -   Publish to Watchlist
    A capability stays generic across domains while each domain supplies its own implementation \(for example, a Sighting Search can call Splunk in one domain and QRadar in another\).

-   Results from Response Automation \(such as Threat Lookup or Sighting Search\) are stored in the domain of the security incident.
-   Related incidents \(by shared observables\), users and configuration items are cross-referenced within the domain of the security incident.
-   Manual response tasks, knowledge base articles and runbooks are added to or referenced from the domain of the security incident.
-   Incident metrics are displayed on dashboards and in reports for the incidents in the domain.

**Note:** In the preceding cases, the overarching principles of visibility in separated domains in the NOW Platform apply. As always, an incident in the parent domain can reference artifacts in the child domain, but not the other way around.

## How domain separation works in Security Incident Response

The Security Incident Response application manages the life cycle of a security incident end to end. The following use cases are domain-separation aware:

-   **Ingestion of events and alerts** to create security incidents for the analyst in the customer SOC or the MSP to respond:
    -   Email parsers \(platform based, user-reported phishing, custom\)
    -   De-duplication events/alerts prior to incident creation
    -   Auto extraction of observables
    -   Applications in third-party SIEM store
-   **Enrichment** of artifacts involved in the incidents \(IP, URLs, domains, file hashes\):
    -   Asset enrichment \(CMDB\)
    -   Users \(Platform\)
    -   Automation: Observable enrichment \(Ex: WhoIs\)
-   **Investigate** the incidents with the help of the artifacts and their reputation or association with known threats
    -   Orchestrate: Playbooks and knowledge base articles
    -   Automation: Threat Lookup \(Ex: VirusTotal\), Sighting Search \(Ex: Splunk\), Get Running Processes \(Ex: Carbon Black\)
-   **Eradicate** the threat-related artifacts involved in the incident based on the investigation performed
    -   Orchestrate: Playbooks and knowledge base articles
    -   Automation: Email search and delete \(Ex: Microsoft Exchange\), Block IP \(Ex: Palo Alto Firewall\)
-   **Measure** the efficiency or Incident response operations
    -   Performance Analytics Dashboards: Productivity and incident trends
    -   Reconstruction of incident investigation steps from work notes
    -   Post-incident review

## Domain separation setup

Setting up domain separation for Security Incident Response doesn’t require any additional steps. All Security Incident Response tables acquire the Domain column after the instance is domain separated.

## Domain-separated data

Data can be domain-separated, which means:

-   Security incidents in one domain can’t be viewed from other domains.
-   Observables extracted from an incident aren't visible from other domains.
-   Integrations and their configuration can be set up per domain. Administrators copy a global integration into a domain, then configure it there.
-   Capabilities, enrichment mappings, security tag rules, filter groups, property overrides, and MITRE ATT&amp;CK data can all be domain-specific.
-   Capabilities stay generic across domains, but each domain can use its own implementation. For example, a Sighting Search can call Splunk in one domain and QRadar in another.
-   Automation results are stored in the incident's domain.

## Configuration

All aspects of product configuration are self-contained in a domain-separated environment. Setup can be tailored for individual domains.

**Note:** Business logic and the processes in \#2-5 below can be administered within the tenant domain.

The following tasks must be configured:

1.  System Administration
    -   Assign roles to users and groups of users: [User roles installed with Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/security-incident-response/installed-with-sir.md)
    -   Install one or more third-party integration plugins to work with Security Incident Response: [Security Incident Response integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/security-incident-response/sir_integrations.md)
2.  Security Incident Response Administration
    -   Add or review roles: [Components installed with Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/security-incident-response/installed-with-sir.md)
    -   Configure groups and users: [Create a security incident group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/security-incident-response/setup-assistant-reference.md)
    -   Set up incident escalations: [Escalate a security incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/security-incident-response/escalate-security-incident.md)
    -   Set up security incident risk score calculators: [Understanding security incident calculators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/security-incident-response/setup-assistant-reference.md)
    -   Set up service level agreements: [Create a Security Incident Response SLA](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/security-incident-response/setup-assistant-reference.md)
    -   Set up security incident process definitions: [Understanding Security Incident Response process definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/security-incident-response/setup-assistant-reference.md)
    -   Set up post-incident review processes: [Manage post incident activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/security-incident-response/c_PostIncidentReview.md)
3.  Security incident email settings
    -   Set the email parsing inbox: [Security Operations email parsing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/email-parsing.md)
    -   Set up email parsers for alert ingestion: [Create email parsers in Security Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/parsing-emails.md)
    -   Set up email matching rules for user-reported phishing: [Create rules to validate user-reported phishing attacks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/security-incident-response/setup-assistant-reference.md)
    -   Set up email inbound actions: [Inbound email actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_InboundEmailActions.md)
4.  Security incident playbook settings
    -   Review and set up runbook documents: [Create a Security Incident Response runbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/security-incident-response/setup-assistant-reference.md)
    -   Set up security incident workflows: [Security Operations common functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/sec-ops-common-functionality.md)
5.  Capability configurations
    -   Block request: [Security Operations Integration- Block Request capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/block-request-capability.md)
    -   Email search and delete: [Security Operations Integration- Email Search and Delete capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/email-search-capability.md)
    -   Enrich configuration item: [Security Operations Integration- Enrich CI capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/enrich-ci-capability.md)
    -   Enrich observable: [Security Operations Integration- Enrich Observable capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/enrich-observable-capability.md)
    -   Get network statistics: [Security Operations Integration- Get Network Statistics capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/get-network-statistics-capability.md)
    -   Get running processes: [Security Operations Integration- Get Running Processes capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/get-running-processes-capability.md)
    -   Isolate host: [Security Operations Integration- Isolate Host capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/isolate-host-capability.md)
    -   Publish to Watchlist: [Security Operations Integration- Publish to Watchlist capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/pubish-to-watchlist-capability.md)
    -   Sighting search: [Security Operations Integration- Sightings Search capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/sightings-search-capability.md)
    -   Threat lookup: [Security Operations Integration - Threat Lookup capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/sec-ops-threat-lookups-capability.md)

## How tenant domains manage their own application data

-   Tenant domain owners create their own email parsing rules for ingesting security incidents.
-   Tenant domain owners can configure specific integrations exclusively for use within the domain.
-   Tenant domain owners can create their own incident response workflows.
-   Tenant domain owners can create their own incident categories, incident response knowledge base articles, and runbooks to be associated with incident response workflows.
-   Tenant domain users create and close their own security incidents.

Tenant administrators with the sn\_si.admin role can administer, within their own domain, the SIR administration, email, playbook and capability configuration listed earlier.

## Business logic and processes that can be domain separated by instance owner

-   Security Incident Response users and groups
-   Security Incident Response integrations \( \(activated per domain\)\)
-   Email parsing rules for incident creation
-   Business rules to consolidate multiple events or alerts into a security incident
-   Workflows for incident response orchestration
-   Security incident risk score calculators
-   Security incident escalation path
-   Security incident SLAs
-   Security incident process definitions
-   Security incident post-incident review processes

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

