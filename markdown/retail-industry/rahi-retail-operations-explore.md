---
title: Exploring Retail
description: Whether you're starting or expanding your implementation of the Retail application, learn more about the features available to optimize your retail organization.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Retail]
---

# Exploring Retail

Whether you're starting or expanding your implementation of the Retail application, learn more about the features available to optimize your retail organization.

## Retail overview

The Retail applications streamline operations and optimize communication within retail organizations and with headquarters. By building on the existing functionalities of Customer Service Management and Field Service Management, this application optimizes workflows, improves coordination, and supports both frontline and backend operations to run smoothly and efficiently.

Retail overview 

Retail helps you accomplish the following:

-   Enable front-line employees and managers to report issues on behalf of the stores they're associated with.
-   Help reduce calls to the call center, reduce or eliminate truck rolls, and enable store-based case management.
-   Get better visibility into store performance, which can also drive improvement in metrics for store support.
-   Streamline task assignment from teams at headquarters\(HQ\) to multiple retail organizations at once.

## Retail users

|User|Description|
|----|-----------|
|Store Associate|Store associates who perform store tasks, organize the store, are often the first to notice and report issues, and engage with customers.|
|Store Manager|Store managers who manage the store, address issues, or request help from the central operations team if needed. If issues aren't resolved in time and manage staff and schedules, they step in to contact local vendors.|
|Regional Manager|Regional managers who oversee multiple retail locations, staying aware of issues and their resolution status across the area's hierarchy.|
|Area Manager|Area managers, also called market managers,who oversee multiple regions and stay aware of issues and resolution status across their store hierarchy.|
|Central Operations Support|Central Operations Support or the HQ Operations team who addresses store questions and needs, performs issue resolution, and interfaces with company field staff or third-party vendors in coordination with Store Manager. They’re responsible for creating tasks and standard operating procedures. They're acting as the fulfilling agent for cases routed to them, including the cases related to security, IT Service Management \(ITSM\), and Central Customer Support.|

For more information on the roles that come with Retail Core, see [.](rahi-retail-components-installed-retail-core.md)

## Retail workflow

![Diagram showing a common retail operations workflow.](../image/z-retail-workflow1.png "Retail")

Retail case types are designed to address various business needs and streamline workflows for store-level and HQ-driven task management. Each case type is essentially a new case application with its own table, workflows, and UI experience that drives the end-to-end flow from issue to resolution.

The case types available are:

-   [HQ communications case](rahi-retail-retail-hq-operations.md): Initiate and coordinate large-scale actions across multiple stores with the HQ communications case type in the Retail HQ operations plugin.
-   [Store inquiry case](rahi-retail-retail-store-services.md): Streamline the process for contacting HQ for store-to-HQ cases with the store inquiry case type in the Retail Store Services plugin, which provides a clearly defined workflow for resolution at HQ.
-   [In-store operations case](rahi-retail-retail-in-store-operations.md): Standardize the reporting, tracking, and resolution of in-store issues with the in-store operations case type in the Retail in-store operations plugin. This case type contributes to structured assignments of store cases and tasks, reducing the time to resolution.
-   [Customer complaint case](rahi-retail-retail-customer-complaint.md): Help ensure quick and efficient customer service resolutions by capturing store-related complaints from customers using the customer complaint case type in the Retail customer complaint plugin.

## Retail data model

|Benefit|Feature|
|-------|-------|
|Helps to create and maintain Retail organization and Retail specific attributes on it.|[Retail organization data model](rahi-retail-data-model.md)|
|Covers the unified data model of cases and tasks in Retail. It helps in solving the Retail workflows.|[Retail unified case and task data model](rahi-retail-retail-unified-cas-task-data-model.md)|

Retail data model also includes:

-   Retail task: A retail task is an operational activity in a retail environment that ensures smooth store functioning, customer satisfaction, and compliance. These tasks can be manual or system-generated and are typically part of broader workflows managed by HQ or regional teams.
-   In-store operations task: In-store operations task is used to support daily in-store activities. These tasks are typically tied to a store-level case and are executed by store associates or managers.

## What to explore next

To learn more about configuring and using Retail, see:

-   [Configuring Retail](rahi-retail-operations-configuring.md)
-   [Manage customer complaints](rahi-retail-manage-customer-complaints.md)
-   [Manage store inquiries](rahi-retail-manage-store-inquiries.md)
-   [Track cases and tasks from the Retail portal](rahi-retail-navigating-retail.md)
-   [Retail reference](rahi-retail-operations-reference.md)

-   **[Retail case overview](rahi-retail-case.md)**  
The Retail case table stores information about your retail case types and provides the base for retail case creation. This table extends the Customer Service Management case table. All fields utilized through Customer Service Management case remain intact.
-   **[Retail portal](rahi-retail-portal.md)**  
Retail portal provides an enhanced experience to use self-service tools, view cases, and gain visibility into metrics for your retail organizations.
-   **[Retail mobile application](rahi-retail-retail-mobile.md)**  
The Retail mobile plugin offers a customized mobile experience for retail operations, enabling frontline teams to manage efficiently store activities and resolve issues on the go. It provides real-time insights into key KPIs, supports issue tracking, and is compatible with both Android and iOS platforms.
-   **[Retail case types](rahi-retail-retail-case-types.md)**  
Retail case types are designed to address various business needs and streamline workflows for store-level and HQ-driven task management.
-   **[Retail store plans](rahi-retail-retail-multistore-operational-planning.md)**  
The Retail store plan provides a centralized way to plan, schedule, and manage operational work across multiple stores, giving HQ and regional teams full visibility while simplifying execution for store teams.

