---
title: Integrating Innovation Management with Universal Request
description: Integration of Innovation Management with Universal Request extends the capabilities of Universal Request and enables your employees and agents to create an idea from a universal request.
locale: en-US
release: australia
product: Innovation Management
classification: innovation-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Innovation Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Integrating Innovation Management with Universal Request

Integration of Innovation Management with Universal Request extends the capabilities of Universal Request and enables your employees and agents to create an idea from a universal request.

Integrate Innovation Management with the Universal Request application to provide a consistent ticketing experience and facilitate inter-department request transfers.

A Universal Request is created from an Interaction Record or New Call record when an agent determines that a new task record must be created for any of the following reasons:

-   Resolve the Universal Request immediately without assigning it to a specific department.
-   Transfer the Universal Request to a different department by assigning it to a Tier 1 assignment group.

Universal Request serves as a parent record for other records created as child records, such as INC, HRC, and custom task types. It is also used for all cross-departmental reporting. For more information about universal request, see [Exploring Universal Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/universal-request-for-hr-service-delivery/explore-universal-request.md).

## Features

The integration provides the following functionalities:

-   Create an idea from a universal request: When a universal request is created, an agent analyses the request. If the request can result in a new product, feature, or change, the agent creates an idea from that universal request.

    The idea manager then reviews submitted ideas and, if necessary, requests more information, and then chooses to accept or reject the idea. Accepted ideas are then converted to a demand, epic, story, or feature.

    The relevant information of the universal request such as details from the **Short description** and **Description** fields are copied to the **Title** and **Idea Description** fields of the idea.

    Also, the idea created from the universal request becomes the primary ticket for the universal request and the **Primary Ticket** field is populated with the idea number.

-   Transfer the idea to another department with or without resolution: If the idea is rejected or cannot be implemented, the routing agent can transfer the idea to another department.

    When an idea is transferred to another department, the idea is closed and a new record is created. For example, a universal request related to HR process improvement can be converted to an idea and then transferred to the HR department as an HRC when the idea is deemed not feasible.

    **Note:** When the idea created from a universal request is transferred to another department, the resulting INC, HRC, or custom task becomes the primary ticket for the parent universal request.


## Plugin requirements

Activate the following plugins if you have the admin role. These plugins are not active by default, and you must install them to integrate Innovation Management with Universal Request applications.

-   PPM Standard plugin \(com.snc.financial\_planning\_pmo\).
-   Universal Request plugin \(com.snc.universal\_request\). For activation information, see [Activate Universal Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/universal-request-for-hr-service-delivery/activate-ur-plugin.md).

Activate other related plugins such as Human Resources Scoped App: Core \(com.sn\_hr\_core\), and Employee Center \(com.snc.employee\_center\) plugins to facilitate inter-department transfers of ideas.

-   **[Create an Idea from Universal Request](../task/create-idea-from-ur.md)**  
Create an idea from a universal request after initial evaluation for a new product, feature, enhancement, or change.
-   **[Idea state mapping](../task/idea-state-mapping.md)**  
Map your idea states to the Universal Request states to provide a better user experience during the idea state transition and to track the progress of the idea.
-   **[Transfer an Idea to another department](../task/transfer-idea-ur.md)**  
Transfer an idea to another department with or without resolution if the idea is rejected or cannot be implemented.

**Parent Topic:**[Innovation Management](innovation-management-landing.md)

