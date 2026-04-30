---
title: Universal Request in Accounts Payable Operations
description: The ServiceNow Universal Request \(UR\) feature transforms fragmented service intake into a centralized, intelligent, and scalable experience for invoice case management.
locale: en-US
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2025-11-06"
reading_time_minutes: 4
breadcrumb: [Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Universal Request in Accounts Payable Operations

The ServiceNow Universal Request \(UR\) feature transforms fragmented service intake into a centralized, intelligent, and scalable experience for invoice case management.

The Universal Request \(UR\) is a key ServiceNow capability that serves as a centralized entry point for both invoice owners and suppliers. The primary purpose of UR is to simplify the process of raising general case requests, thereby removing any uncertainty regarding the appropriate department to contact for assistance.

## Persona based roles

UR can be created by:

-   Invoice owners through Employee center. For more information on ServiceNow Universal Request, see [Exploring Universal Request](https://www.servicenow.com/docs/access?context=explore-universal-request&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)
-   Suppliers submit inquiry case request or issue \(UR\) using the Supplier Collaboration portal. For more information on UR from supplier portal, see [Create Universal Request from Supplier portal](../task/create-ur-from-supplier-portal.md).

## How UR works in Accounts Payable Operations

UR seamlessly integrates with the APO system, enabling more efficient management of invoice cases. This integration not only streamlines the overall invoice handling process but also enhances cross-departmental service delivery, confirming that case requests are addressed promptly and accurately across the organization. UR works in APO in the following order:

1.  Request submission- Invoice owners or suppliers initiate a UR via the Employee portal or the Supplier portal. The UR records essential information and uses predefined mappings.
2.  Routing and case creation-Accounts Payable \(AP\) agents within the Accounts Payable Universal Request group are authorized to review Universal Requests \(URs\) and, based on the provided details, can create an invoice case as the primary ticket. This process can be executed either within the Source-to-Pay workspace or directly from the platform.
3.  Processing and automation- The updates are synchronized back to the UR. The invoice owner or supplier tracks progress and receives updates through the UR case in the employee portal or supplier portal.

![Universal Request](../image/universal-request.png)

Key features:

-   Both invoice owners and suppliers can submit a single request, eliminating the need to navigate multiple portals and simplifying the initial process.
-   Users part of Accounts Payable Universal Request group can check and create primary ticket for invoice case based on the details in the UR.
-   Users benefit from consolidated case activity updates, which are accessible from their respective portals. This eliminates the need to switch between systems and provides a seamless tracking experience.

-   **[Create invoice case from Universal Request](../task/create-invoice-case-from-ur.md)**  
AP agents validate the incoming UR requests in the Source-to-Pay workspace and create an invoice case for further processing.

**Parent Topic:**[Use Accounts Payable Operations](use-acc-pay-mgmt.md)

**Related topics**  


[Create a knowledge base article about invoice](../task/create-knowledge-base-articles-for-invoices.md)

[Invoice case categories and subcategories](working-with-cases.md)

[Using Invoice Case Management](use-invoice-case-mgmt.md)

[Using Accounts Payable Invoice Processing](use-ap-invoice-processing.md)

[Advanced Work Assignment in Accounts Payable Operations](advanced-work-assignment.md)

[Configure Advanced Work Assignment for Accounts Payable Operations](../task/configure-advanced-work-assignment-for-apo.md)

[Using Advanced Work Assignment for Accounts Payable Operations](using-awa-for-apo.md)

[Working with Advanced Work Assignment](../task/working-with-advanved-work-assignment.md)

[Interaction management in Accounts Payable Operations](interaction-record.md)

[Composing emails with predefined content from the Source-to-Pay Workspace](email-composer-apm-workspace.md)

[Playbook for updating the invoice primary data](playbooks.md)

[Using Supplier Collaboration Portal in APO](using-supplier-collaboration-portal.md)

[Using Invoice Case Management](use-invoice-case-mgmt.md)

[Create Universal Request from Supplier portal](../task/create-ur-from-supplier-portal.md)

