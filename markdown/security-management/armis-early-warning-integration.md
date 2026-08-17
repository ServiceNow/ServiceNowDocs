---
title: Early Warning for Security Exposure Management
description: Early Warning for Security Exposure Management, powered by Armis, enriches the Central Vulnerability Database \(CVDB\) in Unified Security Exposure Management \(USEM\) with vulnerability intelligence of imminent exploit. This enables your security team to prioritize and patch vulnerabilities before threat actors weaponize them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/armis-early-warning-integration.html
release: zurich
topic_type: concept
last_updated: "2026-06-24"
reading_time_minutes: 8
keywords: [Armis Early Warning, CVE enrichment, vulnerability intelligence, Security Exposure Management]
breadcrumb: [Integrations, Unified Security Exposure Management, Security Operations]
---

# Early Warning for Security Exposure Management

Early Warning for Security Exposure Management, powered by Armis, enriches the Central Vulnerability Database \(CVDB\) in Unified Security Exposure Management \(USEM\) with vulnerability intelligence of imminent exploit. This enables your security team to prioritize and patch vulnerabilities before threat actors weaponize them.

Early Warning assesses vulnerability intelligence through honeypot activity, open-source research, and operational threat analysis, flagging which vulnerabilities pose immediate risk to your environment. This enrichment helps your team reduce noise and prioritize what truly matters, while accelerating remediation and coordinate patching efforts within your existing vulnerability management workflows.

## When Early Warning matters

Early Warning shifts vulnerability management from reactive crisis to proactive defense, providing strategic advantage by detecting which vulnerabilities threat actors are actively trying to exploit.

**Without early warning**: When security teams rely primarily on severity, all critical and high-severity vulnerabilities may appear to require immediate attention. This can create noise, stretch remediation teams, and make it difficult to determine which vulnerabilities pose the most urgent risk to the organization.

**With early warning**: Early Warning enriches Common Vulnerabilities and Exposures \(CVE\) records with vulnerability intelligence derived from signals such as honeypot activity, OSINT, and operational research. When the Early Warning flag is set to **true**, teams can focus first on critical vulnerabilities with evidence of active exploitation or heightened attacker interest, rather than treating every critical or high-severity vulnerability the same. This additional context helps teams reduce noise, prioritize what matters most, validate fixes, coordinate patching across teams and regions, and deploy updates through planned maintenance windows instead of relying only on reactive emergency remediation.

**When Early Warning Is critical**: Early Warning is most valuable for organizations where patching takes time or downtime is costly:

-   **Legacy systems and industrial controls \(ICS/SCADA\)**: Systems that can't be rebooted quickly or easily patched. Early warning provides time for safe, planned updates instead of emergency changes that risk production downtime.
-   **Healthcare systems**: Patient care equipment and Electronic Health Record \(EHR\) systems require validation before patching. Early warning allows time to coordinate updates during low-patient-census windows without disrupting care.
-   **Manufacturing and operations**: Downtime costs millions per hour. Early warning allows time to plan patches during scheduled maintenance windows instead of emergency shutdowns.
-   **Financial services and payment systems**: Patch windows are scheduled in advance. Early warning ensures patches are tested and ready to deploy when the window arrives, instead of scrambling on the deployment day.
-   **Multi-region enterprises**: Complex environments with factories, offices, or data centers across regions take time to coordinate. Early warning provides the runway to test and deploy across all sites safely.
-   **Regulated industries**: Compliance auditors want to see proactive vulnerability management, not reactive patch-and-pray. Early warning demonstrates a prevention-first security posture.
-   **High-value targets**: Organizations subject to nation-state or sophisticated cyber attacks. Early warning closes the window where you're undefended before threat actors act.

Detecting exploitation signals from honeypots, OSINT, and operational research before broader industry recognition or CISA KEV inclusion enables proactive patching and reduces the need for high-risk emergency updates.

## How it works

Early Warning for Security Exposure Management performs the following operations when integrated with USEM:

-   **Detection**: Identifies a vulnerability that threat actors are planning to exploit.
-   **Integration**: Ingests early warning signal automatically ingested into USEM and elevates the priority of that CVE in your vulnerability inventory.
-   **Prioritization**: Enables your security team to prioritize patching these vulnerabilities ahead of others, even if Common Vulnerability Scoring System \(CVSS\) scores don't reflect the real-world threat.
-   **Response**: Enables your team to coordinate proactive patch deployment during planned maintenance windows and focus on vulnerabilities threat actors are actively targeting - not just those with the highest CVSS scores.

The integration appears in the Security Exposure Management workspace alongside other enrichment integrations such as the CISA Known Exploited Vulnerabilities integration. You can monitor integration run history, ingestion health, and processing health from the integration overview page.

## Key benefits

Early Warning for Security Exposure Management provides the following benefits:

-   **Earlier risk prioritization**: Early warning flags surface alongside your vulnerability risk scores, so remediation teams focus on the threats that matter most. Instead of patching by CVSS score alone, you patch based on real-world threat actor behavior.
-   **Faster remediation without extra setup**: Early warning CVEs trigger existing Vulnerability Change Management workflows automatically, with no custom integration required.
-   **Faster identification of at-risk assets**: Filter findings by early warning status to surface which assets carry elevated risk.
-   **Built-in asset correlation**: Early Warning signals roll up from CVE records to third-party entries \(TPEs\) automatically, extending risk visibility to the assets already tracked in USEM with no additional CMDB mapping required.

## Data available in USEM

When you integrate Early Warning for Security Exposure Management, two new columns appear in your vulnerability records:

-   **Armis Early Warning:** A flag indicating that threat actors are planning to exploit this CVE.
-   **Armis Early Warning CVD Attributes:** Detailed vulnerability intelligence including:
    -   CVE ID and affected product
    -   Intelligence date \(when Armis detected the threat actor activity\)
    -   Admiralty score \(confidence rating of the vulnerability intelligence\)
    -   Honeypot detection date
    -   Research date

You can use these columns to filter, sort, and prioritize your vulnerability remediation workflow.

The integration appears in the Security Exposure Management workspace alongside other enrichment integrations, such as CISA Known Exploited Vulnerabilities. From the integration overview page, you can monitor run history, ingestion health, and processing status. For more information, see [Security Exposure Management Workspace List view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-workspace-list-page.md)

## Admiralty score

Each CVE in the Armis feed includes an Admiralty score - a confidence rating based on the NATO Admiralty grading system. Scores range from A1–A6, B1–B6, C1–C6, D1–D6, E1–E6, and F1–F6, where A1 represents information from a completely reliable source that has been independently corroborated. A lower confidence rating does not prevent a CVE from being identified as an early warning signal. CVEs with lower Admiralty scores may still be surfaced when other factors indicate potential relevance or risk.

You can use the Admiralty score as an additional condition in a risk rule to refine prioritization. For example, you can configure the rule to apply a weight only to CVEs whose admiralty score meets a defined reliability threshold.

## Configuring risk rules

The early warning flag and Admiralty score are available as criteria in your risk rules, allowing you to configure how early warnings influence your vulnerability scores.

In the default risk calculator, you can:

-   Adjust the weight applied to early warning CVEs
-   Add Admiralty score as an additional condition for refinement
-   Create custom rules that combine early warning signals with other risk criteria

In the default risk calculator, you can adjust the weight or add the admiralty score as an additional condition to refine prioritization.

Early Warning extends risk coverage to CVEs which may not yet be identified by intelligence sources such as CISA KEV or EPSS.

## Key components

Early Warning for Security Exposure Management consists of the following components:

-   **Integration plugin**

    Early Warning for Security Exposure Management \(`sn_vul_ew`\): Handles data ingestion via the Vulnerability Integration Framework

-   **CVD attributes table**

    `sn_vul_ew_cvd_attributes`: Stores early warning-specific threat signals \(admiralty score, honeypot date, intelligence date, research date, CWE\)

-   **Flag rollup**

    Business rules propagate `ew_exists` flag from NVD entries to third-party entries for consolidated risk assessment

-   **Risk calculator field**

    `vulnerability.ew_exists`: Boolean risk criteria available for custom risk rule weighting


## Dependencies and prerequisites

The Early Warning for Security Exposure Management integration requires the following:

-   Unified Security Exposure Management \(Vulnerability Response v30.x\)
-   Vulnerability Integration Framework plugin
-   Access to Armis vulnerability intelligence feed and valid authentication credentials

-   **[Install the required applications for Early Warning for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/early-warning-install.md)**  
Install the required applications for Early Warning for Security Exposure Management.
-   **[Set up requirements for Early Warning for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/early-warning-integration-setup.md)**  
Complete the following setup steps in your Armis Intelligence Center console environment before you configure Early Warning for Security Exposure Management in your ServiceNow AI Platform® instance.
-   **[Configure the Early Warning for Security Exposure Management integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/t-configure_early_warning_integration.md)**  
Install and configure the Early Warning for Security Exposure Management integration plugin to ingest vulnerability intelligence and enrich your vulnerability database with threat signals.
-   **[Add Early Warning criteria to a risk rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/add-armis-early-warning-risk-rule.md)**  
Add the Early Warning flag or Admiralty score as a weighted criterion in a risk rule to prioritize vulnerable items based on vulnerability intelligence data.
-   **[Schedule the Early Warning for Security Exposure Management integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/schedule-ew-integration.md)**  
You can schedule the integration import times on the records in the Vulnerability Integrations \[sn\_vul\_int\_fw\_integration\] table and launch them on-demand.
-   **[View Early Warning for Security Exposure Management integration health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/view-armis-early-warning-health.md)**  
Monitor the Early Warning for Security Exposure Management integration by reviewing run history, ingestion performance, and processing health from the Security Exposure Management Administration console.
-   **[Early Warning CVD Attributes field reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/r-early-warning-cvd-attributes.md)**  
The Early Warning CVD Attributes table stores vulnerability intelligence signals for vulnerabilities. Each attribute represents a threat indicator ingested from the Early Warning feed.

**Parent Topic:**[Unified Security Exposure Management integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/integrating-usem.md)

**Related topics**  


[Integrations for Central Vulnerability Database](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/vulnerability-response/cvd-integrations-overview.md)

[Security Exposure Management Workspace List view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-workspace-list-page.md)

[Define fields and weights for the risk rule for Unified Security Exposure Management risk calculators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/sem-vuln-calc-define-risk-rule-fields.md)

