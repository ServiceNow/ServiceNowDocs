---
title: Domain separation and Decision Builder
description: This is an overview of domain separation as it pertains to Decision Builder. Domain separation allows you to separate data, processes, and administrative tasks into logical groupings called domains. You can then control several aspects of this separation, including which users can see and access data.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Decision tables reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Domain separation and Decision Builder

This is an overview of domain separation as it pertains to Decision Builder. Domain separation allows you to separate data, processes, and administrative tasks into logical groupings called domains. You can then control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes **Basic** level support.
-   Business logic: Processes can be created or modified per customer by the service provider \(SP\). The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The owner of the instance must be able to configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments mandatory when a record closes for one tenant but not for another.

## Domain separation in Decision Builder

-   Decision tables belong to the domain of the user who creates them. For example, when the customer in the TOP domain creates a decision table, it belongs to the TOP domain.
-   While users in a parent domain can see decision tables in a child domain, they must edit them in the domain they belong to. For example, an administrator in the TOP domain can see decision tables from the ACME domain but must switch to the ACME domain to edit it.

**Parent Topic:**[Decision tables reference](decision-builder-reference.md)

