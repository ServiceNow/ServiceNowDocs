---
title: Technology Reference Model
description: Use the Technology Reference Model \(TRM\) feature in Enterprise Architecture to define the standards for your software and hardware products and manage unapproved products in your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-portfolio-management/technology-reference-model-in-apm.html
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Explore, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Technology Reference Model

Use the Technology Reference Model \(TRM\) feature in Enterprise Architecture to define the standards for your software and hardware products and manage unapproved products in your organization.

**Important:**

Starting with the Xanadu release, the legacy Technology Reference Model module is moved to the Enterprise Architecture Workspace. To learn more, see [Managing the Technology Reference Model in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/eaw-managing-the-technology-portfolio.md).

## Overview and benefits of a TRM

In your business enterprise, using an unapproved software can create a risk to the organization. The risks can include the following:

-   Security risks: The software might be exposed to security issues.
-   Delivery risks: There might not be sufficient knowledge on how to support the software.
-   Legal risks: A business application might use the software in illegal ways.

You must define the standards for the software to be used. You must define the software versions that are permitted for use in your organization. Also, you must have a way to explore when a non-permitted software is being used within the organization and in which business applications.

Use the TRM module in the Application Portfolio Management to do the following:

-   Approve or restrict the use of a software product within the organization.
-   Define how versions of the software can be used within the organization.
-   Request an introduction of a new software or the business applications, as new requirements arise.
-   Maintain TRM library for your organization.

Using the TRM module, you can manage the standards of the technology and set the right guardrail for technology usage. Setting the standards can improve the technical debt, security posture and save costs for the organization.

\[Omitted image "TRM-products-view.png"\] Alt text: TRM products view

## TRM Product Lifecycle

Each product in the TRM library is associated with a set of life-cycle phases with a start and end date. The life-cycle phases could be approved, unapproved, approved with constraints, Divest, and evaluation.

The TLM home page fetches all the business applications that are being used in your organization. It helps to review the status of the software that is being used. You can understand if any business application is using the software that is not part of the TRM or a software version that is not approved for production. For more information, see [Review TRM lifecycle status in TPM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/review-trm-status-tpm-view.md).

## TRM and other modules

**Warning:** TPM and TRM require installation of either SAM Foundation or SAM Professional. Before installing the SAM Foundation plugin, carefully review the [Software Asset Management Foundation plugin migration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/c_SAMMigrationSAMF.md) documentation. Contact ServiceNow Support if you do not have either SAM Foundation or SAM Professional installed on your instance.

The TRM module uses a similar module to TLM to search in the TRM library. You can view the software that is part of the TRM library, and initiate a request to add the software or software version to the TRM library.

You can also use the TRM with the Software Asset Management \(SAM\) plugin. This plugin helps you to fetch or select the products and versions for the TRM library. You can also define your own software products when the Software Asset Management integration module is not available for your instance.

**Related topics**  


[Add or edit a TRM product request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/add-edit-trm-prod-req.md)

[Add or edit a TRM product lifecycle request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/add-edit-trm-lifecycle-req.md)

[Request a TRM product using the TRM Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/add-trm-prod-business-app.md)

[Request a TRM product lifecycle using the TRM Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/add-trm-using-business-app.md)

[Approve or reject a TRM product or product lifecycle request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/approve-reject-trm-request.md)

[Add or edit a TRM category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/add-edit-trm-category.md)

[View and edit your product requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/view-my-prod-req.md)

[View and edit your product lifecycle requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/view-my-prod-lifecycle-req.md)

[Add or edit a TRM phase](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/define-trm-phases.md)

[Manage Technology Reference Model \(TRM\) technical debt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/trm-technical-debt-calc.md)

[Review TRM lifecycle status in TPM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/review-trm-status-tpm-view.md)

