---
title: Exploring Universal Request
description: The ServiceNow Universal Request application enables cross-departmental reporting from the time of an initial employee request through the final issue resolution. You can map various departmental ticket states and activity streams into a unified and simplified experience for your employees and agents.
locale: en-US
release: xanadu
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Universal Request, Employee Service Management]
---

# Exploring Universal Request

The ServiceNow Universal Request application enables cross-departmental reporting from the time of an initial employee request through the final issue resolution. You can map various departmental ticket states and activity streams into a unified and simplified experience for your employees and agents.

Universal Request application supports the following two most common ESM or GBS service delivery models.

## Cross-departmental Tier 1 support desk

If your organization has a cross-trained group of Tier 1 agents to resolve routine requests, then you can use this support desk model. In this model, universal requests are assigned to the cross-departmental tier 1 support desk agents to triage, resolve, or forward unresolved requests to a higher support level within a specific department.

![Cross-departmental Tier 1 support desk model](../images/ur-landing-graphics.png)

## Embedded Tier 1 Support Desks

If your organization has tier 1 agents in each department, such as IT, HR, and Finance, then you can use this support desk model. In this model, universal requests are routed to the appropriate departmental tier 1 agents who resolve, escalate, or transfer the requests to the correct department.

![Embedded Tier 1 support desk model](../images/ur-landing-tier1-embedded.png)

The Universal Request application provides the following key benefits to employees and agents of your organization:

-   Facilitates employees to create a request by just clicking **Request Help** in the Service Portal if they cannot find the relevant search results or are unsure of which department to contact for help.
-   Provides a consistent and unified ticket page experience to employees across service departments.
-   Enables agents to effectively resolve a case or request through cross-departmental interactions rather than working in silos.
-   Provide an end-to-end user experience with complete visibility to the case details.
-   Enables ticket transfers across departments or between a Tier-1 support desk and higher-level departmental support teams, with enhanced security.
-   Enables agents to task employees using the Universal Task application to complete a catalog item or upload a document to facilitate quick resolution of a request.
-   Monitor and improve the end-to-end experience with cross-departmental SLAs and metrics.

-   **[Universal Request versus Interaction Records \(New Call record\)](ur-versus-ir.md)**  
Universal request and interaction records are created and used by agents of various departments. However, they differ in the way they are handled. The following information provides an overview of both the records and how they differ from each other.
-   **[Universal Request data model](UR-datamodel.md)**  
Universal Request is a task type that supports cross-departmental collaboration and unified employee experience. Universal Request becomes the parent record for departmental primary tickets, such as IT incidents and HR cases, and enables your organization to measure cross-departmental SLAs and OLAs.
-   **[Universal Request roles and groups](ur-roles.md)**  
Users with certain roles and access can use Universal Request.
-   **[Universal Request states and reasons](ur-states.md)**  
The Universal Request \(UR\) state is determined by the state of the primary ticket. The primary ticket for a UR is a child department ticket, such as an IT incident or a HR case. A Universal Request can have only one primary ticket at a time.
-   **[Mobile experience for Universal Request](ur-mobile-exp.md)**  
Create universal requests from a mobile device using the Now Mobile application. Stay connected and access information in real time.

**Parent Topic:**[Universal Request](ur-landing-limitedaccess.md)

