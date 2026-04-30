---
title: Sourcing and Procurement Operations integration with Project Management
description: Eliminate manual efforts of linking purchase orders to projects by integrating Sourcing and Procurement Operations with Strategic Portfolio Management's Project Management.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Integrating Sourcing and Procurement Operations with other applications, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Sourcing and Procurement Operations integration with Project Management

Eliminate manual efforts of linking purchase orders to projects by integrating Sourcing and Procurement Operations with Strategic Portfolio Management's Project Management.

The Project Costing for Sourcing and Procurement Operations plugin \(sn\_spend\_ppm\) provides this integration. This plugin has dependency on the following applications that can be purchased separately:

-   Sourcing and Purchasing Automation
-   Source-to-Pay Common Architecture
-   Finance Common Architecture
-   Common Service Delivery
-   Procurement Case Management
-   Source-to-Pay Workspace
-   Supplier Common Architecture
-   Playbook Experience
-   Document Templates
-   Common Vendor Core

The plugin also has dependency on the following system plugins that need to be installed separately:

-   External User Self-Registration
-   Finance Applications - Common Dependencies
-   Fiscal Calendar
-   GraphQL Plugin
-   Insert Multiple Web Service
-   PPM Standard
-   Process Automation Designer Core
-   Process Automation Designer for App Engine
-   Scoped Application Restricted Caller Access
-   Signature Pad
-   User Criteria Scoped API
-   Vendor Core

**Important:** Your administrator must manually assign the IT Project User, which is a licensed role, to your shopper for them to view project details during checkout. Also, as part of the Source-to-Pay pricing initiative, your administrator must manually assign the PPM user role to your procurement specialist.

With this integration, project managers or shoppers can associate a purchase with a project, which provides the reason for making the purchase, but also automatically creates cost plans and expense lines for that project. This enables project managers, shoppers, and procurement specialists to easily track planned costs each time a purchase is made for a Project Management project, and realize actual costs each time an invoice is paid for a Project Management project purchase.

## Impact on checkout and purchase details

When this application is installed, you must answer the additional question **Is this a purchase for an existing project?** during checkout. If your answer is in the affirmative, you must select your project from the list to proceed with the checkout.

Each project name is associated with a demand number, both of which are then auto-populated in the **Purchase Reason** field. You can add more information in the **Purchase Reason** field if you want to. On completing your checkout, these details are displayed on the purchase details page.

**Note:**

-   If this purchase isn’t made for an existing project, you must mention the reason for purchase in the **Purchase Reason** field to proceed with the checkout.
-   During full checkout, you can select a project for the entire purchase or individually at the product level.
-   You can’t select a project for a credit purchase.

## Impact on purchase request line and purchase order line tables

When a purchase request is created, you can configure the Purchasing Details form layout on the purchase request line table to display the **Project** field. This field references the selected demand record. Similarly, when a purchase request line is converted to a purchase order line, you can configure the Summary Details form layout on the purchase order line table to display the same **Project** field.

As part of this integration, whenever a purchase is ordered as part of a demand or project, a cost plan is automatically created in association with that purchase order line. You can configure the Summary Details form layout on the purchase order line to display the new **Cost plan** field. A Purchase Order Lines related list is also added to the corresponding cost plan record. On the Cost Plan form, the **Total planned cost** field is auto-populated based on when the purchase order had been generated. The **Total actual cost** field is populated based on invoice and expense line creation.

For information on how to configure a form layout, see [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Impact on invoice line and expense line tables

When an invoice is created, and both the invoice and the invoice line are in the Paid state, an expense line is automatically created for the project. This expense line has an Invoice Lines related list reference.

For more information on invoice creation, see [Invoices](../reference/invoices.md).

## Impact of demand and project lifecycle on Sourcing and Procurement Operations flows

When a demand is converted to a project as part of demand and project lifecycle:

-   The demand number isn’t available for selection during checkout.
-   When a purchase request line using that demand number is converted to a purchase order line, the latter references the project and not the demand number.
-   The cost plan references the newly created project and not the one initially selected by the shopper.
-   When an invoice is created, the associated expense line references the project and not the demand number.

When a demand or project is in a closed state:

-   The demand or project number isn’t available for selection during checkout.
-   Cost plans and expense lines aren’t created for closed demands and projects. However, if a cost plan is already created for a closed demand or project, expense lines continue to be auto-generated until all the invoices are paid out.

## Impact on sourcing request

When requesting pricing for a product that doesn’t have pricing available, you must answer the additional question **Is this a purchase for an existing project?**. If your answer is in the affirmative, you must select your project from the list to proceed with submitting the request. On successful submission, the project and demand details are displayed on the sourcing request record.

As a shopper, you can compare the pricing for your purchase, select a supplier, and proceed to checkout.

## Impact on off-catalog purchase request

When requesting a quote for a product that is not available on the Shopping Hub catalog, you must answer the additional question **Is this a purchase for an existing project?**. If your answer is in the affirmative, you must select your project from the list to proceed with submitting the request.

## Email notifications

When a purchase order associated to a demand or project is created, updated, or canceled, the assigned demand manager or project manager gets an email notification about its impacts on the cost plans of the demand or project.

**Parent Topic:**[Integrating Sourcing and Procurement Operations with other applications](integrating-spo.md)

**Related topics**  


[Sourcing and Procurement Operations integration with Employee Center](employee-center-integration-psm.md)

[Sourcing and Procurement Operations integration with third-party sourcing solutions](psm-integration-third-party-sourcing.md)

[Sourcing and Procurement Operations integration with Third-party Risk Management](better-together-with-vrm.md)

[Sourcing and Procurement Operations integration with Celonis](integration-psm-celonis.md)

[Sourcing and Procurement Operations integration with Field Service Management](integration-psm-fsm.md)

[Source-to-Pay Operations integration with Contract Management Pro](integration-spo-cmpro.md)

[ERP source validation on Sourcing and Procurement Operations objects](../reference/erp-source-val-spo-objects.md)

[Spendint API](../../../integrate/inbound-rest/concept/spendint-api.md)

[Procurement File Transfer Framework](procurement-file-transfer-framework.md)

