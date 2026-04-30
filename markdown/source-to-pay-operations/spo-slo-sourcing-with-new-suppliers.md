---
title: End-to-end sourcing and supplier onboarding workflow in Source-to-Pay Operations
description: With Sourcing and Procurement Operations and Supplier Lifecycle Operations together, provide complete visibility to all the stakeholders involved in the sourcing process, along with improved supplier onboarding experience.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [sourcing request, supplier onboarding, sourcing workflow, procurement operations, supplier lifecycle, product sourcing, supplier management, onboarding suppliers, sourcing and procurement operations, supplier lifecycle operations]
breadcrumb: [Purchasing and sourcing workflows, Source-to-Pay Operations, Finance and Supply Chain]
---

# End-to-end sourcing and supplier onboarding workflow in Source-to-Pay Operations

With Sourcing and Procurement Operations and Supplier Lifecycle Operations together, provide complete visibility to all the stakeholders involved in the sourcing process, along with improved supplier onboarding experience.

## How sourcing and supplier onboarding works

The following figure shows how an employee, procurement specialist, supplier manager, and supplier use the SPO and SLO applications together to get complete visibility into the sourcing process and simultaneously enjoy improved supplier onboarding experience.

![Workflow of the sourcing experience](../../product/sourcing-procurement-operations/image/spo-slo-sourcing-new-supplier.png "Workflow for sourcing and supplier onboarding")

In this workflow:

1.  An employee visits Shopping Hub \(or Employee Center\) and creates a sourcing request with a new supplier to be onboarded.
2.  Work assignment rules route the request to a procurement specialist's workspace.
3.  The procurement specialist initiates automated supplier qualification, which creates required cases, including a new supplier onboarding case that is assigned to a supplier manager.
4.  The supplier manager reviews the supplier onboarding case and uses the onboarding playbook in the supplier workspace to onboard suppliers.
5.  The playbook generates tasks and assigns them to the supplier being onboarded.
6.  The supplier contact views the assigned tasks in the Supplier Collaboration Portal.
7.  The supplier contact completes the assigned tasks and submits the required questionnaire in the Supplier Collaboration Portal.
8.  The supplier manager reviews the collected supplier data and completes the onboarding playbook in the supplier workspace.
9.  The employee, procurement specialist, and supplier manager have complete visibility into the status of work, including supplier onboarding, through process completion, from their respective portals.

## Requirements for sourcing with a new supplier

Install and activate these plugins.

-   Shopping Hub \[com.snc.sn\_spend\_uib\]
-   Sourcing and Purchasing Automation \[com.snc.sn\_pr\]
-   Procurement Case Management \[com.sn\_spend\_psd\]
-   Source-to-Pay Workspace \[com.sn\_spend\_workspace\]
-   Playbooks for Sourcing and Procurement Operations \[com.sn\_spend\_cp\]
-   Advanced Work Assignment for Sourcing and Procurement Operations \[com.snc.sn\_spend\_awa\]
-   Supplier Common Architecture \[com.snc.sn\_slm\]
-   Supplier Lifecycle Operations \[com.snc.sn\_supplier\_mgmt\]
-   Supplier Collaboration Portal \[com.snc.sn\_supplier\_sp\]
-   Advanced Work Assignment for Supplier Lifecycle Operations \[com.snc.sn\_slm\_awa\]
-   Source-to-Pay Common Architecture \[com.snc.sn\_shop\]
-   Finance Common Architecture \[com.sn\_fin\]
-   Common Service Delivery \[com.sn\_spend\_sdc\]
-   Risk Assessments Integration for Sourcing and Procurement Operations \[com.sn\_spend\_vrm\]

For information on the installation sequence, see [Application plugin installation sequence in Sourcing and Procurement Operations](../../product/sourcing-procurement-operations/reference/application-plugin-list.md).

## Get started with sourcing with a new supplier

To get started with sourcing with a new supplier, follow these steps:

1.  Request for a product or service that you don't see on Shopping Hub, and add a new supplier that you prefer to source it from. For more information, see [Requesting for products or services that you don't see on ShoppingHub](../../product/sourcing-procurement-operations/concept/request-prod-serv-dont-see-sh.md).

    Role: sn\_shop.shopper.

2.  Review the sourcing request and its associated purchase lines on the Source-to-Pay Workspace. For more information, see [SPO list page](../../product/sourcing-procurement-operations/concept/procurement-specialist-list-page.md).

    Role: sn\_shop.procurement\_specialist.

3.  Begin the qualification process to onboard the new supplier. For more information, see [Supplier qualification](../../product/sourcing-procurement-operations/reference/supplier-qualification.md).

    Role: sn\_shop.procurement\_specialist.

4.  Review the supplier onboarding case and start the supplier onboarding using playbooks. For more information, see [Use the supplier onboarding playbook to onboard suppliers](../../product/supplier-lifecycle-operations/concept/use-playbooks-onboard-supp.md#).

    Role: sn\_slm.manager.

5.  The playbook automatically creates supplier tasks to conduct risk assessment and to collect supplier information, such as banking information and location details.
6.  Log in to the Supplier Collaboration Portal and complete the following:

    -   Assigned tasks. For more information, see [Viewing supplier contact tasks from the Supplier Collaboration Portal](../../product/supplier-lifecycle-operations/concept/my-to-dos.md).
    -   Risk assessment questionnaire. For more information, see [Complete a risk assessment from the Supplier Collaboration Portal](../../product/supplier-lifecycle-operations/task/complete-risk-assessments.md).
    Role: sn\_slm.contact.

7.  Review the collected supplier information and determine whether to continue or cancel the onboarding process.

    Role: sn\_slm.manager.

8.  Complete the different activities in each stage of the playbook to successfully onboard the new supplier.

    Role: sn\_slm.manager.


