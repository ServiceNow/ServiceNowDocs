---
title: Threat Intelligence Security Center release notes
description: The ServiceNow Threat Intelligence Security Center  application is built natively on the ServiceNow AI Platform to operationalize threat intelligence from feed ingestion and enrichment to investigation, response, and sharing. TISC enables security teams to act efficiently on intelligence and defend against threats.  See the following sections for release notes by version.Extract threat intelligence from unstructured documents using AI, sightings with CrowdStrike NextGen SIEM, and link TISC entities directly to security incidents in the SIR workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/secops-tisc-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Security Operations release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Threat Intelligence Security Center release notes

The ServiceNow® Threat Intelligence Security Center  application is built natively on the ServiceNow AI Platform to operationalize threat intelligence from feed ingestion and enrichment to investigation, response, and sharing. TISC enables security teams to act efficiently on intelligence and defend against threats.  See the following sections for release notes by version.

## About Threat Intelligence Security Center

-   Accelerate threat response with AI by summarizing cases, generating reports automatically, and extracting threats directly from imported documents.
-   Reduce investigation time by centralizing threat intelligence from external feeds and internal sources into a single system of action.
-   Resolve threats faster by investigating and responding to cases in the Threat Analyst Workbench, using investigation canvases, MITRE ATT&amp;CK mapping, and case management.
-   Strengthen partner collaboration by sharing threat intelligence securely across trust boundaries with inbound and outbound sharing profiles, TAXII servers, and redaction controls.
-   Keep your intelligence library accurate with less effort by automating expiration, tagging, deduplication, and archival of threat data.

See [Threat Intelligence Security Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/tisc-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Threat Intelligence Security Center by requesting it from the [ServiceNow store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). Visit the [ServiceNow store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

    Install ServiceNow Otto for Threat Intelligence Security Center \(TISC\) to use the AI features.

-   **Upgrade information**
    -   Changes to the automated correlation rules affect which relationships are created after upgrade. Relationships created under the previous rule logic are preserved and aren't modified.
    -   Creation of potential relationships stops once the potential relationship table reaches its configured volume threshold. Review the threshold configuration after upgrade if your instance ingests high-volume feeds.
    -   The Relate Indicators with Objects Based on Common Observables correlation rule is removed. Relationships it created previously are preserved.
-   **Additional requirements**
    -   The CrowdStrike vulnerability intelligence feed requires a CrowdStrike subscription that includes vulnerability intelligence, such as Falcon Adversary Intelligence or Falcon Adversary Intelligence Premium.
    -   Sighting search with CrowdStrike NextGen SIEM requires the CrowdStrike API base URL, a client ID, and a client secret. Which log repositories you can search depends on the Falcon subscriptions enabled on your account.
    -   The Extract information from documents skill must be enabled for the AI-powered intelligence import.

**Parent Topic:**[Security Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/security-operations-rn-landing.md)

## Brazil Early Availability

Extract threat intelligence from unstructured documents using AI, sightings with CrowdStrike NextGen SIEM, and link TISC entities directly to security incidents in the SIR workspace.

### What's new

-   **[Import data using AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/import-data-using-ai.md)**

    Import threat advisories as PDF or image files and let AI extract structured IOCs, threat actors, malware, and campaigns in seconds. Review extracted entities in a dedicated pane, grouped by type with AI extraction confidence score and reasoning, before they enter the library. Every AI-assisted import is captured in an audit record for full traceability.

-   **[Configure CrowdStrike NextGen SIEM sighting search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/tisc-crowdstrike-ngsiem-integration.md)**

    Search CrowdStrike Falcon NextGen SIEM for observable sightings directly from the Threat Intelligence Library, case artifacts, or an automated workflow, with results captured as sighting records on the observable.

-   **[Configure Premium Threat Feed for CrowdStrike](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/premium-threat-feed-for-crowdstrike.md)**

    Ingest and correlate threat intelligence with integrated vulnerability intelligence feed from CrowdStrike.

-   **[Add security incident to TISC case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/add-incident-to-case.md)**

    Link entities to security incidents directly from either the SIR workspace or the entity record without creating a TISC case first.

-   **[Create a related record to link](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/tisc-create-new-related-record.md)**

    Add related intelligence without leaving your investigation. Create and link new records from within your workflow.

-   **[Observable extraction from indicator patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/tisc-extract-observables-from-indicators.md)**

    Observables are extracted from STIX indicator pattern values during ingestion, added to the library, and related to the parent indicator automatically.


### What's changed

-   **[Automated correlation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/automated-correlation-rules.md)**

    Confirmed relationship rules now apply reputation checks and direction-agnostic deduplication, producing accurate source-of-traffic and destination-of-traffic relationships. Potential correlation rules are more selective and correlation requires a reputation match plus multiple shared observables.

-   **[TISC integration within SIR Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/tisc-sir-workspace.md)**

    Directly link or unlink TISC entities in TISC Context tab of SIR workspace. The changes made in TISC context or TISC internal intelligence tab reflect bidirectionally.

-   **[CrowdStrike Falcon EDR integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/crowdstrike-edr-integration.md)**

    Indicators sent to CrowdStrike Falcon EDR now carry "TISC Intelligence" as the source. A configuration option applies the TISC expiration time, falling back to the observable type expiration when the option is disabled. The Prevent action is supported alongside Detect.

-   **[Configure Premium Threat Feed for CrowdStrike](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/premium-threat-feed-for-crowdstrike.md)**

    Ingest Vulnerability intelligence from CrowdStrike. Feed configurations are set to read-only when they're enabled, preventing changes that would disrupt an ingestion already in progress.

-   **[Review revoked MITRE tactic and technique associations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/tisc-review-revoked-mitre-associations.md)**

    MITRE ingestion now provides a review queue for revoked technique-to-tactic associations that the newer MITRE ATT&amp;CK version no longer defines.


### What's deprecated or removed

-   **Now LLM service deprecation**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


### Plugin information

-   **New plugins**

    sn\_sec\_cs\_sighting: Integrates Threat Intelligence Security Center with CrowdStrike Falcon NextGen SIEM for sighting search.


