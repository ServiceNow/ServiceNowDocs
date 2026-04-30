---
title: Exploring Legal Request Management
description: Legal Request Management enables authorized employees in the organization to submit legal requests and to track their progress while users in the legal department with appropriate roles can work to resolve these requests.
locale: en-US
release: yokohama
product: Legal Request Management
classification: legal-request-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Legal Request Management, Legal Service Delivery, Employee Service Management]
---

# Exploring Legal Request Management

Legal Request Management enables authorized employees in the organization to submit legal requests and to track their progress while users in the legal department with appropriate roles can work to resolve these requests.

## Legal Request Management overview

Employees can read legal knowledge base articles, submit legal requests, monitor the progress of submitted requests, and interact through [Virtual Agent](legal-va-conversations.md).

![Transform and modernize your internal Legal operations through Legal Service Delivery applications.](../image/legal-service-delivery-info.png "Legal Service Delivery")

## Legal Request Management users

|User|Description|
|----|-----------|
|Legal Configurator|Legal Configurator configures data such as practice area, category, and legal matter templates.|
|Legal Fulfiller|Legal Fulfiller works on assigned legal requests and matters.|
|Legal User|Legal User submits legal requests and tracks their progress. Can work on assigned tasks related to matters.|

## Legal Request Management configuration workflow

The following sample end-to-end workflow shows how different users can work together to configure the foundation data and submit, review, and legal requests and matters.

1.  Administrator configures a practice area table.
2.  Legal Catalog Administrator creates a legal catalog category
3.  Legal Configurator performs the following actions:
    1.  Creates a practice area.
    2.  Adds an intake form to a practice area.
4.  Legal Configurator or Matter Configurator create a rule to automatically assign legal requests or matters.
5.  Legal Administrator activates a system property to close a long-running legal request.
6.  Request Configurator performs the following actions:
    1.  Creates a record producer for legal services, using Catalog builder.
    2.  Configures an external storage system for legal requests and legal matters.
7.  Legal Configurator creates or modify a response template for legal services.
8.  Administrator performs the following actions:
    1.  Configures an Action for legal services on the Standard ticket page
    2.  Enables and configures AI Search in Legal Service Portal

## Legal request and legal matter workflow

A workflow for a legal request might progress as following:

1.  Legal User submits a legal request.
2.  Legal Fulfiller performs the following actions as required:
    1.  Assigns the legal request.
    2.  Manages attachments for a legal request.
    3.  Initiates an ad hoc approval for a legal request or its attachment.
    4.  If required, promotes a legal request to a legal matter.
3.  If required Request Fulfiller can transfer a legal request.
4.  Legal Fulfiller closes the legal request on fulfilling it.

## Legal Request Management benefits

<table id="table_psf_nnn_tdc"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Remove manual, unstructured email processes and tasks with an easily accessed self-service experience

</td><td>

[Legal Request Management](../reference/legal-request-management-landing-page.md)

</td><td>

-   Legal Configurator
-   Legal Administrator, Legal Fulfiller
-   Legal User
-   Legal Catalog Administrator
-   Request Configurator

</td></tr><tr><td>

Automate responses for common legal requests with virtual agents

</td><td>

[Legal Virtual Agent Conversations](legal-va-conversations.md)

</td><td>

Legal Fulfiller

</td></tr><tr><td>

Make meaningful decisions by gaining real-time visibility on legal service demands

</td><td>

[Analytics and Reporting Solutions for Legal Service Delivery](../../../use/application-content-packs/concept/legalsd-content-pack.md)

</td><td>

Practice Area Lead

</td></tr><tr><td>

Track, prioritize, and work on multiple requests concurrently with an optimized Legal Counsel Center

</td><td>

[Legal Counsel Center](legal-counsel-center-landing.md)

</td><td>

Legal Fulfiller

</td></tr></tbody>
</table>## What to explore next

To learn more about configuring and using Legal Request Management, see:

-   [Configuring Legal Request Management](legal-ops-administration.md)
-   [Using Legal Request Management](submitting-legal-request.md)
-   [Managing legal requests](managing-legal-request.md)
-   [Legal Request Management reference](../reference/legal-request-management-reference.md)

**Parent Topic:**[Legal Request Management](../reference/legal-request-management-landing-page.md)

