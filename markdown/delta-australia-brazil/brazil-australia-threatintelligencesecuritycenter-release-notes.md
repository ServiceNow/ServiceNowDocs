---
title: Combined Threat Intelligence Security Center release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Threat Intelligence Security Center from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-threatintelligencesecuritycenter-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 11
breadcrumb: [Products combined by family]
---

# Combined Threat Intelligence Security Center release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Threat Intelligence Security Center from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Threat Intelligence Security Center release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Threat Intelligence Security Center to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Upgrade information**
    -   Changes to the automated correlation rules affect which relationships are created after upgrade. Relationships created under the previous rule logic are preserved and aren't modified.
    -   Creation of potential relationships stops once the potential relationship table reaches its configured volume threshold. Review the threshold configuration after upgrade if your instance ingests high-volume feeds.
    -   The Relate Indicators with Objects Based on Common Observables correlation rule is removed. Relationships it created previously are preserved.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Threat Intelligence Security Center.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


 -   **[Generate a Case Report using generative AI](https://www.servicenow.com/docs/access?context=na-tisc-generate-ai-reports&family=australia&ft:locale=en-US)**

Introduced the TISC Report Authoring skill to generate analyst‑grade threat intelligence reports from threat cases. Supports configurable styling and analyst-defined instructions for content and focus.


 -   **[Summarize a case](https://www.servicenow.com/docs/access?context=now-assist-tisc-case-summarization&family=australia&ft:locale=en-US)**

The TISC Case Summarization skill brings generative AI capabilities directly into threat intelligence workflows.  Analysts can generate concise AI-powered summaries of threat cases, including case overview, findings, key actions taken, and recommended next steps.


 -   **[Automatic Threat Actor priority tagging](https://www.servicenow.com/docs/access?context=tisc-threat-actor-priority-tagging&family=australia&ft:locale=en-US)**

Enable automatic tagging of threat actors based on their origin locations.


 -   **[Configure TISC add-on in Splunk](https://www.servicenow.com/docs/access?context=tisc-configure-splunk&family=australia&ft:locale=en-US)**

TISC Add-on for Splunk Enterprise adds historical data ingestion and flexible expiration handling.


 -   **[Link nodes in the Relationship Graph](https://www.servicenow.com/docs/access?context=tisc-link-nodes&family=australia&ft:locale=en-US)**

The relationship graphs show immediate relationships to the home node for quick rendering of the graph. Filters enable analysts to narrow down to specific nodes and relationships. 


 -   **[MITRE ATT&amp;CK Technique Extraction Rules](https://www.servicenow.com/docs/access?context=mitre-extraction-rules&family=australia&ft:locale=en-US)**

Enhanced MITRE™ extraction rule schema to add a combined Techniques and tactics regex extraction type.


 -   **[Threat Hunting Playbook](https://www.servicenow.com/docs/access?context=tisc-threat-hunt-playbook&family=australia&ft:locale=en-US)**

Threat hunting playbook is now available out of the box. Analysts can use Playbooks for case management as a guided, stage-based workflow for investigations.


 -   **[Configure Premium Threat Feed for CrowdStrike](https://www.servicenow.com/docs/access?context=premium-threat-feed-for-crowdstrike&family=australia&ft:locale=en-US)**

Enhanced CrowdStrike premium Threat feed by adding `Malware` to the record types to ingest. Threat Actor records now link to `Malware` through `uses` and `develops` relationships, and to `Location` through `originates-from` and `targets` relationships. Report and Indicator records are linked to `Malware` through `associated-with`. Threat Actor records ingested from CrowdStrike now represent `capabilities`, `target industries`, `target regions`, `target countries`, and `origins` as structured tags rather than free-text, additional context fields. Users can use these attributes as filters.


 -   **[Have I Been Pwned integration](https://www.servicenow.com/docs/access?context=tisc-hibp-integration&family=australia&ft:locale=en-US)**

Added support in TISC for Have I been pwned? \(HIBP\) observable enrichment, enabling analysts to identify whether observables have been exposed in known data breaches instances.


 -   **[Configure Tagging Rules in TISC](https://www.servicenow.com/docs/access?context=tisc-tag-rules&family=australia&ft:locale=en-US)**

Introduced automated tagging of RSS feed records using configurable tagging rules to apply tags and taxonomies.


 -   **[Create a CWE record](https://www.servicenow.com/docs/access?context=tisc-create-cwe-record&family=australia&ft:locale=en-US)**

Introduced CWEs as related entities with support for relationship linking.


 -   **[Create Remediations](https://www.servicenow.com/docs/access?context=tisc-create-remediation-record&family=australia&ft:locale=en-US)**

Introduced remediations as related entities with support for relationship linking and added support for managing remediations.


 -   **[Create a Product](https://www.servicenow.com/docs/access?context=tisc-create-product&family=australia&ft:locale=en-US)**

Introduced products as related entities with support for relationship linking.


 -   **[Create a Vendor](https://www.servicenow.com/docs/access?context=tisc-add-vendor-to-vul&family=australia&ft:locale=en-US)**

Associated vendors as related entities with support for relationship linking.


 -   **[Automated creation of zero day vulnerability](https://www.servicenow.com/docs/access?context=tisc-zero-day-vuln-scenario&family=australia&ft:locale=en-US)**

Automatically generate zero day vulnerability records from flagged RSS feeds with extracted and linked CPE, CWE, and CVE details for enhanced threat analysis. The catalog now includes the RSS feed for **Google Project Zero**, enabling real-time detection of emerging threats.


 -   **[Create Vulnerability Assessment from a Vulnerability](https://www.servicenow.com/docs/access?context=tisc-vul-assess&family=australia&ft:locale=en-US)**

Initiate vulnerability assessments directly from identified issues for faster risk evaluation. Sample workflows and flow actions are included to automate the assessment process.


 -   **[Create Security Incident from a Vulnerability Record](https://www.servicenow.com/docs/access?context=tisc-create-security-incident&family=australia&ft:locale=en-US)**

Create security incident records directly from detected vulnerabilities to expedite incident response and streamline threat management workflows.


 -   **[Enable security incidents for vulnerabilities](https://www.servicenow.com/docs/access?context=tisc-view-security-context&family=australia&ft:locale=en-US)**

View vulnerabilities and related intelligence in the **TISC Context** tab of Security Incident Response Workspace, allowing analysts to quickly access risk data during investigations without navigating to separate records.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Import data using AI](https://www.servicenow.com/docs/access?context=import-data-using-ai&family=brazil&ft:locale=en-US)**

Import threat advisories as PDF or image files and let AI extract structured IOCs, threat actors, malware, and campaigns in seconds. Review extracted entities in a dedicated pane, grouped by type with AI extraction confidence score and reasoning, before they enter the library. Every AI-assisted import is captured in an audit record for full traceability.

-   **[Configure CrowdStrike NextGen SIEM sighting search](https://www.servicenow.com/docs/access?context=tisc-crowdstrike-ngsiem-integration&family=brazil&ft:locale=en-US)**

Search CrowdStrike Falcon NextGen SIEM for observable sightings directly from the Threat Intelligence Library, case artifacts, or an automated workflow, with results captured as sighting records on the observable.

-   **[Configure Premium Threat Feed for CrowdStrike](https://www.servicenow.com/docs/access?context=premium-threat-feed-for-crowdstrike&family=brazil&ft:locale=en-US)**

Ingest and correlate threat intelligence with integrated vulnerability intelligence feed from CrowdStrike.

-   **[Add security incident to TISC case](https://www.servicenow.com/docs/access?context=add-incident-to-case&family=brazil&ft:locale=en-US)**

Link entities to security incidents directly from either the SIR workspace or the entity record without creating a TISC case first.

-   **[Create a related record to link](https://www.servicenow.com/docs/access?context=tisc-create-new-related-record&family=brazil&ft:locale=en-US)**

Add related intelligence without leaving your investigation. Create and link new records from within your workflow.

-   **[Observable extraction from indicator patterns](https://www.servicenow.com/docs/access?context=tisc-extract-observables-from-indicators&family=brazil&ft:locale=en-US)**

Observables are extracted from STIX indicator pattern values during ingestion, added to the library, and related to the parent indicator automatically.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Threat Intelligence Security Center features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Now Assist &gt; ServiceNow Otto® announcement](https://www.servicenow.com/docs/access?context=sn-ai-implementation-landing&family=australia&ft:locale=en-US)**

ServiceNow Otto introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


 -   **[TISC Library Repository](https://www.servicenow.com/docs/access?context=tisc-ioc&family=australia&ft:locale=en-US)**

Enhanced Threat Intelligence Library list views by grouping observables, indicators, threat entities, RSS feed, and vulnerability artifacts into appropriate categories for improved navigation.


 -   **[Create Vulnerability Assessment from a Vulnerability](https://www.servicenow.com/docs/access?context=tisc-vul-assess&family=australia&ft:locale=en-US)**

Introduced a new button **Create Vulnerability Assessment** to conduct a vulnerability assessment for a specific vulnerability.


 -   **[Create Security Incident from a Vulnerability Record](https://www.servicenow.com/docs/access?context=tisc-create-security-incident&family=australia&ft:locale=en-US)**

Introduced a new button **Create Security Incident** to facilitate identifying vulnerabilities and enable faster incident response within the threat analysis.


 -   **[Threat Intelligence Security Center Catalog](https://www.servicenow.com/docs/access?context=threat-intelligence-security-center-catalogue&family=australia&ft:locale=en-US)**

Introduced a new catalog entry which includes the RSS feed for **Google Project Zero**, enabling real-time detection of emerging threats.


 -   **[MITRE ATT&amp;CK Technique Extraction Rules](https://www.servicenow.com/docs/access?context=mitre-extraction-rules&family=australia&ft:locale=en-US) and [View extracted MITRE ATT&amp;CK Techniques](https://www.servicenow.com/docs/access?context=mitre-extraction-method&family=australia&ft:locale=en-US)**

Enabled MITRE-ATT&amp;CK extraction rules for RSS feed to map and associate MITRE-ATT&amp;CK techniques.


 -   **[View RSS Feeds](https://www.servicenow.com/docs/access?context=define-rss-feeds&family=australia&ft:locale=en-US)**

Enhanced the RSS feed schema and parsers to support additional fields, including tags, taxonomies, status, and expiration time.


 -   **[Export intelligence data](https://www.servicenow.com/docs/access?context=tisc-export-observables&family=australia&ft:locale=en-US), [Sharing of Outbound Intelligence Records from GUI](https://www.servicenow.com/docs/access?context=tisc-create-intel-records-lib&family=australia&ft:locale=en-US), and [Add to TAXII Collections from Library List View](https://www.servicenow.com/docs/access?context=tisc-obs-add-taxii-collects&family=australia&ft:locale=en-US)**

Enhanced STIX 2.1 export to include Traffic Light Protocol \(TLP\) definitions applied to intelligence objects as TLP 2.0 marking definition objects. For more information, see [Marking Definition](https://www.servicenow.com/docs/access?context=marking-definition&family=australia&ft:locale=en-US).


 -   **[System properties for TISC Reports](https://www.servicenow.com/docs/access?context=reports-system-properties&family=australia&ft:locale=en-US)**

The system property `sn_sec_tisc.reporting.email_template_sn_sec_tisc_case` is no longer supported in TISC. It has been renamed to `sn_sec_tisc.default_report_email_template`, effective with the latest release.


 -   **[Configure custom MISP API feed](https://www.servicenow.com/docs/access?context=tisc-premium-misp&family=australia&ft:locale=en-US)**

Enhanced MISP API feed ingestion to handle events when the published timestamp is greater than the modified timestamp.


 -   **[Define Vulnerability](https://www.servicenow.com/docs/access?context=define-vulnerability&family=australia&ft:locale=en-US) and [Access the Vulnerability Entities](https://www.servicenow.com/docs/access?context=access-the-vulnerability-entities&family=australia&ft:locale=en-US)**

Enhanced the vulnerability schema to support additional vulnerability intelligence fields related to CVSS scoring, exploit details, and remediation information.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Automated correlation](https://www.servicenow.com/docs/access?context=automated-correlation-rules&family=brazil&ft:locale=en-US)**

Confirmed relationship rules now apply reputation checks and direction-agnostic deduplication, producing accurate source-of-traffic and destination-of-traffic relationships. Potential correlation rules are more selective and correlation requires a reputation match plus multiple shared observables.

-   **[TISC integration within SIR Workspace](https://www.servicenow.com/docs/access?context=tisc-sir-workspace&family=brazil&ft:locale=en-US)**

Directly link or unlink TISC entities in TISC Context tab of SIR workspace. The changes made in TISC context or TISC internal intelligence tab reflect bidirectionally.

-   **[CrowdStrike Falcon EDR integration](https://www.servicenow.com/docs/access?context=crowdstrike-edr-integration&family=brazil&ft:locale=en-US)**

Indicators sent to CrowdStrike Falcon EDR now carry "TISC Intelligence" as the source. A configuration option applies the TISC expiration time, falling back to the observable type expiration when the option is disabled. The Prevent action is supported alongside Detect.

-   **[Configure Premium Threat Feed for CrowdStrike](https://www.servicenow.com/docs/access?context=premium-threat-feed-for-crowdstrike&family=brazil&ft:locale=en-US)**

Ingest Vulnerability intelligence from CrowdStrike. Feed configurations are set to read-only when they're enabled, preventing changes that would disrupt an ingestion already in progress.

-   **[Review revoked pairs](https://www.servicenow.com/docs/access?context=tisc-review-revoked-mitre-associations&family=brazil&ft:locale=en-US)**

MITRE ingestion now provides a review queue for revoked technique-to-tactic associations that the newer MITRE ATT&amp;CK version no longer defines.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Threat Intelligence Security Center features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Threat Intelligence Security Center features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Now LLM service deprecation**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr></tbody>
</table>## Activation information

Review information on how to activate Threat Intelligence Security Center.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**

Install Threat Intelligence Security Center by requesting it from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Important:** Threat Intelligence Security Center is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install Threat Intelligence Security Center by requesting it from the [ServiceNow store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). Visit the [ServiceNow store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=brazil&ft:locale=en-US).

Install ServiceNow Otto for Threat Intelligence Security Center \(TISC\) to use the AI features.


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Threat Intelligence Security Center we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Additional requirements**
    -   The CrowdStrike vulnerability intelligence feed requires a CrowdStrike subscription that includes vulnerability intelligence, such as Falcon Adversary Intelligence or Falcon Adversary Intelligence Premium.
    -   Sighting search with CrowdStrike NextGen SIEM requires the CrowdStrike API base URL, a client ID, and a client secret. Which log repositories you can search depends on the Falcon subscriptions enabled on your account.
    -   The Extract information from documents skill must be enabled for the AI-powered intelligence import.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Threat Intelligence Security Center we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Threat Intelligence Security Center, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Threat Intelligence Security Center we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Threat Intelligence Security Center we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Threat Intelligence Security Center \(TISC\). Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.
-   Introduced AI-generated threat intelligence reports from case data with analyst-guided instructions.
-   Introduced AI-generated case summarization that analysts can use to generate concise case summaries.
-   Added playbooks support in Case Management, giving analysts a guided, stage-based workflow for investigations.
-   Added historical data ingestion and flexible expiration handling to TISC Add-on for Splunk Enterprise. 
-   Enhanced MITRE Extraction rule schema to add a combined Techniques and Tactics regex extraction type.
-   Enhanced Relationship Graph with filtering support and performance improvements.
-   Enhanced CrowdStrike feed to support ingestion of malwares.

 See [Threat Intelligence Security Center](https://www.servicenow.com/docs/access?context=tisc-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Accelerate threat response with AI by summarizing cases, generating reports automatically, and extracting threats directly from imported documents.
-   Reduce investigation time by centralizing threat intelligence from external feeds and internal sources into a single system of action.
-   Resolve threats faster by investigating and responding to cases in the Threat Analyst Workbench, using investigation canvases, MITRE ATT&amp;CK mapping, and case management.
-   Strengthen partner collaboration by sharing threat intelligence securely across trust boundaries with inbound and outbound sharing profiles, TAXII servers, and redaction controls.
-   Keep your intelligence library accurate with less effort by automating expiration, tagging, deduplication, and archival of threat data.

 See [Threat Intelligence Security Center](https://www.servicenow.com/docs/access?context=tisc-landing-page&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

