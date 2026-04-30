---
title: Components installed with the Dispute Rules Content Pack for Visa plugin
description: Several types of components are installed with the installation of the Dispute Rules Content Pack for Visa plugin.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Dispute Rules Content Pack for Visa reference, Dispute Rules Content Pack for Visa, Managing Visa disputes, Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Components installed with the Dispute Rules Content Pack for Visa plugin

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

Visa Dispute Intake

 \[sn\_bom\_visa\_cp\_visa\_dispute\_questionnaire\]

</td><td>

Stores all Visa Dispute Questionnaire questions and responses. Extends the Intake Form \[sn\_evnt\_inq\_qtn\] table.

</td></tr><tr><td>

Visa Dispute Cardholder Intake

 \[sn\_bom\_visa\_cp\_visa\_dispute\_cardholder\_intake\]

</td><td>

Stores Visa Dispute Questionnaire questions and responses submitted by consumers, such as a dispute playbook on a service portal. See [Managing dispute intake in portal](../../fso-card-operations/concept/dispute-playbook-for-portal.md) for more information. Extends the Visa Dispute Intake \[sn\_bom\_visa\_cp\_visa\_dispute\_questionnaire\] table.

</td></tr><tr><td>

CRB Region Type

 \[sn\_bom\_visa\_cp\_crb\_region\_type\]

</td><td>

Stores all Visa Card Recovery Bulletin \(CRB\) regions.

</td></tr></tbody>
</table>**Parent Topic:**[Dispute Rules Content Pack for Visa reference](../concept/dispute-content-pack-for-visa-reference.md)

