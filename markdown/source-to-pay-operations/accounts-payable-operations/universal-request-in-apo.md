---
title: Universal Request in Accounts Payable Operations
description: Universal Request provides a centralized entry point for suppliers and invoice owners to submit requests that are converted into invoice cases for processing in Accounts Payable Operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/universal-request-in-apo.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [APO, Accounts Payable Operations, invoice management, invoice case management, universal request, employee inquiry]
breadcrumb: [Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Universal Request in Accounts Payable Operations

Universal Request provides a centralized entry point for suppliers and invoice owners to submit requests that are converted into invoice cases for processing in Accounts Payable Operations.

The Universal Request \(UR\) is a key ServiceNow capability that serves as a centralized entry point for both invoice owners and suppliers. The primary purpose of UR is to simplify the process of raising general case requests, thereby removing any uncertainty regarding the appropriate department to contact for assistance.

## Persona based roles

UR can be created by:

-   Invoice owners through Employee center. For more information on ServiceNow Universal Request, see [Exploring Universal Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/explore-universal-request.md)
-   Suppliers submit inquiry case request or issue \(UR\) using the Supplier Collaboration portal. For more information on UR from supplier portal, see [Create Universal Request from Supplier portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-ur-from-supplier-portal.md).

## How UR works in Accounts Payable Operations

UR seamlessly integrates with the APO system, enabling more efficient management of invoice cases. This integration not only streamlines the overall invoice handling process but also enhances cross-departmental service delivery, confirming that case requests are addressed promptly and accurately across the organization. UR works in APO in the following order:

1.  Request submission- Invoice owners or suppliers initiate a UR via the Employee portal or the Supplier portal. The UR records essential information and uses predefined mappings.
2.  Routing and case creation- Accounts Payable \(AP\) agents within the Accounts Payable Universal Request group are authorized to review Universal Requests \(URs\) and, based on the provided details, can create an invoice case as the primary ticket. This process can be executed either within the Source-to-Pay workspace or directly from the platform.
3.  Processing and automation- The updates are synchronized back to the UR. The invoice owner or supplier tracks progress and receives updates through the UR case in the employee portal or supplier portal.

\[Omitted image "universal-request.png"\] Alt text: Universal Request

## Key features

-   Both invoice owners and suppliers can submit a single request, eliminating the need to navigate multiple portals and simplifying the initial process.
-   Users part of Accounts Payable Universal Request group can check and create primary ticket for invoice case based on the details in the UR.
-   Users benefit from consolidated case activity updates, which are accessible from their respective portals. This eliminates the need to switch between systems and provides a seamless tracking experience.

## Field mappings

When a Universal Request is transferred to an Accounts Payable inquiry case, the following fields are copied from the Universal Request record to the AP case record.

|Universal Request \(source field\)|AP case \(target field\)|
|----------------------------------|------------------------|
|Short description \(short\_description\)|Short description \(short\_description\)|
|Description \(description\)|Description \(description\)|
|Priority \(priority\)|Priority \(priority\)|
|Opened by \(opened\_by\)|Opened by \(opened\_by\)|

-   **[Create invoice case from Universal Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-invoice-case-from-ur.md)**  
Validate incoming Universal Request items in the Source-to-Pay Workspace and create invoice cases for further processing.

**Parent Topic:**[Use Accounts Payable Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/use-acc-pay-mgmt.md)

**Related topics**  


[Create a knowledge base article about invoice]()

[Invoice case categories and subcategories]()

[Using Invoice Case Management]()

[Using Accounts Payable Invoice Processing]()

[Advanced Work Assignment in Accounts Payable Operations]()

[Configure Advanced Work Assignment for Accounts Payable Operations]()

[Using Advanced Work Assignment for Accounts Payable Operations]()

[Working with Advanced Work Assignment]()

[Interaction management in Accounts Payable Operations]()

[Composing emails with predefined content from the Source-to-Pay Workspace]()

[Playbook for updating the invoice primary data]()

[Using Supplier Collaboration Portal in APO]()

[Using Invoice Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/use-invoice-case-mgmt.md)

[Create Universal Request from Supplier portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-ur-from-supplier-portal.md)

