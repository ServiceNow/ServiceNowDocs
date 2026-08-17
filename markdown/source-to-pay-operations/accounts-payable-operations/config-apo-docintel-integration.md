---
title: Configuring the invoice ingestion flows using Accounts Payable Operations integration with Document Intelligence
description: Configure Accounts Payable Operations integration with Document Intelligence to automatically create an invoice processing case and extract the required data from an invoice attachment received via email.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/config-apo-docintel-integration.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [APO, Accounts Payable Operations, Use case configuration, Invoice data extraction, Invoice capture configuration, invoice automation set-up, Doc-Intel, Document Intelligence, APO Integration, email invoice processing]
breadcrumb: [Install Accounts Payable Operations integration with Document Intelligence, Configure, Accounts Payable Operations, Finance and Supply Chain]
---

# Configuring the invoice ingestion flows using Accounts Payable Operations integration with Document Intelligence

Configure Accounts Payable Operations integration with Document Intelligence to automatically create an invoice processing case and extract the required data from an invoice attachment received via email.

The process for configuring Accounts Payable Operations integration with Document Intelligence includes the following scenarios:

<table id="table_lmf_qyg_1xb"><thead><tr><th>

Scenario

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

When Document Intelligence is installed and you want to use the invoice ingestion flows

</td><td>

1.  [Create a copy of the default invoice processing use case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-use-case-copy.md).
2.  Do the following to configure the invoice ingestion flows:
    1.  [Configure the newly created DocIntel Extract Values Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/configure-extract-values-flow.md).
    2.  [Configure the Invoice processing case for Invoice email flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/copy-invoice-email-di-flow.md).
    3.  [Configure the Invoice attachment DI processing flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/copy-di-processing-flow.md).
    4.  [Configure the DI STP Failed flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/copy-di-stp-failed-flow.md).
3.  Perform the steps described in [KB article KB1286265](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1286265) to run the business rule to delete the duplicate ml\_solution record from the ML Solution \[ml\_solution\] table.

</td></tr><tr><td>

When Document Intelligence is not installed

</td><td>

[Configure the Invoice email flow without Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/copy-invoice-email-no-di.md).

</td></tr><tr><td>

When Document Intelligence is installed but you want to disable the invoice ingestion flows

</td><td>

1.  [Configure Invoice email flow for disabling Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/copy-invoice-email-disable-di.md).
2.  [Deactivate the Invoice attachment DI processing flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/deactivate-di-attach-flow.md).

</td></tr></tbody>
</table>**Related topics**  


[Invoice processing cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/working-with-ingestion-cases.md)

