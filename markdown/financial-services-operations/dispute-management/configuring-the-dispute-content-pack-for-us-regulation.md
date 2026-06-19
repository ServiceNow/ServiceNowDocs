---
title: Configuring the Dispute Content Pack for US Regulations
description: Dispute Content Pack for US Regulations includes predefined Service Level Agreement \(SLA\) definitions that align with Regulation E and Regulation Z. SLA durations are calculated from key dates such as the dispute reported date, task creation date, statement date, and billing cycle date.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/configuring-the-dispute-content-pack-for-us-regulation.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Dispute Content Pack for US Regulations, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Configuring the Dispute Content Pack for US Regulations

Dispute Content Pack for US Regulations includes predefined Service Level Agreement \(SLA\) definitions that align with Regulation E and Regulation Z. SLA durations are calculated from key dates such as the dispute reported date, task creation date, statement date, and billing cycle date.

## Service Level Agreement definitions

Dispute Content Pack for US Regulations contains several predefined SLA definitions in accordance with Regulation E \(Reg E\) and Regulation Z \(Reg Z\).

SLA definitions can be found in your instance by navigating to **All** &gt; **Service Level Management** &gt; **SLA** &gt; **SLA Definitions**.

SLA durations are calculated based on one or more of the following dates:

-   Dispute reported date
-   Task creation date
-   Statement date
-   Billing cycle date

**Note:** Billing cycle date and Statement date are retrieved from core banking integrations.

SLA durations are calculated from key regulatory dates — primarily the dispute reported date, and, for Reg Z, the statement date and billing cycle date. When a task is created after the dispute is reported \(for example, provisional credit\), the elapsed time between the reported date and task creation is accounted for so the SLA still reflects the regulatory window.

For a full list of the predefined SLA definitions in Dispute Content Pack for US Regulations and their respective duration formulas, see [Service Level Agreement \(SLA\) definitions installed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/components-installed-with-dispute-content-pack-for-us-regulation.md).

**Parent Topic:**[Dispute Content Pack for US Regulations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/dispute-content-pack-for-us-regulation-landing-page.md)

