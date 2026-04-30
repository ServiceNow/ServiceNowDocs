---
title: Explore Now Assist for Common Finance and Supply Chain Features
description: Use Now Assist for Common Finance and Supply Chain features to summarize supplier details and purchase orders and keep fulfillers informed of their status, progress, and required actions.
locale: en-US
release: zurich
product: Now Assist for FSC Common
classification: now-assist-for-fsc-common
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Now Assist for FSC Common, Now Assist for Finance and Supply Chain, Finance and Supply Chain]
---

# Explore Now Assist for Common Finance and Supply Chain Features

Use Now Assist for Common Finance and Supply Chain features to summarize supplier details and purchase orders and keep fulfillers informed of their status, progress, and required actions.

## Overview of Now Assist for Common Finance and Supply Chain Features

With Now Assist for Common Finance and Supply Chain, fulfillers can leverage generative AI-powered summarization to quickly gain a clear understanding of supplier details and purchase orders. These summaries provide visibility into the overview, completed actions, status, and upcoming steps, empowering fulfillers to take timely and informed actions.

The summarization capabilities are available in the Source-to-Pay Workspace.

**Note:** You can install this application only if you're entitled to the Sourcing and Procurement Operations Pro Plus SKU or the Source-to-Pay Operations Pro Plus SKU.

## Now Assist skills for Common Finance and Supply Chain Features

![Now Assist skills for Common Finance and Supply Chain features section, showing the Field Extractor, Supplier summarization for fulfillers, and Purchase order summarization for fulfillers feature cards.](../../accounts-payable-operations/image/now-assist-for-fsc.png)

## Field Extractor

Extracts the invoice number or supplier invoice number generated in APO and the supplier name by evaluating the description and short description in the inquiry case generated through different channels \(emails, virtual agent chats, or, web content\) and updates the same in the case. In some cases, the supplier provides their invoice number \(supplier invoice number\), and the system will automatically derive corresponding APO invoice number and updates the case.

As a fulfiller, you can extract and auto-populate the invoice number and supplier invoice number by evaluating the description and short description fields in an inquiry case for Accounts Payable Operations. The access control list \(ACLs\) confirms that only authorized agents can activate or configure the skill. Activate the Field extractor skill in the admin console of Now Assist for Common Finance and Supply Chain features, which trigger the automatic extraction of keys \(invoice number and supplier invoice number\) from inquiry cases received through various channels. Automating the extraction of keys \(invoice and supplier numbers\) enhances Accounts Payable agents' efficiency, leading to faster and more accurate resolutions. For more information on working with inquiry cases, see [Invoice inquiry cases](../../accounts-payable-operations/concept/work-with-inquiry-cases.md).

## Supplier summarization for fulfillers

Summarize supplier details and keep fulfillers informed about their overview, total spends, and performance indicators depending on the user persona.

As a fulfiller \(sn\_fsc\_genai.now\_assist\_fulfiller\), you can use summarize supplier details in the Source-to-Pay Workspace for the following products:

-   Sourcing and Procurement Operations
-   Supplier Lifecycle Operations
-   Accounts Payable Operations

The supplier summarization retrieves the information depending upon the user persona \(SPO - sn\_shop.procurement\_specialist, SLO - sn\_slm.manager, or APO - sn\_ap\_apm.accounts\_payable\_specialist\).

## Inquiry Classifier

Auto-populates the subcategory of an invoice inquiry case by analyzing its description and short description.

As a fulfiller \(sn\_fsc\_genai.now\_assist\_fulfiller\), you can use Inquiry Classifier in the Accounts Payable Operations product.

## Purchase order summarization for fulfillers

Summarize purchase orders and keep fulfillers informed about their status, progress, and action items.

As a fulfiller \(sn\_fsc\_genai.now\_assist\_fulfiller\), you can use summarize purchase orders in the Source-to-Pay Workspace for the following products:

-   Sourcing and Procurement Operations
-   Supplier Lifecycle Operations
-   Accounts Payable Operations

For more information on configuring Now Assist for Common Finance and Supply Chain features, see [Configuring Now Assist for Common Finance and Supply Chain features](../task/configure-now-assist-fsc.md).

To learn more about how to use Now Assist for Common Finance and Supply Chain features, see [Using Now Assist for Common Finance and Supply Chain features](now-assist-fsc-using.md)

-   **[Supporting information for Now Assist for Common Finance and Supply Chain features](now-assist-fsc-supporting-info.md)**  
Get a quick overview of the important information that is related to the Now Assist for Sourcing and Procurement Operations \(SPO\) application.
-   **[Roles for Now Assist for FSC Common](now-assist-common-roles.md)**  
Grant fulfiller, requester, and supplier user roles to access Now Assist for FSC Common skills, powered by generative AI along with the product specific Now Assist features.

**Parent Topic:**[Now Assist for FSC Common](now-assist-fsc-common.md)

**Related topics**  


[Explore Now Assist for Sourcing and Procurement Operations \(SPO\)](now-assist-spo-exploring.md)

[Explore Now Assist for Supplier Lifecycle Operations \(SLO\)](../../supplier-lifecycle-operations/concept/now-assist-slo-exploring.md)

[Exploring Now Assist for Accounts Payable Operations \(APO\)](../../accounts-payable-operations/concept/exploring-now-assist-apo.md)

