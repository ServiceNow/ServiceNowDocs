---
title: Contract Management Pro glossary
description: Learn about the terms and concepts used in Contract Management Pro.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/contract-management-pro-glossary.html
release: brazil
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 13
breadcrumb: [Reference, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Contract Management Pro glossary

Learn about the terms and concepts used in Contract Management Pro.

Glossary terms are grouped alphabetically.

[A](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/contract-management-pro-glossary.md) \| [C](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/contract-management-pro-glossary.md) \| [E](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/contract-management-pro-glossary.md) \| [M](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/contract-management-pro-glossary.md) \| [N](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/contract-management-pro-glossary.md) \| [O](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/contract-management-pro-glossary.md) \| [R](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/contract-management-pro-glossary.md) \| [S](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/contract-management-pro-glossary.md) \| [T](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/contract-management-pro-glossary.md) \| [W](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/contract-management-pro-glossary.md)

**Parent Topic:**[Contract Management Pro reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/contract-management-pro/cncore-ref.md)

**Related topics**  


[Components installed with Contract Management Pro]()

[Components installed with Contract Workspace]()

[Components installed with Analytics Pack for Contract Management Pro]()

[Contract request State and Contract document status in Contract Management Pro]()

[Amendment and renewal interaction messages]()

[Signatory roles]()

[Clause Variation form]()

[Contract Configuration form]()

[Properties installed to configure expiry notifications]()

[Properties installed to configure contracts integrations]()

[Expiring Contracts Condition form fields]()

[Action assignment form]()

[UFX Add on Event mapping form]()

[Obligation form]()

[Obligation Management notifications]()

[Contract Analysis Playbook form]()

[Contract analysis playbook tool messages]()

[Contract request ticket page actions]()

[Default availability of out-of-the-box record producers]()

[Contract Management solutions]()

## A

### Approval workflow

A predefined sequence of automated or manual steps that a contract must go through to receive necessary approvals before execution.

### audit trail

A record of all changes made to a contract.

### ad hoc obligation task

An obligation task in Contract Management Pro that is required only once or at irregular intervals to fulfill a contract obligation, created manually rather than on a schedule.

### AI Contract Administrator

A Contract Management Pro role that provides administrative access to Now Assist in Contract Management Pro, including installing the plugin and activating required skills.

### AI Contract Configurator

A Contract Management Pro role that configures the use case mappings for Now Assist in Contract Management Pro.

### AI Contract Fulfiller

A Contract Management Pro role that uses Now Assist in Contract Management Pro to analyze contract documents for deviations, extract metadata from signed contracts, and query the contract repository through conversational search.

### amendment request

A request type in Contract Management Pro used to modify an existing contract by adding, removing, or updating terms, without replacing the entire contract; supports both own-paper and third-party paper contracts.

## C

### clause management

The process of creating, storing, and managing standard contract clauses and their variations to ensure consistency and compliance.

### clause mapping

Mapping clauses to field groups and expected responses, which helps in automating the contract review process.

### clause library

A centralized repository within ServiceNow where standard contract clauses and their approved variations are stored for easy access and consistent usage.

### contract analysis

A Now Assist skill used to analyze contract documents for clause deviations, ensuring compliance with standard clauses and identifying potential risks

### content controls

Dynamic placeholders within Microsoft Word documents that integrate with ServiceNow for inserting and updating contract content.

### contract dashboard

A visual interface that provides an overview of contract statuses, key metrics, and performance indicators.

### Contract Lifecycle Management \(CLM\)

The end-to-end process of managing contracts from initiation through execution, performance monitoring, and renewal or termination.

### contract repository

A secure, centralized storage within ServiceNow where all contract documents and related information are stored, providing easy retrieval and management.

### contract workspace

A centralized interface within ServiceNow where contract-related activities are tracked and managed.

### contract templates

Predefined templates that are used to expedite the contract creation process and maintain consistency across agreements. These templates include placeholders for clauses, fields, dynamic tables, and signature blocks, which are automatically updated based on the information in a contract request.

### change request

In Contract Management Pro, a user-submitted request asking a contract fulfiller to revise a contract document's content, tracked through its own status; distinct from a ServiceNow ITSM change request.

### clause

In Contract Management Pro, a clause is a collection of clause variations, each containing a block of content; the applicable variation is selected automatically when a contract document is generated.

### clause variation

A version of a clause's content in Contract Management Pro that is inserted into a contract document only when its defined condition, such as a field value, user criteria, or script, is met.

### collaborator

A user added to a contract request in Contract Management Pro who can access and work on it like an assignee, but can't modify the Assigned to, Assignment group, or Assignment group permission fields.

### Contract Administrator

A Contract Management Pro role that provides administrative access to Contracts Core and its underlying data.

### Contract Analytics Pack

The plugin that installs the roles and scheduled jobs needed to activate and populate the Contract Dashboard in Contract Management Pro with contract volume, work-distribution, and renewal analytics.

### contract configuration

An admin record in Contract Management Pro that determines which contract template and contract repository are used to generate a contract document, based on conditions evaluated against the contract request.

### Contract Configurator

A Contract Management Pro role that provides access to configure data for contract templates and contract configurations, without access to transactional data.

### contract family hierarchy

The set of parent, child, sibling, and grandchild contract and amendment requests related to a contract request in Contract Management Pro, linked together with optional field inheritance and viewable in the Related Contract Requests tab.

### Contract Fulfiller

A Contract Management Pro role required to initiate actions while fulfilling an assigned contract execution, such as creating revisions, adding signers, or canceling a signer.

### contract history

An automatically maintained set of prior versions of a contract record in Contract Management Pro, created whenever the contract's end date or its terms and conditions change.

### contract reminder date

A date in Contract Management Pro that's automatically calculated from the contract end date, the presence of an auto-renewal clause, and the notice period, used to notify designated recipients about an upcoming contract renewal or termination.

### Contract Report Publisher

A Contract Management Pro role that provides restricted access to contract requests and signed contracts data for publishing related reports.

### Contract Report Viewer

A Contract Management Pro role that provides restricted access to view reports for contract requests and signed contracts data on the Contracts Dashboard.

### contract repository rule

A configurable rule in Contract Management Pro, tied to a contract repository field such as expiration level, that determines when automated actions like expiring-contract reminder emails are triggered.

### Contract Reviewer

A Contract Management Pro role that reviews contract documents, tracks review tasks, and uses the clause library to add appropriate clauses.

### contract status

A field on the contract request in Contract Management Pro that tracks the granular processing state of the contract document, such as awaiting approval or awaiting signature, tracked separately from the request's overall State field.

### contract template rule

A rule in Contract Management Pro that determines which contract document template is used to generate a document for a request, based on conditions and a priority order.

### Contract User

A Contract Management Pro role required to initiate and track contract and amendment requests.

### Contract Workspace Administrator

A Contract Management Pro role that grants administrators permission to change the Contract Workspace to fit business or user requirements.

### Contract Workspace User

A Contract Management Pro role that provides access to the Contract Workspace.

### Contracts Core

The underlying ServiceNow application that provides the foundational contract management capabilities used by Contract Management Pro, including clause variations, electronic signature requests, notifications, and external storage integration.

### Contracts PA Admin

A Contract Management Pro role that provides permission to activate and configure the Contract Analytics Pack application.

### Conversational Contract Search and Insights

A named skill in Contract Management Pro that lets users search and retrieve information from contracts using natural-language, dialogue-driven queries.

## E

### e-signature

A legally binding electronic method for signing contracts, with integrations available for providers such as DocuSign and Adobe Sign.

### employee center

A portal for submitting contract requests.

### external storage

Third-party cloud storage platforms such as OneDrive or Google Drive that can be integrated with ServiceNow for contract document management.

### expected response mapping

A Yes/No answer mapped to a field, or prompt question, within a Contract Management Pro contract analysis use case; AI compares its generated answer to the expected response to decide whether a clause is standard or non-standard.

### expiring contracts condition

A rule in Contract Management Pro that specifies when a contract-expiration email notification is triggered, based on a table field condition and the configured number of days before expiry.

## I

### internal signatory rule

A configuration in Contract Management Pro that automatically maps an internal user as a signatory on a contract document generated from a template, based on conditions such as assignment group; it takes precedence over participant-based mapping when both apply.

## M

### metadata extraction

A Now Assist skill used to extract metadata from signed contracts and add the information to the system, streamlining the data entry process

### Microsoft Word Add-in

A program that integrates with Microsoft Word that enables a user to add content controls for metadata, clauses, signature blocks, and dynamic tables.

### manage contract repository

The named agentic AI workflow in Contract Management Pro that runs after a contract is signed, using AI agents to extract key metadata and obligations from the signed contract and calculate the contract reminder date.

### modify signatories

An option in Contract Management Pro that pauses an in-progress contract signature process so a fulfiller can add, edit, reorder, or remove pending signatories; changes are automatically reverted if not resumed within a configured time window.

### multiple contracts

A contract request type in Contract Management Pro that supports more than one contract type or document within a single request, as opposed to a single contract, enabling actions like reclassifying documents between contract types.

## N

### non-self-served request

A contract request that requires legal team involvement for drafting, negotiation, or finalization of the contract.

### Now Assist in Contract Management Pro

A generative AI-powered feature that enhances productivity by suggesting contract clauses, and extracting metadata from a signed contract.

## O

### obligation

Specific commitments or duties outlined in a contract that parties are required to fulfill.

### obligation management

The process of tracking and managing obligations within ServiceNow to ensure compliance and timely execution.

### Optical Character Recognition \(OCR\)

A technology that converts scanned contract documents or PDFs into searchable and editable text within ServiceNow.

### own-paper request

A contract request initiated and managed by the requester where the contract document is created using templates and clauses that have already been verified and approved by the internal contract team, reducing dependency on legal teams and accelerating processing.

### Obligation Administrator

A Contract Management Pro role that provides administrative access to Obligation Management and its underlying data.

### Obligation Fulfiller

A Contract Management Pro role required to perform actions while managing an obligation, such as creating, approving, rejecting, or canceling obligation tasks.

### Obligation User

A Contract Management Pro role required to update and submit obligation tasks.

### offline signature

A signature type in Contract Management Pro recording that a contract was signed outside the application, such as on paper or via a third-party application; no signature-request emails are sent, and the signed document is uploaded directly.

## P

### participant

A placeholder configured in a Contract Management Pro contract template for a person who will later be assigned an action, such as filling, signing, or reviewing, on the generated document.

### playbook

A tab on a contract repository record in Contract Management Pro that opens a step-by-step interface where contract managers and fulfillers review, edit, approve, or reject AI-extracted metadata and obligations from a signed contract.

## R

### record producer

A catalog item that allows end users to create records from the Service Catalog.

### recurring obligation task

An obligation task in Contract Management Pro that is required at regular intervals to fulfill a contract obligation, generated automatically based on a defined schedule.

### regenerate

An action in Contract Management Pro that creates a new version of the contract document directly from the template with the latest metadata, signatories, and tables, discarding changes made in the previous revision.

## S

### self-served contract request

A contract request that is initiated and managed by the requester. The contract document is created by using templates and clauses that have already been verified and approved by the internal contract team. The self-served contract request reduces the dependency on legal teams and accelerates processing.

### ServiceNow Store

A marketplace where users can find and install applications, plugins, and enhancements for ServiceNow, including contract management extensions.

### Search Contracts AI Agent

The AI agent in Contract Management Pro that finds and interprets legal contracts and documents, returning results for natural-language questions as part of conversational search and Q&amp;A.

### signatory role

A configuration field in Contract Management Pro that assigns a signing role, such as Signer, Viewer, Receiver, or Approver, to a contract signatory; active only for contracts using the DocuSign electronic signature provider.

### signature block

A contract template mode in Contract Management Pro where signature fields are embedded directly in the document as an alternative to a participant-based template; the number of blocks generated is based on the signatories specified in the contract request.

### sync document

An action in Contract Management Pro that creates a new contract document revision with updated metadata and signatories while retaining edits made in the previous revision.

## T

### third-party contract request

A contract request that requires the legal team to draft, negotiate, or finalize the contract.

### table mapping

A contract template configuration in Contract Management Pro that links a data source table in the instance to a table placeholder in the template, so matching records are dynamically inserted into the generated contract document.

### template mapping

A contract template configuration in Contract Management Pro that pre-fills metadata, signature, and signatory values into the generated document based on fields tagged with content control prefixes, distinct from AI-driven metadata extraction.

## W

### wet signature

A traditional handwritten signature on a physical contract document, sometimes required for compliance or regulatory purposes.

