---
title: Exploring Fix Intelligence for Security Exposure Management
description: Fix Intelligence for Security Exposure Management enriches USEM with a de-duplicated catalog of remediation actions, each linked to the findings and assets it resolves and scored by the risk it removes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/exploring-fix-intel.html
release: zurich
topic_type: concept
last_updated: "2026-07-29"
reading_time_minutes: 3
keywords: [Fix Intel, Fix Intelligence, remediation, Armis]
breadcrumb: [Fix Intelligence for Security Exposure Management, Integrations, Unified Security Exposure Management, Security Operations]
---

# Exploring Fix Intelligence for Security Exposure Management

Fix Intelligence for Security Exposure Management enriches USEM with a de-duplicated catalog of remediation actions, each linked to the findings and assets it resolves and scored by the risk it removes.

Vulnerability teams often work finding by finding, even when a single patch or configuration change resolves many findings across many assets. Fix Intelligence for Security Exposure Management identifies fix information for your detections and turns it into Fix records. These records group findings under the action that resolves them, so you can plan and prioritize remediation by fix.

Vulnerability detections that USEM ingests from your scanners are processed by Armis Centrix™ for Vulnerability Prioritization and Remediation \(ViPR\), which identifies and normalizes a fix for each detection. Because fixes are normalized and de-duplicated, a single Fix record can represent the same remediation action across many detections, assets, and scanners.

## Supported integrations

In this release, Fix Intelligence for SEM identifies fixes for host vulnerabilities \(host vulnerable items\) ingested from the following integrations:

-   Qualys
-   Rapid7
-   Tenable.io
-   Wiz
-   Microsoft Defender Vulnerability Management

## Features

-   **De-duplicated fix catalog**

    Each remediation action is stored once as a Fix record, no matter how many detections or scanners report it, with its remediation category \(for example, Patch Update, OS Update, or Configuration Change\), affected software, and a rolled-up risk score.

-   **Finding and asset linkage**

    Every fix is linked to the vulnerable items it resolves, and each finding carries a read-only reference back to its fix.

-   **Per-fix risk rollup**

    A rollup calculator scores each fix from the active findings that share it, and maintains a findings count and a distinct-assets count so you can size the impact of applying the fix.

-   **Automated exchange with Armis Centrix™ for ViPR**

    USEM exports detection data to Armis Centrix™ for ViPR and retrieves the identified fixes on a schedule, keeping the catalog current without manual imports.

-   **Workspace and dashboard visibility**

    Fixes appear as a list and form in Unified Security Exposure Management Workspace, and as widgets on the **Findings View** and the **Remediation View** — for example, **Findings with fix identified** and **Top fixes by finding count**.


## Who uses Fix Intelligence for SEM

|User|Goal|
|----|----|
|Vulnerability analyst|Find the fixes that resolve the most findings and highest risk, then act on them first.|
|Vulnerability manager|See which assets a fix covers, and coordinate the patch or configuration change across the assigned remediation teams.|
|Remediation Owner|Navigate to the fix list and see other findings if they are assigned to them.|

## Benefits

-   **Remediate by fix, not by finding**: One fix can clear many findings across many assets, reducing repetitive work.
-   **Prioritize by risk removed**: The per-fix risk rollup surfaces the fixes that reduce the most exposure.
-   **Stay current automatically**: Scheduled exchanges keep the fix catalog aligned with Armis Centrix™ for ViPR.

## What next

-   [How Fix Intelligence for Security Exposure Management works](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/fix-intel-data-flow.md)

-   [Install Fix Intelligence for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/install-fix-intel.md)


-   **[How Fix Intelligence for Security Exposure Management works](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/fix-intel-data-flow.md)**  
Fix Intelligence for Security Exposure Management enriches your host findings with normalized fix information and stores each unique fix as a Fix record. The feature links every fix to the findings it resolves and rolls up a risk score per fix. Your team can remediate by fix instead of one finding at a time.

**Parent Topic:**[Fix Intelligence for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/fix-intel-for-usem-landing.md)

**Related topics**  


[Exploring Unified Security Exposure Management \(USEM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/exploring-unified-security-exposure-management.md)

