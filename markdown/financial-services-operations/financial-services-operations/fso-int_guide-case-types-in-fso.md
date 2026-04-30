---
title: Case Types in FSO
description: Learn about case types, how they’re structured, and how they’re used in Financial Services Operations \(FSO\).
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-22"
reading_time_minutes: 2
---

# Case Types in FSO

Learn about case types, how they’re structured, and how they’re used in Financial Services Operations \(FSO\).

A case type represents the processes and data needed to resolve a specific type of customer issue. Use case types to create and configure the different types of customer service cases for your organization.

For example, in the banking industry customer service agents can use case types to capture different servicing requests, such as loans, credit cards or managing complaints.

In Loan Operations, there are two primary case types: business-to-consumer \(B2C\) and business-to-business \(B2B\). In this implementation, there are separate case types for loans because they are in different domains and there isn’t an existing application to leverage. The B2C cases are also separated from the B2B cases due to the agents that work on the different requests. Banks also need clear separation of these case types for regulatory requirements.

**Note:** FSO implementations should use case types even when not using a base system application. Even if there’s no need for multiple case types, you should still start with one case type. This type of implementation enables easy adoption of future case types from either FSO applications or custom applications.

## Case type hierarchy

FSO implements hierarchical case types to provide the data model, roles, business rules, and associated workflows that closely align with different domains of financial institutions \(FIs\). The FSO Base Case case type, which extends CSM Case, provides functionalities like the data model, roles, and business rules that are applicable to a bank or insurance company.

## Primary and domain-specific case types

FSO applications are separated into primary case types that extend FSO Base Case. These case types align with business functions and industry standards like those by the Banking Industry Architecture Network \(BIAN\). Primary case types enable better querying and reporting, and provide subdomain-specific fields, field labels, and so on.  Standard components are prebuilt for each domain, which provide logical groupings by core banking and insurance domains, with preconfigured personas, roles, and ACLs. This structure makes it easier for FIs to implement domain-specific rules.

FSO domain-specific case types are further extended to the product/lines of business. Domain-specific case types enable separation of services and different fulfillers \(that is, processors\) or defined roles that interact with each case type. Granular case types enable FIs to build a tailored user experience with dedicated workspaces. If the business wants to implement access controls, it also provides an easier way to segregate access and visibility to the data.

**Parent Topic:**[Using case types and service definitions in FSO](fso-int_guide-work_case_types.md)

