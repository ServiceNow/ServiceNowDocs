---
title: Configuring Card Data Security
description: Plan and configure your implementation of Card Data Security by following the tasks listed in this configuration overview.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Configuring Card Data Security

Plan and configure your implementation of Card Data Security by following the tasks listed in this configuration overview.

## Configuration overview

Refer to the following steps to set up and configure Card Data Security for the first time.

<table id="table_gsz_1jw_33c"><thead><tr><th>

Step

</th><th>

Description

</th><th>

Where to perform

</th></tr></thead><tbody><tr><td>

[Provision our tokenizer service and complete the onboarding procedure](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2830577)

</td><td>

Ensure that you have provisioned our tokenizer service and that you have completed the onboarding procedure. Tokenizer service accounts are hosted on multi-tenant shared infrastructure, isolated by account and vault boundaries.

 For more information, contact your ServiceNow account representative.

</td><td>

Tokenizer service

</td></tr><tr><td>

[Create tokenizer service vault](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2830577)

</td><td>

Create the tables in our tokenizer service. These tables will contain the PCI data from Third-Party Systems.

</td><td>

Tokenizer service

</td></tr><tr><td>

[Set up connections, service accounts, and context-aware authorization in the tokenizer service](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2830577)

</td><td>

Set up the connections, service accounts, and context-aware authorization to enable communication between your ServiceNow instance, the tokenizer service, and the Third-Party System.

</td><td>

Tokenizer service

</td></tr><tr><td>

[Set up Visa integration](../../fso-visa-spoke/concept/financial-services-operations-integration-with-visa-landing-page.md)

 [Set up Mastercard integration](../../fso-mastercard/concept/financial-services-operations-integration-with-mastercard-landing-page.md)

</td><td>

Install and set up integrations to the Third-Party Systems \(such as Financial Services Operations Integration with Visa, and Financial Services Operations Integration with Mastercard\). Card Data Security requires these integrations to function correctly.

</td><td>

ServiceNow

</td></tr><tr><td>

[Install Card Data Security](../task/install-card-data-security.md)

</td><td>

Install Card Data Security \(sn\_data\_sec\) from the ServiceNow Store.

</td><td>

ServiceNow

</td></tr><tr><td>

[Set up OAuth for Card Data Security](set-up-oauth-for-card-data-security.md)

</td><td>

For OAuth authentication, follow these steps to set up connectivity with your ServiceNow instance. These connections are required to get file metadata and download URLs from files hosted in the tokenizer service vault.

**Note:** You must set up OAuth to use the Card Data Security container components, including the [PAN reveal components](../task/reveal-a-pan-using-card-data-security.md) and the [file viewing component](manage-attachments-in-card-data-security.md).

</td><td>

ServiceNow

</td></tr><tr><td>

[Set up tokenized HTTP connection &amp; credential aliases](../task/create-a-new-tokenizer-route.md)

</td><td>

For API authentication, define the connection and credentials in ServiceNow to communicate to the Third-Party System via our tokenizer service.

</td><td>

ServiceNow

</td></tr><tr><td>

[Manage Tokenizer Resource Configurations](manage-tokenizer-resource-configurations.md)

</td><td>

Review the entries for each endpoint that sends and receives tokenized data.

</td><td>

ServiceNow

</td></tr><tr><td>

[Customize your card disputes workflow with the Card Data Security container](card-data-security-component.md)

</td><td>

Card Data Security includes a [PAN reveal component](../task/reveal-a-pan-using-card-data-security.md) and a [document viewing component](manage-attachments-in-card-data-security.md).

 To make changes, you can modify the preconfigured Card Data Security components using UI Builder.

</td><td>

ServiceNow

</td></tr></tbody>
</table>