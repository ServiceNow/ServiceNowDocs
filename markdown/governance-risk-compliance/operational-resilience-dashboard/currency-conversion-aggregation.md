---
title: Currency conversion and third-party aggregation
description: Beginning with Digital Operational Resilience Management \(sn\_dora\_accel\), version 22.x.x, currency conversion and third-party aggregation capabilities are supported for DORA reporting of third-party expenses. As a DORA application user, you can convert and aggregate contractual expenses from multiple currencies to a regulator-required designated base currency using automated daily exchange rates.
locale: en-US
release: australia
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Digital resilience third-party registers, Maintaining Digital resilience third-party registers, Managing Operational Resilience, Operational Resilience, Governance, Risk, and Compliance]
---

# Currency conversion and third-party aggregation

Beginning with Digital Operational Resilience Management \(sn\_dora\_accel\), version 22.x.x, currency conversion and third-party aggregation capabilities are supported for DORA reporting of third-party expenses. As a DORA application user, you can convert and aggregate contractual expenses from multiple currencies to a regulator-required designated base currency using automated daily exchange rates.

## Supported capabilities

Currency conversion and third-party total expense aggregation are independently optional. You can enable either feature on its own or together, depending on your DORA reporting requirements. When both are enabled, aggregation uses the converted \(base-currency\) values.

**Note:** Raw \(un-rounded\) contract amounts are summed first across all contracts for a given provider; the total is then rounded to the nearest whole unit of base currency.

When creating an Excel download and upload request for DORA reporting, you can configure currency conversion and third-party aggregation settings to generate consolidated reports. Third-party aggregation consolidates expenses across multiple contracts associated with the same provider. You can enable both currency conversion and aggregation features independently as optional features, providing flexibility based on DORA reporting requirements.

When creating a Plain-CSV reporting package \(for regulatory submission\), the following fields are required in addition to the standard entity details: Competent authority \(for example, "CA"\), Reference date \(for example, 2025-12-31\), Date of reporting \(for example, 2026-01-28\).

## Report outputs

The application generates two types of reports to support regulatory conformance. The Primary download report provides Microsoft Excel based analysis, while the CSV package is designed for regulatory submission and includes Level 3 validation. Summary reports generated with both types display conversion and aggregation success or failure details with explanatory messages when issues occur. Currency conversion and aggregation apply to generated report outputs and do not modify underlying contract or third-party records.

## Currency rates and validation rules

Once you activate the instance, currency rates populate automatically via a daily scheduled job. Administrators or DORA administrators can update currency rates and validation rules to align with regulator requirements.

If specific date rates aren’t available, the system uses fallback default rates. The validation rules table must be maintained to stay current with regulatory requirements.

Administrator prerequisite: Before generating reports, a DORA administrator must verify two maintenance areas:

1.  DPM business validation rules table — must be kept current with regulator requirements; new rules can be added by the administrator without waiting for a platform release.
2.  System currency conversion rates table — populated automatically by a daily scheduled job once the instance is activated. Administrators can add historical rates via background script. If rates are unavailable for the reference date, the system falls back to default rates.

The following examples illustrate business validation rules and system currency conversion rates.

![Business validation rules.](../image/dora-validation-rules-table.png)![System currency conversion rates.](../image/dora-validation-rules-currency-rates.png)

## Related documentation

For information on creating a Microsoft Excel download and upload request and generating the reports, see [Create Microsoft Excel download and upload request](../task/create-excel-upload-download-request.md).

For steps on converting and aggregating contractual expenses to regulator-required currencies, see [Convert and aggregate contractual expenses to regulator-required currencies](../task/create-excel-report-aggregate-expenses.md).

-   **[Convert and aggregate contractual expenses to regulator-required currencies](../task/create-excel-report-aggregate-expenses.md)**  
Convert and aggregate contractual expenses to regulator-required currencies and generate consolidated reports for reporting submissions. Beginning with Digital Operational Resilience Management \(sn\_dora\_accel\), version 22.x.x, these currency conversion and third-party aggregation capabilities are supported for DORA reporting.

**Parent Topic:**[Using Digital resilience third-party registers](using-dg-registers.md)

