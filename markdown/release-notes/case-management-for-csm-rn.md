---
title: Case management for CSM
description: The ServiceNow Case management application enables customer service organizations and support teams to collaborate on customer problems proactively to resolve issues. See the following sections for release notes by version.The September 2026 release adds an AI agent that drafts task plan templates from documents and diagrams, and gives templates more control with advanced conditions, record tracing, and extended dependency and document reference support for cloning and the multi-case generator.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/case-management-for-csm-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Customer Service Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Case management for CSM

The ServiceNow® Case management application enables customer service organizations and support teams to collaborate on customer problems proactively to resolve issues. See the following sections for release notes by version.

## About Case management for CSM

-   Case management provides a structured, efficient framework for handling customer service requests, incidents, and inquiries from initiation through resolution, keeping service delivery consistent and timely.
-   Configure case types and service definitions to route customer issues to the right process, connecting products and services to the appropriate case type so agents can resolve issues efficiently.
-   Create and work cases as needed, using tools such as case tasks, work orders, SLA definitions, and knowledge and community content to support resolution.
-   Configure Case form views, major issue management, and special handling notes to tailor the case experience and keep agents informed of important case details.

See [Case management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/case-management.md) for more information.

## Activation and other requirements

-   **Activation information**

    The Case Management Core plugin \(com.sn\_customerservice\) for CSM is available with activation of the Customer Service plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/t_ActivateCustomerService.md).


**Parent Topic:**[Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/customer-service-mgmt-rn-landing.md)

## Version 1.0

The September 2026 release adds an AI agent that drafts task plan templates from documents and diagrams, and gives templates more control with advanced conditions, record tracing, and extended dependency and document reference support for cloning and the multi-case generator.

### What's new

-   **AI-drafted task plan templates from documents and diagrams**

    Generate a draft task plan template from an uploaded SOP, flowchart, or process diagram using the new AI agent, so you can start from existing process documentation instead of building a template from scratch.


### What's changed

-   **Advanced conditions on template items**

    Apply conditions to template items based on related-record data using the new Advanced mode on the template item condition form. Define the relationship with the Base table, Base table mapping field, and Condition table mapping field fields.

-   **Trace generated records to their source template**

    Trace generated records back to the template item, execution, and service organization that created so you can tell which template produced which record.

-   **Cascade configuration updates to linked template items**

    Apply a Template Item Configuration change to every template item linked to it using the new cascade confirmation prompt, so you don't have to update item individually.

-   **Clone task plan templates and items with dependencies and document references intact**

    Clone a task plan template or template item to carry over its service organizations, dependencies, and document references, so the copy is usable without rebuilding those links.

-   **Dependencies and document references extended to the multi-case generator**

    Generate records with the multi-case generator to create their task dependencies and document references at the same time, including when you clone.


### Plugin information

-   **Renamed or changed plugins**

    Customer Service \(com.sn\_customerservice\): Renamed to Case Management Core \(com.sn\_customerservice\)

    CSM Extension for Proxy Contacts \(com.snc.csm\_proxy\_contacts\): Renamed to Customer Proxy Contacts \(com.snc.csm\_proxy\_contacts\)


