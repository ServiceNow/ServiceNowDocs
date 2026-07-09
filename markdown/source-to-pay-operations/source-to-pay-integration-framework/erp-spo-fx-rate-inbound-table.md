---
title: FX Rate Stage inbound staging table
description: The FX Rate Stage inbound \[sn\_fcms\_intg\_fx\_rate\_stage\] staging table temporarily stores important data about FX rates before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/erp-spo-fx-rate-inbound-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-07-01"
reading_time_minutes: 1
breadcrumb: [ERP Integration Framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# FX Rate Stage inbound staging table

The FX Rate Stage inbound \[sn\_fcms\_intg\_fx\_rate\_stage\] staging table temporarily stores important data about FX rates before this data is sent to the primary table.

The following table lists the fields for the FX Rate Stage inbound \[sn\_fcms\_intg\_fx\_rate\_stage\] staging table.

<table id="table_erp_spo_fx_rate_inbound_table"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Conversion date

</td><td>

String

</td><td>

Date of currency conversion.

</td></tr><tr><td>

ERP source

</td><td>

String

</td><td>

ERP source from which data is imported. For purchase order, receipt, and invoice integrations, the ERP source is determined through the legal entity associated with these records.This is a mandatory field.

</td></tr><tr><td>

Exchange rate

</td><td>

Floating point number

</td><td>

Rate of exchange for currency conversion.This is a mandatory field.

</td></tr><tr><td>

From currency

</td><td>

String

</td><td>

Currency that is imported from.This is a mandatory field.

</td></tr><tr><td>

Rate type

</td><td>

String

</td><td>

Specifies the type of exchange rate used for currency conversion.

</td></tr><tr><td>

Span end

</td><td>

String

</td><td>

End date for the FX rate schedule.

</td></tr><tr><td>

Span start

</td><td>

String

</td><td>

Start date for the FX rate schedule.

</td></tr><tr><td>

To currency

</td><td>

String

</td><td>

Currency that is imported to. This is a mandatory field.

</td></tr></tbody>
</table>