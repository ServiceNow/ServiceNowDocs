---
title: How Fix Intelligence for Security Exposure Management works
description: Fix Intelligence for Security Exposure Management enriches your host findings with normalized fix information and stores each unique fix as a Fix record. The feature links every fix to the findings it resolves and rolls up a risk score per fix. Your team can remediate by fix instead of one finding at a time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/fix-intel-data-flow.html
release: australia
topic_type: concept
last_updated: "2026-08-03"
reading_time_minutes: 3
keywords: [Fix Intel, Fix Intelligence, ViPR, remediation, Security Exposure Management]
breadcrumb: [Exploring Fix Intelligence for SEM, Fix Intelligence for Security Exposure Management, Integrate, Unified Security Exposure Management, Security Operations]
---

# How Fix Intelligence for Security Exposure Management works

Fix Intelligence for Security Exposure Management enriches your host findings with normalized fix information and stores each unique fix as a Fix record. The feature links every fix to the findings it resolves and rolls up a risk score per fix. Your team can remediate by fix instead of one finding at a time.

Fix Intelligence for Security Exposure Management connects Armis Centrix™ for Vulnerability Prioritization and Remediation \(ViPR\) to Unified Security Exposure Management. Instead of surfacing one vulnerability at a time, it consolidates the remediation actions that resolve those vulnerabilities into de-duplicated Fix records. It maps each fix to the findings and assets it affects and prioritizes fixes by an aggregate risk score.

## How fixes are identified

Fix Intelligence for SEM relies on the normalization and deduplication capability of Armis Centrix™ for ViPR to identify a normalized fix for each vulnerability detection. The data moves through the following stages:

1.  **Detections are ingested**: Your vulnerability integrations bring detections from your scanners into USEM as findings.
2.  **Detections are consumed for normalization**: Armis Centrix™ for ViPR consumes the scanner detection data from your instance through the Integration Sync API.
3.  **Fixes are identified**: Armis Centrix™ for ViPR normalizes and de-duplicates the detections and identifies a fix for each one.
4.  **Fixes are stored and linked**: USEM retrieves the identified fixes and stores them as Fix records, linked to the findings each fix resolves.
5.  **Risk is rolled up**: Each fix receives a risk score, a findings count, and a distinct-assets count, calculated from the active findings that share the fix. For more information on roll-up calculators, see [Vulnerability Response Rollup Calculators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-vuln-rollup-calculator.md).

In this release, fixes are identified for host vulnerabilities \(host vulnerable items\) from the Qualys, Rapid7, Tenable.io, Wiz, and Microsoft Defender Vulnerability Management integrations.

## Where fixes appear

After fixes are identified, they are available as a list and form in Unified Security Exposure Management Workspace, and as widgets on the **Findings View** and the **Remediation View** — for example, **Findings with fix identified** and **Top fixes by finding count**. Each finding also shows a read-only **Fix** reference linking to the fix that resolves it. To learn how to read and act on this data, see [View fixes in USEM Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/view-fixes-in-workspace.md) and [Prioritize remediation by fix](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/prioritize-remediation-by-fix.md).

**Parent Topic:**[Exploring Fix Intelligence for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/exploring-fix-intel.md)

**Related topics**  


[Fix Intelligence for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/fix-intel-for-usem-landing.md)

[Exploring Fix Intelligence for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/exploring-fix-intel.md)

