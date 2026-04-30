---
title: Managing the Technology Reference Model \(TRM\) in Enterprise Architecture Workspace
description: You can use the Technology Reference Model \(TRM\) feature in Enterprise Architecture Workspace to define the standards for your software and hardware products and manage unapproved products in your organization.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Technology Portfolio view, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Managing the Technology Reference Model \(TRM\) in Enterprise Architecture Workspace

You can use the Technology Reference Model \(TRM\) feature in Enterprise Architecture Workspace to define the standards for your software and hardware products and manage unapproved products in your organization.

## Overview and benefits of a TRM

In your business enterprise, using an unapproved software can create a risk to the organization. The risks can include the following:

-   Security risks: The software might be exposed to security issues.
-   Delivery risks: There might not be sufficient knowledge on how to support the software.
-   Legal risks: A business application might use the software in illegal ways.

You need to define the standards for the software that is to be used and the software versions that are permitted for use in your organization. Also, you need a way to explore when a non-permitted software is being used within the organization and in which business applications.

You can use the TRM module in the Enterprise Architecture Workspace to perform the following:

-   View a list of all available TRM products. You can also view the list of TRM products grouped by product category.
-   Request a TRM product
-   Request a TRM product lifecycle
-   Create a TRM product
-   Create a TRM product lifecycle
-   Approve or reject TRM product and product lifecycle requests.

Using the TRM module, you can manage the standards of the technology and set the right guardrail for technology usage. Setting the standards can improve the technical debt, security posture and save costs for the organization.

## TRM Product Lifecycle

Each product in the TRM library is associated with a set of life-cycle phases with a start and end date. The life-cycle phases could be approved, unapproved, approved with constraints, Divest, and evaluation.

The TPM home page fetches all the business applications that are being used in your organization. It helps to review the status of the software that is being used. You can understand if any business application is using the software that is not part of the TRM or a software version that is not approved for production. For more information, see [TRM lifecycle timelines on Gantt chart](eaw-trm-lifecycle-timelines-on-gantt-chart.md).

The TRM module uses a similar module to TPM to search in the TRM library. You can view the software that is part of the TRM library, and initiate a request to add the software or software version to the TRM library.

You can also use the TRM with the Software Asset Management \(SAM\) plugin. This plugin helps you to fetch or select the products and versions for the TRM library. You can also define your own software products when the Software Asset Management integration module isn’t available for your instance.

-   **[View all TRM products grouped by product category](../../task/eaw-task/eaw-view-all-trm-products-grouped-by-product-category.md)**  
You can view all your Technology Reference Model \(TRM\) products, grouped by category, in the Enterprise Architecture Workspace.
-   **[View all TRM products](../../task/eaw-task/eaw-view-all-trm-products.md)**  
You can view all available Technology Reference Model \(TRM\) products in the Enterprise Architecture Workspace.
-   **[Request a TRM product](../../task/eaw-task/eaw-request-a-trm-products.md)**  
You can request a TRM product using the TRM catalog to add a new software or hardware to the TRM library.
-   **[Request a TRM product lifecycle](../../task/eaw-task/eaw-request-a-trm-product-lifecycle.md)**  
You can add a new request to create a life cycle for a TRM product.
-   **[Add a TRM product in Enterprise Architecture Workspace](../../task/eaw-task/eaw-create-trm-prod-lifecycle.md)**  
As an Enterprise Architect, you can add a new TRM product to the TRM library.
-   **[Add a TRM product lifecycle](../../task/eaw-task/eaw-create-trm-prod-lifecycle-req.md)**  
As an Enterprise Architect, you can add a new TRM product lifecycle.
-   **[View product capabilities associated with a Technology Reference Model product](../../task/eaw-task/eaw-view-capabilities-associated-with-trm-product.md)**  
You can view the list of product capabilities associated with Technology Reference Model \(TRM\) product, in the Enterprise Architecture Workspace.
-   **[Create product capabilities and associate it with a Technology Reference Model product](../../task/eaw-task/eaw-create-a-new-product-capability-and-assoc-trm-product.md)**  
You can create product capabilities and associate it with Technology Reference Model \(TRM\) products in the Enterprise Architecture Workspace.
-   **[Add an existing product capability to a Technology Reference Model product](../../task/eaw-task/eaw-add-existing-product-capability-to-trm-product.md)**  
You can add existing product capabilities to Technology Reference Model \(TRM\) products in the Enterprise Architecture Workspace.
-   **[Remove product capabilities associated with a Technology Reference Model product](../../task/eaw-task/eaw-remove-product-capabilities-assoc-with-trm-product.md)**  
You can remove the product capabilities associated with Technology Reference Model \(TRM\) products in the Enterprise Architecture Workspace, confirming only the relevant and current product capabilities are associated with the TRM products.
-   **[Working with TRM lifecycle with wildcard](eaw-trm-wildcard-to-create-technical-debts.md)**  
You can use Technology Reference Model \(TRM\) lifecycles with wildcards to update multiple TRM software product lifecycles simultaneously without having to specify the exact minor version details of individual TRM software products.
-   **[Manage TRM technical debt](eaw-manage-trm-technical-debt.md)**  
Manage the TRM technical debts that are created for the products that aren’t approved for the usage.

**Parent Topic:**[Technology Portfolio view](eaw-technology-portfolio-view.md)

**Related topics**  


[Approve or reject TRM requests](../../task/eaw-task/eaw-approve-trm-req.md)

