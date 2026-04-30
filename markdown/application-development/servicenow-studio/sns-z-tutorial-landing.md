---
title: ServiceNow Studio tutorial: Zurich
description: Use this tutorial to help you create an application in ServiceNow Studio.
locale: en-US
release: zurich
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Explore, ServiceNow Studio, Developing your application, Building applications]
---

# ServiceNow Studio tutorial: Zurich

Use this tutorial to help you create an application in ServiceNow Studio.

The powerful ServiceNow AI Platform is designed to streamline and automate business processes. While out-of-the-box solutions provide a great starting point, they may not always align with your specific business requirements. In such cases, building a custom application using App Engine can be the best approach, offering flexibility, scalability, and tailored functionality to meet your organization's unique needs.

This tutorial is structured into three phases, showcasing how to rapidly build an application to deliver business value and then expand upon it after the initial release. The application developed in this tutorial enables efficient, structured service management for a team or department. It includes service request functionality and provides users with a streamlined way to submit issues or inquiries.

## Use case overview

When considering whether to build a custom application on the ServiceNow AI Platform, it is important to evaluate product workflows first. In general, it is best practice to use pre-built workflows when their value chain aligns with business needs. Conversely, if a pre-built workflow is not designed for a specific purpose, it is better to build a custom application rather than over-customizing an existing one.

Departments that perform functions beyond the out-of-the-box capabilities of existing products are strong candidates for custom applications. This approach allows them to fully leverage the benefits of the ServiceNow AI Platform, including tailored data models, security, and user experiences specific to their unique use cases.

In this tutorial, we will build a custom application for a marketing department. We will start by creating a workflow to manage marketing design requests, then identify opportunities to enhance business value, improve user experiences, and ensure maintainability.

The basic workflow you will design in this tutorial is as follows:

1.  A Marketing design request is initiated.
2.  The request is assigned to a Design Manager.
3.  A Design Manager re-assigns the request to a junior or senior graphic designer.
4.  If the design is public facing, the approval is assigned to the Branding Team and the Marketing design request is complete.
5.  If the design is not public facing, the Marketing design request is complete.

## Application design process overview

![Begin creating your app as an MVP, then automate and improve it, and then expand to a departmental solution.](../image/sns-z-tut-plan-flow.png)

1.  **Begin with a minimum viable product \(MVP\)**.

    The first part of the tutorial will focus on one the most common use cases, a request-fulfill workflow. The request-and-fulfill workflow is the backbone of ServiceNow applications, as it provides a structured mechanism for managing service requests and incidents. These workflows offer several key benefits:

    -   Efficiency and automation: Streamlines service request handling, reducing manual intervention
    -   Improved task management: Helps fulfillers track, prioritize, and complete requests effectively
    -   Enhanced user experience: Enables requester to submit and monitor requests with ease
    -   Scalability: Supports growing business needs by adapting to new service demands and departments
    In this phase you will build an MVP using ServiceNow Studio. The MVP will use a custom data model, record producer, and a custom workspace. You will use Workflow Studio to structure the workflow.

2.  **Automate and improve**.

    Simple request-fulfillment processes that are initially built using workflow elements such as approvals and tasks can quickly become inefficient as complexity increases. Manual approvals, inconsistent decision-making, and poor visibility into request statuses can slow down service delivery, frustrate employees, and ultimately impact business productivity.

    To address these challenges, ServiceNow offers playbooks and Decision Builder, two powerful features that enhance workflow automation, improve user experience, and ensure compliance with business policies.

    This second section will enhance the MVP with a playbook for step-by-step task guidance and improved user experience. A decision table will also be added to encapsulate business decisions and decouple the logic from the business process.

3.  **Expand to a departmental solution**.

    Your request-fulfillment application is the first step toward full automation—not just a standalone process. To maximize its impact, take a strategic approach to scaling workflow automation, improving efficiency, and streamlining service delivery to enhance and support the initial workflow. This expansion transforms the initial request process into a fully scalable departmental solution.

    The final section of the tutorial expands the request-fulfill process to a departmental solution by adding workflows and improving the workspace dashboard.

    The tutorial is structured into three phases to demonstrate quickly building an application to realize business value and then expanding after the initial release. The application structure built in this tutorial can be used to quickly provide structured service management for a group or department. The application provides for service request functionality as well as ways for service consumers to submit issues or questions.


-   **[ServiceNow Studio tutorial part 1: Begin with an MVP](sns-z-tutorial-begin-with-mvp.md)**  
In this section, you will build a minimum-viable-product \(MVP\) using ServiceNow Studio. The MVP will use a custom data model, record producer, and a custom workspace. You will also use Workflow Studio to structure the MVP's workflow.
-   **[ServiceNow Studio tutorial part 2: Automate and improve](sns-z-tutorial-automate-improve.md)**  
This section enhances the MVP with a playbook for step-by-step task guidance and improved user experience. A decision table will also be added to encapsulate business decisions and decouple the logic from the business process.
-   **[ServiceNow Studio tutorial part 3: Expand to a departmental solution](sns-z-tutorial-expand-departmental-solution.md)**  
Your first request-fulfill workflow is the first step toward full automation-not just a standalone process. To maximize its impact, take a strategic approach to scaling workflow automation, improving efficiency, and streamlining service delivery to enhance and support the initial workflow.
-   **[ServiceNow Studio tutorial part 4: Conclusion and review](sns-z-tutorial-conclusion-review.md)**  
Thank you for completing this ServiceNow Studio tutorial. This topic reviews some of what you learned through the tutorial.

**Parent Topic:**[Exploring ServiceNow Studio](exploring-servicenow-studio.md)

