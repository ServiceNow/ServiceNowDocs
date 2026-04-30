---
title: Configuring the invoice ingestion flows using Accounts Payable Operations integration with Document Intelligence
description: Configure Accounts Payable Operations integration with Document Intelligence to automatically create an invoice processing case and extract the required data from an invoice attachment received via email.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Install Accounts Payable Operations integration with Document Intelligence, Configuring Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
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

1.  [Create a copy of the default Invoice Processing use case](../task/create-use-case-copy.md).
2.  Do the following to configure the invoice ingestion flows:
    1.  [Configure the newly created DocIntel Extract Values Flow](../task/configure-extract-values-flow.md).
    2.  [Copy and configure the Invoice processing case for Invoice email flow](../task/copy-invoice-email-di-flow.md).
    3.  [Copy and configure the Invoice attachment DI processing flow](../task/copy-di-processing-flow.md).
    4.  [Copy and configure the DI STP Failed flow](../task/copy-di-stp-failed-flow.md).
3.  Perform the steps described in [KB article KB1286265](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1286265) to run the business rule to delete the duplicate ml\_solution record from the ML Solution \[ml\_solution\] table.

</td></tr><tr><td>

When Document Intelligence is not installed

</td><td>

[Copy and configure the Invoice processing case for Invoice email flow when Document Intelligence is not installed](../task/copy-invoice-email-no-di.md).

</td></tr><tr><td>

When Document Intelligence is installed but you want to disable the invoice ingestion flows

</td><td>

1.  [Configure the Invoice processing case for Invoice email flow for disabling the Document Intelligence capability](../task/copy-invoice-email-disable-di.md).
2.  [Deactivate the Invoice attachment DI processing flow](../task/deactivate-di-attach-flow.md).

</td></tr></tbody>
</table>