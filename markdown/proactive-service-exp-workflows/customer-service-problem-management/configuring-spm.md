---
title: Configuring Customer Service Problem Management
description: With Customer Service Problem Management \(CSPM\) define the tests to diagnose the service problems. Implement targeted solutions based on test results to resolve those problems.
locale: en-US
release: yokohama
product: Customer Service Problem Management
classification: customer-service-problem-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Customer Service Problem Management]
---

# Configuring Customer Service Problem Management

With Customer Service Problem Management \(CSPM\) define the tests to diagnose the service problems. Implement targeted solutions based on test results to resolve those problems.

The configuration of CSPM requires setting up the following applications to manage service problems from detection through resolution:

-   **Customer Service Problem Management**

    Streamlines how service-related issues are handled. It enables customer service agents to either initiate a case or access the existing ones that are created in response to the issues experienced by customers. This application serves as a central hub for tracking, managing, and resolving customer issues.

-   **Service Test Management**

    Enables you to define and manage various tests that help diagnose service problems. By using this application, service teams can confirm that they have robust testing procedures in place, which are critical for identifying the root causes of issues and implementing timely solutions.


As an administrator, follow these steps to configure the Customer Service Problem Management:

-   Activate the Customer Service Problem Management application.
-   Define Test definitions. For more information, see [Setting up test definitions](settingup-test-specifications.md).

-   **[Activate Customer Service Problem Management](../task/install-spm.md)**  
Activate the Customer Service Problem Management plugin \(sn\_sprb\_mgmt\) for Customer Service Problem Management if you have the admin role. The application includes demo data and activate related ServiceNow® Store applications and plugins if they aren't already installed.
-   **[Setting up a test group](setting-test-group.md)**  
Define tests for a particular service type, product model, or inventory to troubleshoot the service-related problems.
-   **[Setting up test definitions](settingup-test-specifications.md)**  
Define tests for a particular service type, product model, or inventory to troubleshoot the service-related problems.
-   **[Integrating Customer Service Problem Management with southbound external systems](cspm-integrate-southbound.md)**  
If you have a Customer Service Problem Management subscription, you can submit outbound service test run requests to various external systems by integrating the Customer Service Problem Management application with the external southbound systems.

**Parent Topic:**[Customer Service Problem Management](../reference/cspm-landing-page.md)

