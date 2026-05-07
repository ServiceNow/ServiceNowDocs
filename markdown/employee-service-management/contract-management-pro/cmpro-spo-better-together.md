---
title: Optimizing Sourcing and Procurement Operations through Contract Lifecycle Automation
description: This solution enables seamless collaboration between sourcing professionals and legal teams by embedding contract request workflows into the Sourcing and Procurement Operations workflow.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Explore, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Optimizing Sourcing and Procurement Operations through Contract Lifecycle Automation

This solution enables seamless collaboration between sourcing professionals and legal teams by embedding contract request workflows into the Sourcing and Procurement Operations workflow.

## Benefits of integrating Contract Management Pro and Sourcing and Procurement Operations

Using Sourcing and Procurement Operations and Contract Management Pro together provides the following benefits:

-   Streamline Procurement and Contracts: Seamlessly request and manage contracts directly within the procurement workspace.
-   Mitigate risk to the organization: Ensure contract compliance and consistency with pre-approved templates and proactive obligation management
-   Control spend with contract data: Optimize procurement cost with access to historical metadata through a robust contract repository
-   Boost legal team productivity: Utilize common contract processes like review and signature to boost productivity.
-   Reduce manual review work by using generative AI: Use AI to identify missing and non-standard clauses for reducing manual review work

|Feature|Sourcing and Procurement Operations|Contract Management Pro|All applications together|
|-------|-----------------------------------|-----------------------|-------------------------|
|Connected procurement workflows across systems|![Yes](../../../reuse/images/icon-check-mark-green.png)|![No](../../../reuse/images/icon-error-red-x.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|
|Omni-channel self-service for employees and suppliers|![Yes](../../../reuse/images/icon-check-mark-green.png)|![No](../../../reuse/images/icon-error-red-x.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|
|Non-standard and negotiated purchasing capabilities|![Yes](../../../reuse/images/icon-check-mark-green.png)|![No](../../../reuse/images/icon-error-red-x.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|
|Catalog access for goods and services requests|![Yes](../../../reuse/images/icon-check-mark-green.png)|![No](../../../reuse/images/icon-error-red-x.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|
|Automated procurement with supplier risk assessment|![Yes](../../../reuse/images/icon-check-mark-green.png)|![No](../../../reuse/images/icon-error-red-x.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|
|Interactive experiences for supplier engagement|![Yes](../../../reuse/images/icon-check-mark-green.png)|![No](../../../reuse/images/icon-error-red-x.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|
|Contract lifecycle management|![No](../../../reuse/images/icon-error-red-x.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|
|Contract document authoring|![No](../../../reuse/images/icon-error-red-x.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|
|Obligation Management|![No](../../../reuse/images/icon-error-red-x.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|
|Contract document Analysis using generative AI|![No](../../../reuse/images/icon-error-red-x.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|
|Contract document metadata extraction using generative AI|![No](../../../reuse/images/icon-error-red-x.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|![Yes](../../../reuse/images/icon-check-mark-green.png)|

Within the Source-to-Pay Workspace, Procurement Specialists can create contract requests for the following records:

-   Purchase requests
-   Purchase lines
-   Sourcing requests
-   Negotiations
-   Negotiation events

## Workflow for Sourcing and Procurement Operations and Contract Management Pro

The following figure shows an example workflow of how a procurement specialist and a contract fulfiller can use these applications to streamline collaboration with legal teams, enabling them to execute contracting tasks within the procurement workflow. It also provides procurement professionals with full visibility into contract progress, reducing delays and improving operational transparency.

![SPO - CM Pro workflow](../image/mmassest0021243-SPO-CMPro-workflow.png "The Sourcing and Procurement Operations and Contract Management Pro workflow")

In this workflow:

1.  The employee initiates a sourcing request from the Sourcing and Procurement Operations workspace.
2.  The procurement specialist reviews the sourcing request and initiates contract request.
3.  The contract fulfiller reviews contract terms and clauses.
4.  The contract fulfiller finalizes the contract document.
5.  The contract fulfiller send the contract document for signature.
6.  The contract document is signed.
7.  A contract repository record with signed contract document is created in Sourcing and Procurement Operations.

## User roles required for the Contract Management Pro and Sourcing and Procurement Operations better together solution

The following roles are required to initiate, view, and manage contract execution:

-   **Sourcing and purchasing viewer**: This is a new role provided within the **Contract specialist** assignment group. This role can be assigned to the contracting and procurement professionals to have read-only access into the purchase lines, sourcing requests, negotiations, and purchase requisitions.
-   **Contract fulfiller**: This is a licensed role for CM Pro. This role has to be explicitly assigned to the contracting and procurement professionals if they have to work on contract requests. Once assigned, they can work on the contract requests, leveraging all capabilities from CM Pro – obtaining contract signatures, authoring contracts, tracking revisions, and creating the contract documents to be stored in the contract repository.​
-   **Contract user**: This role is also provided within the **Contract specialist** assignment group and is required to initiate and track contract execution.

You can assign your procurement and contracting professionals to these roles as required.

## Requirements for integrating Sourcing and Procurement Operations and Contract Management Pro

1.  [Install Sourcing and Procurement Operations](https://www.servicenow.com/docs/access?context=activate-finance-spend-central&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US).
2.  [Install Contract Management Pro](../task/cncore-install-cmpro.md).
3.  [Integrate with Contract Management Pro](https://www.servicenow.com/docs/access?context=integrate-spo-with-cmpro&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US).

    **Note:** To use this application, a license is required for both Contract Management Pro and Sourcing and Procurement Operations.


## Get started with initiating contract request

Get started with initiating contract request by completing these tasks:

1.  [Configure Sourcing and Procurement Operations](https://www.servicenow.com/docs/access?context=configuring-spo&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US).
2.  Configuring Contract Management Pro
    -   **[Create a contract type](../task/cncore-create-contract-type.md)**

        Create a contract type for defining different types of contract requests and associate it to a contract model.

        Role:contract administrator.

    -   **[Configure templates for a contract and amendment request in Contract Management Pro](cncore-document-templates.md)**

        Create a contract template of type .docx that can be used when submitting a contract request to generate a standard contract with predefined content.

        Role:contract configurator.

    -   **[Configure dynamic clauses for contract templates](cncore-clause-and-cv.md)**

        Enable dynamic customized content in contract templates through clauses that contain clause variations for preset conditions.

        Role:contract configurator.

    -   **[Define an internal signatory rule](../task/cncore-define-internal-signers-rule.md)**

        Define a user as an internal signatory rule so that the signer can be added to a contract template to automatically add to the contract document for a request.

        Role:contract configurator.

    -   **[Create a contract configuration](../task/cncore-contract-config.md)**

        Define the contract repository where the contracts will be stored and map the data to be added to the contract document.

        Role:contract configurator.

3.  [Initiate a contract request](https://www.servicenow.com/docs/access?context=initiate-contract-request&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US).

