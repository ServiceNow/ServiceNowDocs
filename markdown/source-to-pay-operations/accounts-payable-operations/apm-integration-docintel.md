---
title: Install Accounts Payable Operations integration with Document Intelligence
description: Accounts Payable Operations integration with Document Intelligence \(com.sn\_ap\_ic\) is installed automatically with Accounts Payable Invoice Processing \(com.sn\_ap\_apm\) to enable invoice data extraction.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/apm-integration-docintel.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice processing, DocIntel, Document Intelligence, integration]
breadcrumb: [Configure, Accounts Payable Operations, Finance and Supply Chain]
---

# Install Accounts Payable Operations integration with Document Intelligence

Accounts Payable Operations integration with Document Intelligence \(com.sn\_ap\_ic\) is installed automatically with Accounts Payable Invoice Processing \(com.sn\_ap\_apm\) to enable invoice data extraction.

## Required plugins

To use the flows for extracting data from the invoice document received as an email attachment, you must install ServiceNow® Document Intelligence.

**Note:** Accounts Payable Operations integration with Document Intelligence supports Document Intelligence version 2.4.

For more information, see [Install Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-document-intelligence.md).

-   **[Components installed with Accounts Payable Operations integration with Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/installed-with-docintel-apm.md)**  
Reference information for the roles, flows, and tables installed with the Accounts Payable Operations integration with Document Intelligence \(sn\_ap\_ic\) application plugin during activation.
-   **[Invoice Processing use case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/docintel-invoice-process-usecase.md)**  
The predefined Document Intelligence Invoice Processing use case identifies invoice fields to extract from email attachments and stores the data in invoice stage records for further processing.
-   **[Configuring the invoice ingestion flows using Accounts Payable Operations integration with Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/config-apo-docintel-integration.md)**  
Configure Accounts Payable Operations integration with Document Intelligence to automatically create an invoice processing case and extract the required data from an invoice attachment received via email.
-   **[How Accounts Payable Operations integration with Document Intelligence works](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/apm-docintel-how-it-works.md)**  
Document Intelligence uses automated workflows to extract invoice data from email attachments and populate invoice records in Accounts Payable Operations.

**Parent Topic:**[Configure Accounts Payable Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/config-acc-pay-mgmt.md)

**Related topics**  


[Install Accounts Payable Invoice Processing]()

[Install Invoice Case Management]()

[Domain separation and Accounts Payable Operations]()

