---
title: Currency conversion and third-party total expense aggregation
description: During report generation, the Register of Information \(RoI\) can standardize contract annual expenses by converting amounts to a base currency and aggregating totals per eligible third-party provider or engagement. The RoI is a regulatory reporting requirement under the Digital Operational Resilience Act \(DORA\) and is supported by the Digital Resilience Third-party Information Register application in the Vendor Management Workspace application.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-02-11"
reading_time_minutes: 3
keywords: [DORA, Register of Information, currency conversion, ECB exchange rates, third-party aggregation, Plain-CSV reporting package]
breadcrumb: [Use digital resilience third-party registers, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Currency conversion and third-party total expense aggregation

During report generation, the Register of Information \(RoI\) can standardize contract annual expenses by converting amounts to a base currency and aggregating totals per eligible third-party provider or engagement. The RoI is a regulatory reporting requirement under the Digital Operational Resilience Act \(DORA\) and is supported by the Digital Resilience Third-party Information Register application in the Vendor Management Workspace application.

## Currency and aggregation overview

The DORA Register of Information Digital Resilience Third-party Information Register provides two optional features during report generation: currency conversion and third-party total expense aggregation. These features standardize and consolidate annual expense data in the Plain-CSV reporting package and the Excel Master Template.

You enable these options per export request on the Excel download/upload request page when generating an Excel Master Template or a Plain-CSV Reporting Package. Both features are disabled by default and apply only to exported reports, not to the underlying contract or third-party records.

Administrators maintain the currency rates and validation rules. Currency rates populate automatically using a daily scheduled job once the instance is activated. Administrators or DORA administrators can update currency rates and validation rules to align with regulator requirements by navigating to **All** &gt; **Digital Operational Resilience Management** &gt; **Digital Resilience Choices** or **DPM Business Validation Rules**.

## Currency conversion

Currency conversion converts each contract’s annual expense into a single base currency using historical exchange rates from the European Central Bank \(ECB\). The Reference Date on the report determines which exchange rate is used. Converted amounts appear only in the generated reporting package; source records remain unchanged.

Enable conversion when contracts span multiple currencies, when reporting requires a standardized currency, or when you plan to aggregate provider totals but contract currencies are inconsistent. Disable it when all amounts already use the base currency or when preserving original currencies is required.

When conversion is enabled, the system produces a Currency Conversion Summary Report and, if any conversion fails \(for example, because a rate is unavailable or a currency code is invalid\), a Currency Conversion Detail Report.

General guidelines:

-   Set the Reference Date to the last day of the reporting period \(for example, 2025‑12‑31\).
-   Ensure ECB exchange rates are available in the platform for the selected date.
-   Validate results with a small test export before running large data sets.

**Note:** If a conversion fails for a contract, the original currency and amount are retained for that contract in the exported output.

## Third-party total expense aggregation

Aggregation consolidates annual expenses across all contracts that belong to the same third-party provider or third-party engagement. The result appears as a single combined value in the exported reporting output. Aggregation runs only when all eligibility criteria for a provider are satisfied.

Eligibility rules:

-   Contract structure: Certain contract configurations, such as multi-provider contracts, can make a provider ineligible for aggregation \(for example, when split ratios are not defined\).
-   Currency alignment: All contract amounts must be in the base currency or successfully converted.
    -   If conversion is enabled, every required conversion must succeed.
    -   If conversion is disabled, all contracts must already use the base currency.

If aggregation is disabled on the request or if any eligibility rule is not met, the system reports manual entry values for that provider. Manual entry serves as the fallback for providers that do not aggregate.

When aggregation is enabled, the system produces an Aggregation Summary Report and, when providers are ineligible, a Skipped Contracts Detail Report explaining why aggregation did not occur.

**Important:** Keep manual entry values current for providers that may not qualify for aggregation.

## Relationship between conversion and aggregation

Currency conversion and aggregation operate independently but can be combined. Successful conversion can enable aggregation when a provider’s contracts use different currencies. Any failed conversion for a provider prevents aggregation for that provider.

## Reports and exports

When you generate a Plain-CSV reporting package, the platform produces a ZIP package structured to regulator specifications, containing the required CSV files and supporting metadata.

When enabled, the package also includes consolidated reports that summarize currency conversion results, aggregation outcomes, and validation findings.

Conversion-related reports appear only when currency conversion is enabled. Aggregation-related reports appear only when aggregation is enabled.

**Related topics**  


[Convert and aggregate contractual expenses to regulator-required currencies](../task/tprm-create-report-aggregate-expenses.md)

[Register of information regulatory packages](tprm-dora-roi.md)

