---
title: Properties installed with Digital Operational Resilience Management
description: When you install the Digital Operational Resilience Management application, several system properties are added to your instance. You can access the properties by navigating to All &gt; Digital Operational Resilience Management &gt; Properties .
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/properties-dora.html
release: australia
topic_type: reference
last_updated: "2026-05-04"
reading_time_minutes: 2
breadcrumb: [Digital resilience third-party registers reference, Reference, Operational Resilience, Governance, Risk, and Compliance]
---

# Properties installed with Digital Operational Resilience Management

When you install the Digital Operational Resilience Management application, several system properties are added to your instance. You can access the properties by navigating to **All &gt; Digital Operational Resilience Management &gt; Properties** &gt; **.**

<table><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

HTTP timeout for GLEIF API calls \(sn\_dora\_accel.gleif\_api\_timeout\_ms\)

</td><td>

Property used for HTTP timeout in milliseconds for GLEIF API requests. Increase if requests are timing out due to network latency.

 Type: Integer

 Default value: 10,000 ms \(10 seconds\)

</td></tr><tr><td>

Max LEIs per GLEIF API request \(sn\_dora\_accel.gleif\_api\_batch\_size\)

</td><td>

Maximum number of LEIs per GLEIF API request. The GLEIF API supports a maximum of 200 per request. Lower this value to reduce individual request size.

 Type: Integer

 Default value: 200

</td></tr><tr><td>

Save LEI data on GLEIF validation error \(sn\_dora\_accel.lei\_save\_on\_gleif\_error\)

</td><td>

Controls whether records are saved when LEI validation fails against the GLEIF database.

 Type:

-   Yes \(default\): Records are saved with a warning message when the LEI is not found, the entity status is not active, or the registration status is not issued.
-   No: Records are blocked from saving for the above scenarios.

 A complete behavior matrix is shown in the "Behavior matrix for the upload path" table.

 **Note:**

This property governs the Excel upload path only. It does not affect whether records are saved when a GLEIF validation failure occurs on a UI form save \(UI form saves always allow the record to be saved regardless of this property; the client script displays a warning independently\). LEI format and checksum errors always block saving regardless of this property value, because those failures never reach the GLEIF API. When the GLEIF API is unreachable \(timeout or HTTP error\), saving is always allowed regardless of this property value.

</td></tr><tr><td>

decimalsInteger \(sn\_dora\_accel.decimals\_integer\)

</td><td>

Default number of decimal places for integer values.

 Set this to “0” unless regulatory requirements specify otherwise.

</td></tr><tr><td>

decimalsMonetary \(sn\_dora\_accel.decimals\_monetary\)

</td><td>

Decimal places for monetary values.

 Enter "-3" to round values to the nearest thousand \(for example, 123,456 becomes 123,000\).

</td></tr><tr><td>

report.json \(sn\_dora\_accel.report\_json\)

</td><td>

Configuration file for preparing the DORA plain CSV report.

 \{ "documentInfo": \{ "documentType": "https://xbrl.org/2021/xbrl-csv", "extends": \[ "http://www.eba.europa.eu/eu/fr/xbrl/crr/fws/dora/4.0/mod/dora.json" \] \}\}

</td></tr><tr><td>

reportPackage.json \(sn\_dora\_accel.report\_package\_json\)

</td><td>

Configuration file for preparing the DORA plain CSV reporting package. Regulatory reporting JSON schema URL.

 \{ "documentInfo": \{ "documentType": "https://xbrl.org/report-package/2023" \}\}

</td></tr><tr><td>

FrameworkCodeModuleVersion \(sn\_dora\_accel.framework\_code\_module\_version\)

</td><td>

Configuration for preparing the DORA plain-CSV reporting package. Framework code is DORA and the module version is from DORA reporting taxonomy. For example, module version 1.1.0 is formatted to 010100.

 Framework code and module version are used for naming the DORA plain-csv reporting package. For example, LEI123456789012.CON\_IT\_DORA010100\_DORA\_2025-03-31\_20250421141632000.zip

</td></tr></tbody>
</table>|Failure scenario|Property = Yes \(default\)|Property = No|
|----------------|--------------------------|-------------|
|LEI not found in GLEIF|Row saved with warning|Row blocked \(error\)|
|Entity status not ACTIVE|Row saved with warning|Row blocked \(error\)|
|Registration status not ISSUED|Row saved with warning|Row blocked \(error\)|
|LEI format invalid|Row blocked \(always\)|Row blocked \(always\)|
|LEI checksum invalid|Row blocked \(always\)|Row blocked \(always\)|
|GLEIF API unavailable|Row saved \(always\)|Row saved \(always\)|
|Name or country mismatch \(UI\)|Warning shown, save OK|Row blocked \(error\)|

**Parent Topic:**[Digital resilience third-party registers reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/digi-resi-ref.md)

