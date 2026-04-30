---
title: Sales contract review requests
description: Sales team members can submit legal requests for sales contract review when they have to engage legal counsel for customer queries, review the terms and conditions provided by customers, or for legal guidance. The commercial legal team can review the sales contract and provide the requested contract support.
locale: en-US
release: xanadu
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Employee Service Management]
---

# Sales contract review requests

Sales team members can submit legal requests for sales contract review when they have to engage legal counsel for customer queries, review the terms and conditions provided by customers, or for legal guidance. The commercial legal team can review the sales contract and provide the requested contract support.

## Features

-   Routing requests to the legal team for changes to standard contracts and on-demand approvals for content changes.
-   Configurable deflection rules to provide predefined legal guidance based on the CRM data, such as account segment and opportunity size.
-   Ad hoc approvals for contract drafting.
-   Legal contracts repository containing metadata of signed contract documents.

## Setting up a sales contracts review request

The administrator must set up the following items for the sales team members to see their assigned sales accounts and opportunities while submitting legal requests for sales contract review:

-   [Configure Microsoft Dynamics CRM for sales contracts](../task/integrate-legal-ms-dynamics-crm.md)
-   [Schedule import set jobs to pull data from the CRM system](../task/schedule-import-sales-contract-crm.md)
-   [Create a deflection rule for sales contracts](../task/create-contract-deflection-rule.md)

## Sales contracts review request - Workflow

As a sales team member, you can submit a legal request for getting legal support on sales contracts for the sales opportunities or accounts you own. On clicking the **Submit** button, the system checks for a deflection rule to match its defined conditions with the information entered in the request.

-   If the conditions in any deflection rules do not match the details of the request, the legal request is submitted and assigned to the legal sales contract group.
-   If the conditions of a deflection rule match the details of the request, the preconfigured legal guidance text appears in a dialog box. You can choose to take one of the following actions:
    -   Follow the guidance and cancel submitting the Legal request.
    -   Provide appropriate reasons in **Business justification** and submit the request.

The legal department can manage and process these requested changes to make necessary revisions to the contract document from a centralized location.

![Legal Simple Contracts - Sales contracts review request workflow.](../image/workflow-sales-contract.png "Legal Simple Contracts - Non-disclosure Agreement workflow")

-   **[Submit a legal request for sales contract review](../task/submit-legal-request-sales-contract-review.md)**  
Submit a legal request to the legal team for review and legal support for a sales contract.
-   **[Work on a sales contract review request](../task/work-legal-request-sales-contract.md)**  
As a member of the legal contracts support team, review and revise a sales contract document as per the requested changes. Upload the revised document to the request and send it to the requester directly from the request.

**Parent Topic:**[Legal Simple Contracts](../reference/legal-simple-contracts-landing-page.md)

