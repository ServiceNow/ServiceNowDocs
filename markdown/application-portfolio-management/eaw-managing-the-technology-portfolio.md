---
title: Manage the Technology Reference Model in Enterprise Architecture Workspace
description: You can use the Technology Reference Model \(TRM\) feature in Enterprise Architecture Workspace to define the standards for your software and hardware products and manage unapproved products in your organization.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Exploring Technology Portfolio view, Explore, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Manage the Technology Reference Model in Enterprise Architecture Workspace

You can use the Technology Reference Model \(TRM\) feature in Enterprise Architecture Workspace to define the standards for your software and hardware products and manage unapproved products in your organization.

## Overview and benefits of a TRM

In your business enterprise, using an unapproved software can create a risk to the organization. The risks can include the following:

-   Security risks: The software might be exposed to security issues.
-   Delivery risks: There might not be sufficient knowledge on how to support the software.
-   Legal risks: A business application might use the software in illegal ways.

You must define the standards for the software that is to be used and the software versions that are permitted for use in your organization. Also, you need a way to explore when a non-permitted software is being used within the organization and in which business applications.

You can use the TRM module in the Enterprise Architecture Workspace to perform the following:

-   View a list of all available TRM products. You can also view the list of TRM products grouped by product category.
-   Request a TRM product
-   Request a TRM product lifecycle
-   Create a TRM product
-   Create a TRM product lifecycle
-   Approve or reject TRM product and product lifecycle requests.

Using the TRM module, you can manage the standards of the technology and set the right guardrail for technology usage. Setting the standards can improve the technical debt, security posture and save costs for the organization.

You can also assign an owner to a TRM category, to ensure clear accountability and improved governance standards. The owner is responsible for maintaining consistent technology compliance standards for that TRM category.

## TRM Product Lifecycle

Each product in the TRM library is associated with a set of life-cycle phases with a start and end date. The life-cycle phases could be approved, unapproved, approved with constraints, Divest, and evaluation.

The TPM home page fetches all the business applications that are being used in your organization. It helps to review the status of the software that is being used. You can understand if any business application is using the software that is not part of the TRM or a software version that is not approved for production. For more information, see [TRM lifecycle timelines on Gantt chart](eaw-trm-lifecycle-timelines-on-gantt-chart.md).

The TRM module uses a similar module to TPM to search in the TRM library. You can view the software that is part of the TRM library, and initiate a request to add the software or software version to the TRM library.

You can also use the TRM with the Software Asset Management \(SAM\) plugin. This plugin helps you to fetch or select the products and versions for the TRM library. You can also define your own software products when the Software Asset Management integration module isn’t available for your instance.

-   **[Manage TRM technical debt](eaw-manage-trm-technical-debt.md)**  
Manage the TRM technical debts that are created for the products that aren’t approved for the usage.
-   **[TRM Technical Debt calculation in Enterprise Architecture Workspace](eaw-trm-technical-debt-calc.md)**  
A TRM technical debt indicates the unapproved usage of a software. The technical debts table \[sn\_apm\_trm\_standards\_technical\_debt\], displays the TRM products and associated business applications details, and the reason for the technical debt.
-   **[Work with TRM lifecycle with wildcard](eaw-trm-wildcard-to-create-technical-debts.md)**  
You can use Technology Reference Model \(TRM\) lifecycles with wildcards to update multiple TRM software product lifecycles simultaneously without having to specify the exact minor version details of individual TRM software products.

**Parent Topic:**[Exploring Technology Portfolio view](eaw-technology-portfolio-view.md)

**Related topics**  


[Approve or reject TRM requests](../../task/eaw-task/eaw-approve-trm-req.md)

[Working with Technology Reference Model \(TRM\) in EA Workspace](eaw-work-with-trm.md)

[View TPM and TRM lifecycle timelines on the Gantt chart](../../task/eaw-task/eaw-view-tpm-and-trm-lifecycle-timelines-in-gantt-chart.md)

[Gantt view of TPM and TRM lifecycle timelines](eaw-gantt-view-of-tpm-and-trm-lifecycle-timelines.md)

[TRM lifecycle timelines on Gantt chart](eaw-trm-lifecycle-timelines-on-gantt-chart.md)

[Configure TRM phases](eaw-setup-trm-phases.md)

[Configure TRM categories](eaw-setup-trm-categories.md)

