---
title: Exploring Technology Reference Model
description: Use the Technology Reference Model \(TRM\) feature in Enterprise Architecture to define the standards for your software and hardware products and manage unapproved products in your organization.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Exploring Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Exploring Technology Reference Model

Use the Technology Reference Model \(TRM\) feature in Enterprise Architecture to define the standards for your software and hardware products and manage unapproved products in your organization.

**Important:**

Starting with the Xanadu release, the legacy Technology Reference Model module has been deprecated from Enterprise Architecture \(formerly Application Portfolio Management\). However, if you’re an existing user of Enterprise Architecture \(formerly Application Portfolio Management\), you can still use the legacy Technology Reference Model module. If you’re a new activation user, the legacy Technology Reference Model module isn’t available.

You can leverage the same functionality by using the Enterprise Architecture Workspace. To learn more, see [Manage the Technology Reference Model in Enterprise Architecture Workspace](eaw-concept/eaw-managing-the-technology-portfolio.md).

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

## TRM Product Lifecycle

Each product in the TRM library is associated with a set of life-cycle phases with a start and end date. The life-cycle phases could be approved, unapproved, approved with constraints, Divest, and evaluation.

The TPM home page fetches all the business applications that are being used in your organization. It helps to review the status of the software that is being used. You can understand if any business application is using the software that is not part of the TRM or a software version that is not approved for production. For more information, see [Review the TRM lifecycle status in the Technology Portfolio Management page](../task/review-trm-status-tpm-view.md).

## TRM and other modules

**Warning:** TPM and TRM require installation of either SAM Foundation or SAM Professional. Before installing the SAM Foundation plugin, carefully review the [Software Asset Management Foundation plugin migration](https://www.servicenow.com/docs/access?context=c_SAMMigrationSAMF&version=australia&pubname=australia-it-service-management&ft:locale=en-US) documentation. Contact ServiceNow Support if you do not have either SAM Foundation or SAM Professional installed on your instance.

The TRM module uses a similar module to TPM to search in the TRM library. You can view the software that is part of the TRM library, and initiate a request to add the software or software version to the TRM library.

You can also use the TRM with the Software Asset Management \(SAM\) plugin. This plugin helps you to fetch or select the products and versions for the TRM library. You can also define your own software products when the Software Asset Management integration module is not available for your instance.

**Related topics**  


[Add or edit a TRM product request](../task/add-edit-trm-prod-req.md)

[Add or edit a TRM product lifecycle request](../task/add-edit-trm-lifecycle-req.md)

[Request a TRM product using the TRM Catalog](../task/add-trm-prod-business-app.md)

[Request a TRM product lifecycle using the TRM Catalog](../task/add-trm-using-business-app.md)

[Approve or reject a TRM product or product lifecycle request](../task/approve-reject-trm-request.md)

[Add or edit a TRM category](../task/add-edit-trm-category.md)

[View and edit your product requests](../task/view-my-prod-req.md)

[View and edit your product lifecycle requests](../task/view-my-prod-lifecycle-req.md)

[Add or edit a TRM phase](../task/define-trm-phases.md)

[Manage Technology Reference Model \(TRM\) technical debt](../task/trm-technical-debt-calc.md)

[Review the TRM lifecycle status in the Technology Portfolio Management page](../task/review-trm-status-tpm-view.md)

