---
title: Domain separation and Decision Builder
description: Domain separation in Decision Builder enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control which users can see and access data within each domain.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/domain-separation-decision-builder.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-07-22"
reading_time_minutes: 1
breadcrumb: [Decision tables reference, Decision tables, Workflow Studio, Build workflows]
---

# Domain separation and Decision Builder

Domain separation in Decision Builder enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control which users can see and access data within each domain.

## Support level: Standard

-   Includes **Basic** level support.
-   Business logic: Processes can be created or modified per customer by the service provider \(SP\). The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The owner of the instance must be able to configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments mandatory when a record closes for one tenant but not for another.

## Domain separation in Decision Builder

-   Decision tables belong to the domain of the user who creates them. For example, when the customer in the TOP domain creates a decision table, it belongs to the TOP domain.
-   While users in a parent domain can see decision tables in a child domain, they must edit them in the domain they belong to. For example, an administrator in the TOP domain can see decision tables from the ACME domain but must switch to the ACME domain to edit it.

**Parent Topic:**[Decision tables reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/decision-builder-reference.md)

