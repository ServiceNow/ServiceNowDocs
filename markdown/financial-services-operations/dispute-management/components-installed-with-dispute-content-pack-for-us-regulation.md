---
title: Components installed with Dispute Content Pack for US Regulations
description: The Dispute Content Pack for US Regulations plugin installs components such as SLAs and additional plugins.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Dispute Content Pack for US Regulations, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Components installed with Dispute Content Pack for US Regulations

The Dispute Content Pack for US Regulations plugin installs components such as SLAs and additional plugins.

## Plugins installed

**Note:** The Dispute Content Pack for US Regulations application is dependent on the Financial Services Card Operations application.

|Plugin|Description|
|------|-----------|
|Financial Services Card Operations \[com.sn\_bom\_credit\_card\]|Enables quick processing of credit card applications and card transaction disputes.|
|Dispute Content Pack for US Regulations \[sn\_disp\_reg\_cp\_us\]|Enables issuers in the United States \(US\) to track dispute cases and conform with regulatory guidelines.|

## Tables installed

The Dispute Content Pack for US Regulations application includes no new tables.

## Decision tables

|Decision table|Description|
|--------------|-----------|
|Reg E resolution days |Determines the Reg E resolution days for a case. The default duration is set to 45 days.|

## Service Level Agreement \(SLA\) definitions installed

The following SLA definitions are added with Dispute Content Pack for US Regulations.

<table id="table_w3s_lxz_zbc"><thead><tr><th>

SLA

</th><th>

Table \[name\]

</th></tr></thead><tbody><tr><td>

Reg E 10day provisional limit

</td><td>

Card Disputes Task \[sn\_bom\_credit\_card\_disputes\_task\]

</td></tr><tr><td>

Reg E 20day provisional limit

</td><td>

Card Disputes Task \[sn\_bom\_credit\_card\_disputes\_task\]

</td></tr><tr><td>

Reg E 45day resolution limit

</td><td>

Card Disputes Service Case\[sn\_bom\_credit\_card\_disputes\_service\]

</td></tr><tr><td>

Reg E 90day resolution limit

</td><td>

Card Disputes Service Case\[sn\_bom\_credit\_card\_disputes\_service\]

</td></tr><tr><td>

Reg E acknowledgement limit

</td><td>

Card Disputes Service Case\[sn\_bom\_credit\_card\_disputes\_service\]

</td></tr><tr><td>

Reg E PC reversal limit

</td><td>

Card Disputes Task \[sn\_bom\_credit\_card\_disputes\_task\]

</td></tr><tr><td>

Reg Z acknowledgement limit

</td><td>

Card Disputes Service Case\[sn\_bom\_credit\_card\_disputes\_service\]

</td></tr><tr><td>

Reg Z resolution limit

</td><td>

Card Disputes Service Case\[sn\_bom\_credit\_card\_disputes\_service\]

</td></tr></tbody>
</table>**Parent Topic:**[Dispute Content Pack for US Regulations reference](../concept/dispute-content-pack-for-us-regulation-reference.md)

