---
title: Link generator for HR Service Delivery
description: Use the Link Generator to create a link on an HR case form that accesses information outside of the application to help fulfill the case.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Link generator for HR Service Delivery

Use the Link Generator to create a link on an HR case form that accesses information outside of the application to help fulfill the case.

Create links on the HR case form to payroll, social media, or to products to fulfill computer or software requests. Generate URLs to manage content, knowledge articles, and catalogs.

An example would be to create a link to a third-party HR application from the HR case form so HR agents can access additional profile information. Creating these types of links assume:

-   The HR agent has valid credentials to access a third-party HR application.
-   The link takes the HR agent directly to the profile information in the third-party HR application and not to the home page.

The **Human Resources Scoped App: Core \[com.sn\_hr\_core\]** plugin activates the **Link Generator \[com.snc.linkgenerator\]** plugin.

The process for creating a link for a form is:

-   Create a record for the target website name and URL in **Define Link**\(Link Generator Sources\).
-   Create a record for the deep link name, website name, link type, and script in **Define Link Parameters** \(Link Generator Services\).
-   Map information like the button name, button location type, form \(table\), Location \(field\), and Deep link name in **Define Button** \(Link Generator Mappings\).

-   **[Add or modify an HR deep link](../task/CreateModLink.md)**  
Use the **Define Link** \(Link Generator Sources\) to create a record for the target website name and URL.

**Parent Topic:**[HR Administration](c_AdministerHRServiceManagement.md)

