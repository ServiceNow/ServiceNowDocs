---
title: Components installed with Dispute Rules Content Pack for Nacha
description: Several types of components are installed with Dispute Rules Content Pack for Nacha.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Dispute Rules Content Pack for Nacha reference, Dispute Rules Content Pack for Nacha, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Components installed with Dispute Rules Content Pack for Nacha

Several types of components are installed with Dispute Rules Content Pack for Nacha.

## Plugins

**Note:** The Dispute Rules Content Pack for Nacha application is dependent on the Financial Services Card Operations application.

<table id="table_qmv_14w_5gc"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Financial Services Card Operations \[com.sn\_bom\_credit\_card\]

</td><td>

Used to reference dispute transactions and related disputes data.

</td></tr></tbody>
</table>## Tables

No tables are included with Dispute Rules Content Pack for Nacha. Chargeback reason codes are stored in Financial Services Operations Core.

## Dispute Reason Codes

Dispute Rules Content Pack for Nacha includes 10 reason codes and the predefined logic to determine if the codes apply to a disputed transaction.

|Reason code|Title|Timeframe|WSUD required|
|-----------|-----|---------|-------------|
|R05|Unauthorized Consumer Debit using Corporate SEC Code|60 days|Yes|
|R06|ODFI Requested Return|Not defined, determined by ODFI and RDFI|No|
|R07|Customer Revoked Authorization|60 days|Yes|
|R10|Originator not known and/or not authorized to Debit Receiver’s Account|60 days|Yes|
|R11|Customer advises not within Authorization Terms|60 days|Yes|
|R24|Duplicate Entry|2 banking days|No|
|R29|Not Authorized by Corporate Customer|2 banking days|No|
|R31|Permissible Return \(CCD and CTX only\)|Not defined, determined by the ODFI and RDFI|No|
|R37|Source Document Presented|60 days|Yes|
|R39|Improper Source Document|2 banking days|No|

**Parent Topic:**[Dispute Rules Content Pack for Nacha reference](dispute-rules-content-pack-nacha-reference.md)

