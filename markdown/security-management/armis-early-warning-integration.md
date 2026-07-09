---
title: Early Warning for Security Exposure Management integration
description: The Early Warning for Security Exposure Management integration, powered by Armis, enriches the Unified Security Exposure Management \(USEM\) with vulnerability intelligence of imminent exploit, enabling your security team to prioritize and patch vulnerabilities months before threat actors weaponize them. Verify keyref: UI shows "Security Exposure Management" workspace header — confirm whether var.unified-sec-exp-mgmt is the correct product key or whether a different key applies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/armis-early-warning-integration.html
release: australia
topic_type: concept
last_updated: "2026-06-24"
reading_time_minutes: 8
keywords: [Armis Early Warning, CVE enrichment, vulnerability intelligence, Security Exposure Management]
breadcrumb: [Integrate, Unified Security Exposure Management, Security Operations]
---

# Early Warning for Security Exposure Management integration

The Early Warning for Security Exposure Management integration, powered by Armis, enriches the Unified Security Exposure Management \(USEM\) with vulnerability intelligence of imminent exploit, enabling your security team to prioritize and patch vulnerabilities months before threat actors weaponize them.

The Early Warning for Security Exposure Management integration pulls a curated list of Common Vulnerabilities and Exposures \(CVEs\) into Unified Security Exposure Management, enriching vulnerability records with threat intelligence validated through honeypot activity, Open Source Intelligence Framework \(OSINT\), and Armis research. This enrichment enables security teams to prioritize vulnerabilities before public disclosure and coordinate response through established vulnerability management workflows.

## When Early Warning matters

Early Warning shifts vulnerability management from reactive crisis to strategic advantage - detecting which vulnerabilities threat actors are actively trying to exploit.

**Without early warning**: When a vulnerability is published, threat actors can exploit it within hours. Your team patches reactively under pressure, often with inadequate testing and high risk of failure.

**With early warning**: Your team has months to test patches, coordinate across regions, validate against your systems, and deploy during planned maintenance windows. You patch proactively, not in crisis mode.

**When Early Warning Is critical**: Early Warning is most valuable for organizations where patching takes time or downtime is costly:

-   **Legacy systems and industrial controls \(ICS/SCADA\)**: Systems that can't be rebooted quickly or easily patched. Early warning provides time for safe, planned updates instead of emergency changes that risk production downtime.
-   **Healthcare systems**: Patient care equipment and Electronic Health Record \(EHR\) systems require validation before patching. Early warning allows time to coordinate updates during low-patient-census windows without disrupting care.
-   **Manufacturing and operations**: Downtime costs millions per hour. Early warning allows time to plan patches during scheduled maintenance windows instead of emergency shutdowns.
-   **Financial services and payment systems**: Patch windows are scheduled in advance. Early warning ensures patches are tested and ready to deploy when the window arrives, instead of scrambling on the deployment day.
-   **Multi-region enterprises**: Complex environments with factories, offices, or data centers across regions take time to coordinate. Early warning provides the runway to test and deploy across all sites safely.
-   **Regulated industries**: Compliance auditors want to see proactive vulnerability management, not reactive patch-and-pray. Early warning demonstrates a prevention-first security posture.
-   **High-value targets**: Organizations subject to nation-state or sophisticated cyber attacks. Early warning closes the window where you're undefended before threat actors act.

In these scenarios, detecting exploits before public disclosure allows safe, coordinated patching instead of reactive, high-risk emergency updates.

## How Early Warning integrates with USEM

When you integrate Early Warning for Security Exposure Managementwith Unified Security Exposure Management \(USEM\), early warning signals automatically feed into your vulnerability prioritization workflow:

1.  Early Warning detects that threat actors are planning to exploit CVE-XXXX.
2.  USEM receives early warning signal and automatically elevates the priority of that CVE in your inventory.
3.  Your team prioritizes patching this vulnerability ahead of others, even if severity scores don't reflect the real-world threat.
4.  You patch proactively before the vulnerability is published and exploits become available.

This means your security team spends time on the vulnerabilities that actually matter- the ones threat actors are targeting and not just the ones with the highest Common Vulnerability Scoring System \(CVSS\) scores.

The integration appears in the Security Exposure Management workspace alongside other enrichment integrations such as the CISA Known Exploited Vulnerabilities integration. You can monitor integration run history, ingestion health, and processing health from the integration overview page.

## Key benefits

This integration provides the following benefits:

-   Earlier risk prioritization: Early warning flags surface alongside your vulnerability risk scores, so remediation teams focus on the threats that matter most. Instead of patching by CVSS score alone, you patch based on real-world threat actor behavior.
-   Faster remediation without extra setup: Early warning CVEs trigger existing Vulnerability Change Management workflows automatically, with no custom integration required
-   Faster identification of at-risk assets: Filter findings by early warning status to surface which assets carry elevated risk
-   Built-in asset correlation: Early warning signals roll up from CVE records to third-party entries automatically, extending risk visibility to the assets already tracked in your Vulnerability Response data with no additional CMDB mapping required

## How it works

The Early Warning for Security Exposure Management integration performs the following operations:

1.  **Detection**: Identifies a vulnerability that threat actors are planning to exploit, often months before it's publicly known.
2.  **Integration**: The early warning signal is ingested into USEM and automatically elevates the priority of that CVE in your vulnerability inventory.
3.  **Prioritization**: Your security team sees the early warning flag and prioritizes patching this vulnerability ahead of others, even if CVSS scores don't reflect the real-world threat.
4.  **Response**: Your team coordinates a patch deployment during a planned maintenance window. By the time the vulnerability is published publicly, your systems are already protected.

Your team spends time on vulnerabilities that threat actors are actually targeting, not just the ones with the highest severity scores.

## Data available in USEM

When you integrate Early Warning for Security Exposure Management, two new columns appear in your vulnerability records:

-   **Armis Early Warning:** A flag indicating that threat actors are planning to exploit this CVE
-   **Armis Early Warning CVD Attributes:** Detailed threat intelligence including:
    -   CVE ID and affected product
    -   Intelligence date \(when Armis detected the threat actor activity\)
    -   Admiralty score \(confidence rating of the threat intelligence\)
    -   Honeypot detection date
    -   Research date

You can use these columns to filter, sort, and prioritize your vulnerability remediation workflow.

The integration appears in the Security Exposure Management workspace alongside other enrichment integrations, such as CISA Known Exploited Vulnerabilities. From the integration overview page, you can monitor run history, ingestion health, and processing status. For more information, see [Security Exposure Management Workspace List view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-workspace-list-page.md)

## Admiralty score

Each CVE in the Armis feed includes an Admiralty score - a confidence rating based on the NATO Admiralty grading system. Scores range from A1–A6, B1–B6, C1–C6, D1–D6, E1–E6, and F1–F6, where A1 represents information from a completely reliable source that has been independently corroborated. A lower confidence rating does not prevent a CVE from being identified as an early warning signal. CVEs with lower Admiralty scores may still be surfaced when other factors indicate potential relevance or risk.

You can use the Admiralty score as an additional condition in a risk rule to refine prioritization. For example, you can configure the rule to apply a weight only to CVEs whose admiralty score meets a defined reliability threshold.

## Customizing risk rules

The early warning flag and Admiralty score are available as criteria in your risk rules, allowing you to customize how early warnings influence your vulnerability scores.

In the default risk calculator, you can:

-   Adjust the weight applied to early warning CVEs
-   Add Admiralty score as an additional condition for refinement
-   Create custom rules that combine early warning signals with other risk criteria

In the default risk calculator, you can adjust the weight or add the admiralty score as an additional condition to refine prioritization.

Because the early warning flag can be set to **true** even when no known exploit exists in other feeds such as CISA KEV or Exploit Prediction Scoring System \(EPSS\), the integration extends risk coverage to CVEs that have not yet appeared in those other intelligence sources.

## Key components

The Early Warning for Security Exposure Management integration consists of the following components:

-   **Integration plugin**

    Early Warning for Security Exposure Management\(`com.snc.vulnerability.ew`\): Handles data ingestion via the Vulnerability Integration Framework

-   **CVD attributes table**

    `sn_vul_ew_cvd_attributes`: Stores early warning-specific threat signals \(admiralty score, honeypot date, intelligence date, research date, CWE\)

-   **Flag rollup**

    Business rules propagate `ew_exists` flag from NVD entries to third-party entries for consolidated risk assessment

-   **Risk calculator field**

    `vulnerability.ew_exists`: Boolean risk criteria available for custom risk rule weighting


## Dependencies and prerequisites

The Early Warning for Security Exposure Managementintegration requires the following:

-   Unified Security Exposure Management \(Vulnerability Response v30.x\)
-   Vulnerability Integration Framework plugin
-   Access to Armis threat intelligence feed and valid authentication credentials

-   **[Configure the Early Warning for Security Exposure Management integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/t-configure_early_warning_integration.md)**  
Install and configure the Early Warning for Security Exposure Management integration plugin to ingest threat intelligence and enrich your vulnerability database with pre-disclosure threat signals.
-   **[View Early Warning for Security Exposure Management integration health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/view-armis-early-warning-health.md)**  
Monitor the Early Warning for Security Exposure Management integration by reviewing run history, ingestion performance, and processing health from the Security Exposure Management Administration console.
-   **[Add Early Warning criteria to a risk rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/add-armis-early-warning-risk-rule.md)**  
Add the Early Warning flag or Admiralty score as a weighted criterion in a risk rule to prioritize vulnerable items based on threat intelligence data.
-   **[Early Warning CVD Attributes field reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/r-early-warning-cvd-attributes.md)**  
The Early Warning CVD Attributes table stores threat intelligence signals for vulnerabilities. Each attribute represents a pre-disclosure threat indicator ingested from the Early Warning feed.

**Parent Topic:**[Unified Security Exposure Management integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/integrating-usem.md)

**Related topics**  


[Integrations for Central Vulnerability Database](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-response/cvd-integrations-overview.md)

[Security Exposure Management Workspace List view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-workspace-list-page.md)

[Define fields and weights for the risk rule for Unified Security Exposure Management risk calculators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-vuln-calc-define-risk-rule-fields.md)

