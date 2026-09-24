---
title: Components installed with Dispute Rules Content Pack for Visa
description: Several types of components are installed with the installation of the Dispute Rules Content Pack for Visa plugin.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/components-installed-with-dispute-rules-content-pack-for-visa.html
release: brazil
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Reference, Dispute Rules Content Pack for Visa, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Components installed with Dispute Rules Content Pack for Visa

Several types of components are installed with the installation of the Dispute Rules Content Pack for Visa plugin.

**Note:** The Dispute Rules Content Pack for Visa application is dependent on the Financial Services Card Operations application.

## Plugins

|Plugin|Description|
|------|-----------|
|Financial Services Card Operations \[com.sn\_bom\_credit\_card\]|Enables quick processing of credit card applications and card transaction disputes.|

## Tables installed

<table id="table_f2h_prv_s1c"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Dispute Intake

 \[sn\_bom\_credit\_card\_dispute\_intake\]

</td><td>

Stores all Visa Dispute Questionnaire questions and responses. Extends the Intake Form \[sn\_evnt\_inq\_qtn\] table.

</td></tr><tr><td>

Cardholder Dispute Intake

 \[sn\_bom\_credit\_card\_cardholder\_dispute\_intake\]

</td><td>

Stores Visa Dispute Questionnaire questions and responses submitted by consumers, such as a dispute playbook on a service portal. See [Create a dispute case with Dispute Intake in Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/dispute-management/creating-an-onboarding-case-with-dispute-playbook-for-portal.md) for more information. Extends the Dispute Intake \[sn\_bom\_credit\_card\_dispute\_intake\] table.

</td></tr></tbody>
</table>## Tables referenced by chargeback eligibility rules

**Note:** The tables in this section aren't installed by the Dispute Rules Content Pack for Visa application. They are owned by other applications that the Dispute Rules Content Pack for Visa application depends on. See [Tables installed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/dispute-management/components-installed-with-dispute-rules-content-pack-for-visa.md) for the tables this application installs.

<table id="table_cbrules_tbl_ref"><thead><tr><th>

Table

</th><th>

Owning application

</th><th>

Role in chargeback eligibility rules

</th></tr></thead><tbody><tr><td>

Card Transaction

 \[sn\_bom\_card\_transaction\]

</td><td>

Financial Services Operations Core \[sn\_bom\]

</td><td>

The core financial transaction record. Nearly every eligibility rule evaluates fields on this table, including authorization amounts, settlement amounts, and merchant details.

</td></tr><tr><td>

Disputes Transaction

 \[sn\_bom\_credit\_card\_disputes\_transaction\]

</td><td>

Financial Services Card Operations \[sn\_bom\_credit\_card\]

</td><td>

The per-transaction dispute record. This is the entry point every chargeback eligibility rule evaluates against.

</td></tr><tr><td>

Dispute Intake

 \[sn\_bom\_credit\_card\_dispute\_intake\]

</td><td>

Financial Services Card Operations \[sn\_bom\_credit\_card\]

</td><td>

Dispute intake questionnaire responses. Decision-table conditions reference this table directly to determine eligibility based on the agent's or customer's answers.

</td></tr><tr><td>

Cardholder Dispute Intake

 \[sn\_bom\_credit\_card\_cardholder\_dispute\_intake\]

</td><td>

Financial Services Card Operations \[sn\_bom\_credit\_card\]

</td><td>

Portal-submitted dispute intake questionnaire responses. Extends the Dispute Intake table.

</td></tr></tbody>
</table>**Parent Topic:**[Dispute Rules Content Pack for Visa reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/dispute-management/dispute-content-pack-for-visa-reference.md)

