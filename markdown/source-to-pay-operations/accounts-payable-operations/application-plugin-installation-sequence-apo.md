---
title: Application plugin installation sequence in Accounts Payable Operations
description: View the consolidated list of plugins, high-level description of each plugin, and the dependencies that are required before installing each plugin in Accounts Payable Operations.
locale: en-US
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Components installed with Accounts Payable Invoice Processing, Install Accounts Payable Invoice Processing, Configure, Accounts Payable Operations, Finance and Supply Chain]
---

# Application plugin installation sequence in Accounts Payable Operations

View the consolidated list of plugins, high-level description of each plugin, and the dependencies that are required before installing each plugin in Accounts Payable Operations.

**Important:** Before installing a plugin listed in the Plugin name column, ensure that you install all corresponding dependencies listed in the Plugin dependencies column from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

<table id="table_mqm_3sr_hrb"><thead><tr><th>

Sequence

</th><th>

Plugin name

</th><th>

Description

</th><th>

Plugin dependencies

</th></tr></thead><tbody><tr><td>

1

</td><td>

Source-to-Pay Common Architecture

 \[com.snc.sn\_shop\]

</td><td>

Maintains primary data such as Enterprise Resource Planning \(ERP\) sources, legal entities, accounting periods, and so on.

</td><td>

-   Finance Common Architecture \[com.sn\_fin\]
-   Service Delivery Common \[com.sn\_spend\_sdc\]

</td></tr><tr><td>

2

</td><td>

Source-to-Pay Workspace

 \[com.sn\_spend\_workspace\]

</td><td>

Provides a single environment for Procurement Specialists to work on purchase requisitions, sourcing requests, negotiations, procurement requests, and more.

</td><td>

10

</td></tr><tr><td>

3

</td><td>

Supplier Collaboration Portal

 \[com.snc.sn\_supplier\_sp\]

</td><td>

Includes demo data and relatedServiceNow Store applications and plugins.

</td><td>

Supplier Common Architecture \[com.snc.sn\_slm\]

</td></tr><tr><td>

4

</td><td>

Glide Virtual Agent

</td><td>

Activate the virtual agent chatbot \(chat channel\) in the supplier portal for suppliers to complete Accounts Payable Operations related self-service tasks.

</td><td>

 

</td></tr><tr><td>

5

</td><td>

Advanced Work Assignment for Source-to-Pay Operations

 \[com.snc.sn\_spend\_awa\]

</td><td>

Provides configurations to support automatic routing, queuing, and assignment of procurement cases, emails, and live agent chat conversations.

</td><td>

-   Advanced Work Assignment \[com.glide.awa\]
-   Agent chat \[com.glide.interaction.awa\]

</td></tr><tr><td>

6

</td><td>

Document Intelligence

 \[com.snc.docintel\]

</td><td>

Provide solutions that enables any organization to automate and accelerate the process of extracting data from documents.

</td><td>

sn-docintel-iframe

 \[com.sn\_docintel\_iframe\]

</td></tr><tr><td>

7

</td><td>

Document Intelligent Admin

 \[com.snc.docintel\_admin\]

</td><td>

Provides full access to the Document Intelligence application, apart from modifying a subset of system properties, and the billing and internal tables.

</td><td>

sn-docintel-iframe

 \[com.sn\_docintel\_iframe\]

</td></tr><tr><td>

8

</td><td>

Accounts Payable Operations integration with Document Intelligence

 com.sn\_ap\_ic

</td><td>

Enables you to automatically capture data from incoming invoices, thus significantly reducing manual effort.

</td><td>

Document Intelligence

 \[com.snc.docintel\]

</td></tr><tr><td>

9

</td><td>

Invoice Case Management

 \[com.sn\_ap\_cm\]

</td><td>

Includes demo data and relatedServiceNow Store applications and plugins.

</td><td>

-   Source-to-Pay Common Architecture \[com.snc.sn\_shop\]
-   Source-to-Pay Workspace \[com.sn\_spend\_workspace\]

</td></tr><tr><td>

10

</td><td>

Accounts Payable Invoice Processing

 \[com.sn\_ap\_apm\]

</td><td>

Enables Accounts Payable specialists to ingest invoice documents and extract invoice data using Document Intelligence

</td><td>

-   Invoice Case Management \[com.sn\_ap\_cm\]
-   Accounts Payable Operations integration with Document Intelligence \[com.sn\_ap\_ic\]

</td></tr></tbody>
</table>**Related topics**  


[Invoice Case Management](../concept/acc-pay-case-mgmt-overview.md)

[Accounts Payable Invoice Processing](../concept/acc-pay-invoice-processing.md)

[Source-to-Pay Workspace](../concept/acc-pay-workspace.md)

[Using Supplier Collaboration Portal in APO](../concept/using-supplier-collaboration-portal.md)

