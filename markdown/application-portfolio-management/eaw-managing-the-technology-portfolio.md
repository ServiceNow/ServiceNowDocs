---
title: Technology Reference Model in Enterprise Architecture Workspace
description: The Technology Reference Model \(TRM\) feature in Enterprise Architecture Workspace helps define the standards for your software and hardware products and manage unapproved products in your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-managing-the-technology-portfolio.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [Exploring Technology Portfolio view, Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Technology Reference Model in Enterprise Architecture Workspace

The Technology Reference Model \(TRM\) feature in Enterprise Architecture Workspace helps define the standards for your software and hardware products and manage unapproved products in your organization.

## Overview and benefits of a TRM

In your business enterprise, using unapproved software can create a risk to the organization. The risks can include the following:

-   Security risks: The software might be exposed to security issues.
-   Delivery risks: There might not be sufficient knowledge on how to support the software.
-   Legal risks: A business application might use the software in illegal ways.

You must define the standards for the software that is to be used and the software versions that are permitted for use in your organization. Use this module to identify non-permitted software in use across the organization and the business applications that use it.

You can use the TRM module in the Enterprise Architecture Workspace to perform the following:

-   View a list of all available TRM products. You can also view the list of TRM products grouped by product category
-   Request a TRM product
-   Request a TRM product lifecycle
-   Create a TRM product
-   Create a TRM product lifecycle
-   Approve or reject TRM product and product lifecycle requests

When you request or create a TRM product, you can optionally add one or more lifecycle records as part of the same action. This eliminates the need to submit a separate lifecycle request afterward. Similarly, approving or rejecting a standalone TRM product lifecycle request applies to all child lifecycle records included in that request.

Using the TRM module, you can manage the standards of the technology and set the right guardrail for technology usage. Setting the standards can improve the technical debt, security posture and save costs for the organization.

You can also assign an owner to a TRM category, to facilitate clear accountability and improved governance standards. The owner is responsible for maintaining consistent technology compliance standards for that TRM category.

## TRM product lifecycle

Each product in the TRM library is associated with a set of lifecycle phases with a start and end date. The lifecycle phases could be approved, unapproved, approved with constraints, divest, and evaluation.

The TLM home page fetches all the business applications that are used in your organization. It helps to review the status of the software that is being used. You can understand if any business application is using the software that is not part of the TRM or a software version that is not approved for production. For more information, see [TRM lifecycle timelines on Gantt chart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-trm-lifecycle-timelines-on-gantt-chart.md).

The TRM module uses a similar module to TLM to search in the TRM library. You can view the software that is part of the TRM library, and initiate a request to add the software or software version to the TRM library.

You can also use the TRM with the Software Asset Management \(SAM\) plugin. This plugin helps you to fetch or select the products and versions for the TRM library. You can also define your own software products when the Software Asset Management integration module isn't available for your instance.

You can add lifecycle records to a TRM product as part of a product request or a standalone TRM product lifecycle request. The following limits apply to the number of lifecycle groups and phases you can include:

**Note:**

-   For software products: You can add up to 5 version and edition combinations, with a maximum of 10 phases per combination.
-   For hardware products: You can add up to 5 hardware models, with a maximum of 10 phases per hardware model.
-   You can zoom on this page to 200% or 400% through your browser settings without the loss of content or functionality. Page layouts are transformed into a vertical, stacked view automatically.

-   **[TRM technical debt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-manage-trm-technical-debt.md)**  
Manage the TRM technical debts that are created for the products that aren’t approved for the usage.
-   **[Technical debt calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-trm-technical-debt-calc.md)**  
Technical debt records identify products used in business applications that aren't approved in the TRM or that use unapproved versions. View technical debt records to understand conformance gaps and plan remediation.
-   **[Work with TRM lifecycle with wildcard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-trm-wildcard-to-create-technical-debts.md)**  
Use Technology Reference Model \(TRM\) lifecycles with wildcards to update multiple software product lifecycles simultaneously without specifying exact minor version details.

**Parent Topic:**[Exploring Technology Portfolio view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-technology-portfolio-view.md)

**Related topics**  


[Approve or reject TRM requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-approve-trm-req.md)

[Working with Technology Reference Model \(TRM\) in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-work-with-trm.md)

[View TPM and TRM lifecycle timelines on the Gantt chart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-view-tpm-and-trm-lifecycle-timelines-in-gantt-chart.md)

[Gantt view of TLM and TRM lifecycle timelines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-gantt-view-of-tpm-and-trm-lifecycle-timelines.md)

[TRM lifecycle timelines on Gantt chart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-trm-lifecycle-timelines-on-gantt-chart.md)

[Configure TRM phases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-setup-trm-phases.md)

[Configure TRM categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-setup-trm-categories.md)

[TRM technical debt states and transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-trm-technical-debt-states.md)

