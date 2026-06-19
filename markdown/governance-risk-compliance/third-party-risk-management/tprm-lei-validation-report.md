---
title: Level 4 LEI Validation Report columns
description: The Level 4 LEI Validation Report \(Level4\_LEI\_Validation\_Report.csv\) is generated during Plain-CSV Reporting Package download and lists the validation result for each Legal Entity Identifier \(LEI\) code found in the reporting package.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-lei-validation-report.html
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: reference
last_updated: "2026-05-15"
reading_time_minutes: 4
keywords: [LEI validation, GLEIF, DORA, Level 4 LEI Validation Report]
breadcrumb: [Validate LEI codes, Validation framework for RoI, Use digital resilience third-party registers, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Level 4 LEI Validation Report columns

The Level 4 LEI Validation Report \(`Level4_LEI_Validation_Report.csv`\) is generated during Plain-CSV Reporting Package download and lists the validation result for each Legal Entity Identifier \(LEI\) code found in the reporting package.

The report is included in `Consolidated_Reports.zip` alongside the Level 3 DPM Validation Summary. It covers LEI codes sourced from the DORA reporting tables that contain LEI fields, including Legal entities \(B.01.02\), ICT third-party service providers \(B.05.01\), and other sheets where LEI codes appear. Each row in the report represents a single LEI code occurrence, ordered by sheet name and then row number.

For information on how to review and resolve validation results, see [Validate Legal Entity Identifier codes for DORA reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-valid-lei.md).

**Note:** Name, Country, Entity Status, and Registration Status values are derived from the GLEIF API response used during validation.

\[Omitted image "l4-lei-valid-ex.png"\] Alt text: Level 4 LEI Validation Report \(Level4\_LEI\_Validation\_Report.csv\)

<table id="table_lei_report_columns"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sheet Name

</td><td>

The DORA reporting table that contains the LEI code, for example, `b_01.02` or `b_05.01`.

</td></tr><tr><td>

Row Number

</td><td>

The row number of the LEI code within the generated CSV sheet. Use this value together with Sheet Name to locate the specific record in the reporting package.

</td></tr><tr><td>

Column

</td><td>

The column identifier within the source reporting table that contains the LEI code, for example, `c0010`. Use this value together with Sheet Name and Row Number to precisely locate the field.

</td></tr><tr><td>

LEI Code

</td><td>

The Legal Entity Identifier code that was validated, as stored in the digital resilience register.

</td></tr><tr><td>

LEI Format Valid

</td><td>

Indicates whether the LEI code meets the ISO 17442 format requirement: 20 characters, with the first 18 characters being uppercase alphanumeric and the last two being digits. Values: `Yes` or `No`. If No, the LEI is not sent to GLEIF for further validation.

</td></tr><tr><td>

LEI Checksum Valid

</td><td>

Indicates whether the LEI code passes the MOD 97-10 checksum as specified by ISO 17442. Values: `Yes` or `No`. If No, the Validation Result is Fail regardless of other results.

</td></tr><tr><td>

LEI Found

</td><td>

Indicates whether the LEI code exists in the GLEIF database. Values: `Yes`, `No`, or `N/A` \(when the GLEIF API was unavailable during validation\).

</td></tr><tr><td>

Entity Status

</td><td>

The entity registration status returned by GLEIF. Expected value for a valid LEI is `ACTIVE`. Other values include `INACTIVE` and `NULL` when the LEI is not found. `N/A` when the GLEIF API is unavailable.

</td></tr><tr><td>

Registration Status

</td><td>

The registration status returned by GLEIF. Expected value for a valid LEI is `ISSUED`. Other values include `LAPSED`, `RETIRED`, `PENDING_VALIDATION`, and `ANNULLED`. Empty when the LEI is not found. `N/A` when the API is unavailable.

</td></tr><tr><td>

Entity Name \(Input\)

</td><td>

The entity name as recorded in the digital resilience register for this LEI code.

</td></tr><tr><td>

Name \(GLEIF\)

</td><td>

The legal name returned by the GLEIF database for this LEI code. Empty when the LEI is not found. `N/A` when the API is unavailable.

</td></tr><tr><td>

Name Match

</td><td>

Indicates whether the entity name in the system matches the legal name returned by GLEIF for this LEI code. Values: `Match`, `No match`, or `N/A`. A mismatch results in a `Warning` rather than a `Fail`.

</td></tr><tr><td>

Country code \(Input\)

</td><td>

The country code as recorded in the digital resilience register for this LEI code.

</td></tr><tr><td>

Country code \(GLEIF\)

</td><td>

The country returned by the GLEIF database for this LEI code. For legal entities also appearing in B.01.02, this reflects the registered country. For third-party-only rows in B.05.01, this reflects the headquarters country. Empty when the LEI is not found. `N/A` when the API is unavailable.

</td></tr><tr><td>

Country Match

</td><td>

Indicates whether the country code in the system matches the country returned by GLEIF for this LEI code. Values: `Match`, `No match`, or `N/A`. A mismatch results in a `Warning` rather than a `Fail`.

</td></tr><tr><td>

Corroboration Level

</td><td>

The GLEIF corroboration level indicating how thoroughly the record has been verified against authoritative public sources. Values: `FULLY_CORROBORATED`: all mandatory fields verified; `PARTIALLY_CORROBORATED`: some fields verified; `ENTITY_SUPPLIED_ONLY`: data provided by the entity. This field does not affect the Validation Result.

</td></tr><tr><td>

Validation Result

</td><td>

The overall validation outcome for this LEI code. Values: `Pass`, `Warning`, `Fail`, or `N/A`. Validation logic:

-   `Fail`: Any of the following conditions apply: LEI Format Valid = No, LEI Checksum Valid = No, LEI Found = No, Entity Status is not ACTIVE, or Registration Status is not ACTIVE or ISSUED.
-   `Warning`: LEI is found and active/issued, but Name Match or Country Match is `No match`.
-   `Pass`: All validation checks pass and Name and Country match GLEIF data.
-   `N/A`: GLEIF API was unavailable during validation.

</td></tr><tr><td>

Validation Messages

</td><td>

A descriptive message explaining the validation result, for example, "LEI not found in GLEIF database" or "Entity name mismatch". Use this message to identify the issue and determine the required correction.

</td></tr></tbody>
</table>