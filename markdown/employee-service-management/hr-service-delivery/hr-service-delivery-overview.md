---
title: Supporting information for HR Service Delivery
description: The ServiceNow HR Service Delivery application improves the employee service experience by automating HR interactions and providing a single platform for all HR services.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [HR Service Delivery, Employee Service Management]
---

# Supporting information for HR Service Delivery

The ServiceNow® HR Service Delivery application improves the employee service experience by automating HR interactions and providing a single platform for all HR services.

## HR Service Delivery applications

Users can choose from the following applications to enhance the employee service experience. The list of available applications depends on the HR Service Delivery package your organization purchased.

|Application|Description|
|-----------|-----------|
|[Case and Knowledge Management](../reference/case-knowledge-management-landing-page.md)|Automates standard HR processes and provides a centralized platform for employees to submit and track requests, while enabling HR agents to efficiently manage and monitor cases.|
|[Employee Document Management](hr-employee-doc-management.md)|Efficiently manages large numbers of documents by providing cloud-based storage, a robust filing system, easy retrieval, secure access controls, and compliance risk reduction, ensuring that employees can complete and return documents related to benefits, payroll, and other services seamlessly.|
|[Agent Workspace for HR Case Management](agent-ws-hr-case-mgmt-landing-page.md)|Interact with employees, respond to inquiries, and resolve issues quickly as an HR agent.|
| | |
| | |

## HR Service Delivery Integrations

HR Service Delivery integrates with other ServiceNow® applications as well as third-party applications to enhance the overall employee service experience.

-   [Enterprise Service Management Integrations Framework](hr-integrations-framework.md) provides a consistent way of building integrations for common use cases such as pulling employee profiles and tasks from third-party application to a ServiceNow application, and pushing data from a ServiceNow application into a third-party application.
-   [HR Predictive Intelligence Workbench](hr-predictive-intelligence-wb.md) to guide you through your predictive machine learning implementation to create intelligent HR processes.
-   [Machine learning solutions for HR Service Delivery](predictive-intelligence-for-hr-service-delivery-1.md) to help in auto determining assignment groups and services for HR cases, auto creating cases from emails, and discovering knowledge articles that help in faster resolution of cases and tasks.
-   [Performance Analytics for HR Service Delivery](scoped-hr-performance-analytics.md) to reduce HR inefficiencies by reporting and analyzing service delivery performance and quality. A separate subscription is required.
-   [Virtual Agent for HR Service Delivery](hr-virtual-agent-conversations.md#) to enable automated chats for employees requesting HR services.

For the full list of integrations, see [Integration of HR Service Delivery with ServiceNow applications](integrate-hr-platform-apps.md) and [Integration of HR Service Delivery with third-party systems](integrate-third-party-systems.md).

## Employee experience

HR Service Delivery enables many of the capabilities available on the [Employee Center](../../employee-center/concept/ec-and-ecpro-landing-page.md) portal, where employees can report issues, request items or services, receive training, and complete to-dos.

## Mobile application

Employees view HR requests, request help, complete HR tasks, receive targeted mobile content and push notifications, chat with a virtual agent, and more using the [Now Mobile app](../../../administer/mobile-employee/concept/mobile-employee-experience.md) app.

## Domain separation and HR Service Delivery

Domain separation separates data, processes, and administrative tasks into logical groupings called domains. You can then control several aspects of this separation, including which users can see and access data. For more information, see [Domain Separation and HR Service Delivery](hr-domain-separation.md).

## Quick start tests for HR Service Delivery

Copy and customize quick start tests to validate that your instance works after you make any configuration changes, such as after applying an upgrade or developing an application. For more information, see [Quick start tests for HR Service Delivery](../../../administer/atf-quick-start-tests/reference/quick-start-tests-hr.md).

## Fields Containing Possibly Sensitive, Personal, or Personally Identifiable Information

Customers are responsible for ensuring their use of HR Service Delivery application is compliant with applicable data protection laws and regulations. Customers using the HR Service Delivery application should assess fields that may contain sensitive, personal, or personally identifiable information, the extent of which is solely determined by customers. Once installed, customers are able to access table definitions within their instance to review fields used by HR Service Delivery application. This can be done by navigating to "System Definition &gt; Tables" and filtering "Name" "starts with" "sn\_hr\_".

COE security policies are a way to easily restrict access to different COEs via configuration. The underlying COE security policy implementations are [ServiceNow ACLs](https://www.servicenow.com/docs/access?context=access-control-rules&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

