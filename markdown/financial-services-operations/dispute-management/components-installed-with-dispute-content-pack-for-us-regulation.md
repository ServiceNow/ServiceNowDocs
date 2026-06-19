---
title: Components installed with Dispute Content Pack for US Regulations
description: The Dispute Content Pack for US Regulations plugin installs components such as SLAs and additional plugins.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/components-installed-with-dispute-content-pack-for-us-regulation.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
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

## Service Level Agreement \(SLA\) definitions installed

The following SLA definitions are preconfigured with Dispute Content Pack for US Regulations.

**Note:** Billing cycle date and Statement date are retrieved from core banking integrations.

SLA durations are calculated from key regulatory dates — primarily the dispute reported date, and, for Reg Z, the statement date and billing cycle date. When a task is created after the dispute is reported \(for example, provisional credit\), the elapsed time between the reported date and task creation is accounted for so the SLA still reflects the regulatory window.

<table id="table_w3s_lxz_zbc"><thead><tr><th>

SLA

</th><th>

Table \[name\]

</th><th>

SLA duration

</th></tr></thead><tbody><tr><td>

Reg E 10day provisional limit

</td><td>

Card Disputes Task \[sn\_bom\_credit\_card\_disputes\_task\]

</td><td>

10 days minus &lt;Days elapsed between dispute reported date and task creation date&gt;

</td></tr><tr><td>

Reg E 20day provisional limit

</td><td>

Card Disputes Task \[sn\_bom\_credit\_card\_disputes\_task\]

</td><td>

20 days minus &lt;Days elapsed between dispute reported date and task creation date&gt;

</td></tr><tr><td>

Reg E 45day resolution limit

</td><td>

Card Disputes Service Case\[sn\_bom\_credit\_card\_disputes\_service\]

</td><td>

45 days from dispute reported date

</td></tr><tr><td>

Reg E 90day resolution limit

</td><td>

Card Disputes Service Case\[sn\_bom\_credit\_card\_disputes\_service\]

</td><td>

90 days from dispute reported date

</td></tr><tr><td>

Reg E acknowledgement limit

</td><td>

Card Disputes Service Case\[sn\_bom\_credit\_card\_disputes\_service\]

</td><td>

10 days from dispute reported date

</td></tr><tr><td>

Reg E PC reversal limit

</td><td>

Card Disputes Task \[sn\_bom\_credit\_card\_disputes\_task\]

</td><td>

5 days minus &lt;Days elapsed between dispute reported date and task creation date&gt;

</td></tr><tr><td>

Reg Z acknowledgement limit

</td><td>

Card Disputes Service Case\[sn\_bom\_credit\_card\_disputes\_service\]

</td><td>

30 days, starts from dispute reported date \(stops when Acknowledgement is marked "yes"\)

</td></tr><tr><td>

Reg Z resolution limit

</td><td>

Card Disputes Service Case\[sn\_bom\_credit\_card\_disputes\_service\]

</td><td>

Starts from dispute reported date. Two complete billing cycles, no later than 90 calendar days from date of notice.

</td></tr></tbody>
</table>**Parent Topic:**[Dispute Content Pack for US Regulations reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/dispute-content-pack-for-us-regulation-reference.md)

