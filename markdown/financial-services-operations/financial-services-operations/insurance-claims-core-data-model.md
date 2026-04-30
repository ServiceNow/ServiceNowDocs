---
title: Insurance Claims Core
description: The Insurance Claims Core application includes a framework that provides generic claims data model components and approval engine that your organization can use to create flexible data structures that meet your business needs.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
---

# Insurance Claims Core

The Insurance Claims Core application includes a framework that provides generic claims data model components and approval engine that your organization can use to create flexible data structures that meet your business needs.

## Introduction to Insurance Claims Core

The Insurance Claims Core application includes all the required common entities in an insurance claim process for your different lines of business. A financial institution can use these common entities for all the other applications that relate to insurance claims. The main components in the Insurance Claims Core application are the data model such as the claim property, claim participant, claim coverage, claim reserve, and claim payment, approval engine and validations.

The claim reserve and claim payment components have a claims approval engine for approval process. This approval engine consists of decision tables and flows along with ServiceNow AI Platform `sysapproval_approver` table to ensure that the requests are accurate and monitored as per your company guidelines.

-   **[Insurance Claims Core tables](insurance-claims-core-tables.md)**  
This section explains the insurance tables in Insurance Claims Core and how they handle insurance data.
-   **[Insurance Claims Core roles and properties](insurance-claims-core-roles-and-properties.md)**  
This section outlines the core roles involved in managing insurance claims and highlights their system properties.
-   **[Approval Engine for Reserves and Payments](../concept/approval-engine-for-reserves-and-payments.md)**  
Insurance claims core includes a claim reserve and payment approval rules engine. It can be found in the decision table **Claim reserve and payment approval rules**.

**Parent Topic:**[Data Model](data-models.md)

