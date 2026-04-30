---
title: Install Accounts Payable Operations integration with Document Intelligence
description: Accounts Payable Operations integration with Document Intelligence \(com.sn\_ap\_ic\) is installed automatically along with Accounts Payable Invoice Processing \(com.sn\_ap\_apm\).
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Install Accounts Payable Operations integration with Document Intelligence

Accounts Payable Operations integration with Document Intelligence \(com.sn\_ap\_ic\) is installed automatically along with Accounts Payable Invoice Processing \(com.sn\_ap\_apm\).

## Required plugins

To use the flows for extracting data from the invoice document received as an email attachment, you must install ServiceNow® Document Intelligence.

**Note:** Accounts Payable Operations integration with Document Intelligence supports Document Intelligence version 2.4.

For more information, see [Install Document Intelligence](https://www.servicenow.com/docs/access?context=install-document-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

-   **[Components installed with Accounts Payable Operations integration with Document Intelligence](../reference/installed-with-docintel-apm.md)**  
Several types of components are installed with activation of the Accounts Payable Operations integration with Document Intelligence \(com.sn\_ap\_ic\) application plugin, including user roles, flows, and tables.
-   **[Invoice Processing use case](docintel-invoice-process-usecase.md)**  
Accounts Payable Operations integration with Document Intelligence provides the **DO NOT USE - Invoice Processing** use case.
-   **[Configuring the invoice ingestion flows using Accounts Payable Operations integration with Document Intelligence](config-apo-docintel-integration.md)**  
Configure Accounts Payable Operations integration with Document Intelligence to automatically create an invoice processing case and extract the required data from an invoice attachment received via email.
-   **[How Accounts Payable Operations integration with Document Intelligence works](apm-docintel-how-it-works.md)**  
Accounts Payable Operations integration with Document Intelligence uses automated workflows to extract the required information from the invoice document received as an email attachment, creates an invoice record in Accounts Payable Operations, and adds the extracted information into the newly created invoice record.

**Parent Topic:**[Configuring Accounts Payable Operations](config-acc-pay-mgmt.md)

**Related topics**  


[Install Accounts Payable Invoice Processing](../task/install-acc-pay-mgmt.md)

[Install Invoice Case Management](../task/install-invoice-case-mgmt.md)

[Domain separation and Accounts Payable Operations](apm-domain-separation.md)

