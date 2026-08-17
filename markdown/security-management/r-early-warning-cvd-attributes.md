---
title: Early Warning CVD Attributes field reference
description: The Early Warning CVD Attributes table stores vulnerability intelligence signals for vulnerabilities. Each attribute represents a threat indicator ingested from the Early Warning feed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/r-early-warning-cvd-attributes.html
release: zurich
topic_type: reference
last_updated: "2026-06-23"
reading_time_minutes: 2
keywords: [Early Warning, CVD attributes, field reference, threat intelligence, schema]
breadcrumb: [Early Warning for Security Exposure Management, Integrations, Unified Security Exposure Management, Security Operations]
---

# Early Warning CVD Attributes field reference

The Early Warning CVD Attributes table stores vulnerability intelligence signals for vulnerabilities. Each attribute represents a threat indicator ingested from the Early Warning feed.

Early warning threat signals are stored in the Armis Early Warning CVD Attributes \[sn\_vul\_ew\_cvd\_attributes\] table, a specialized extension table for vulnerability attributes. Each record in this table represents a unique CVE and stores the set of vulnerability intelligence attributes ingested from Armis.

## Attribute fields

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CVE ID

</td><td>

Identifier of the CVE record, such as `CVE-2026-33824`.

</td></tr><tr><td>

CWE

</td><td>

Common Weakness Enumeration identifier associated with the CVE, such as `CWE-415`.

</td></tr><tr><td>

Date Added

</td><td>

Date and time when this CVE was added to the Armis Early Warning dataset.

</td></tr><tr><td>

Intel Date

</td><td>

Date and time when Armis first obtained intelligence about this CVE.

</td></tr><tr><td>

Admiralty Score

</td><td>

NATO grading system for vulnerability intelligence confidence and reliability. Scores range from A1 \(highest confidence\) to F6 \(lowest confidence\). Use this score to assess the credibility of associated threat signals.

</td></tr><tr><td>

Vendor/Project

</td><td>

Name of the vendor or project associated with the affected software.

</td></tr><tr><td>

Research Date

</td><td>

Date when academic or security research was published that details the vulnerability, its impact, or exploitation techniques.

</td></tr><tr><td>

Honeypot Date

</td><td>

Date and time when honeypot systems recorded exploit activity against this CVE. A honeypot is a decoy system deliberately exposed to attackers. This field is empty when no honeypot activity has been observed.

</td></tr><tr><td>

Product

</td><td>

Name of the specific product affected by the CVE, such as `Windows 10 1607`.

</td></tr><tr><td>

Notification Date

</td><td>

Date and time when ServiceNow received notification of this CVE from Armis.

</td></tr><tr><td>

Updated On

</td><td>

Date and time when this record was last updated in ServiceNow.

</td></tr><tr><td>

Enabled

</td><td>

Option to indicate whether this CVE record is active and included in risk scoring and downstream processing.

</td></tr><tr><td>

Special

</td><td>

Option to flag this CVE as a special case for further review or custom handling.

</td></tr><tr><td>

Summary Note

</td><td>

Free-text summary describing the intelligence gathered for this CVE, including the source of the information and the basis for the admiralty score.

</td></tr><tr><td>

External Note

</td><td>

Structured free-text field containing sub-categories of intelligence detail: Intel Source, Honeypot, Research, Detection, Vulnerable, Malware hash, Analyst note, Intel note, and Admiralty score. Values are reported as `NA` when no data is available for a sub-category.

</td></tr></tbody>
</table>**Parent Topic:**[Early Warning for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/armis-early-warning-integration.md)

