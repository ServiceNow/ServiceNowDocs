---
title: Unified ticket experience setting
description: Set up your service to provide your employees with a unified and consistent ticket experience. This setup automatically creates a universal request when requests are raised from an interaction record, email, or record producer.
locale: en-US
release: australia
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure service to use Universal Request, Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Unified ticket experience setting

Set up your service to provide your employees with a unified and consistent ticket experience. This setup automatically creates a universal request when requests are raised from an interaction record, email, or record producer.

You can customise and configure to automatically create universal request for a task from various channels using APIs provided with the Universal Request application. For more information, see [UniversalRequestUtilsSNC API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/UniversalRequestUtilsSNCScopedAPI.md).

Universal Request application supports the creation of universal request from an interaction record in the Agent Workspace. For more information, see [Create a Universal Request from an Interaction Record](use-UR-workspace.md#).

Modifying email notification preferences helps in controlling the outbound email actions. For more information, see [Email notification preferences for your service](ur-customize-email-notifcations.md).

Set up email preferences to create universal request when an email is received in the configured mail box. For more information, see [Automatically create universal request from an inbound email](create-ur-from-inbound-email.md).

Configure your service record producer to create universal request from a request raised from the record producer. For more information, see [Configure a catalog item or record producer to create a universal request](../../service-catalog-management/task/create-ur-recordproducer.md).

-   **[Create universal request automatically for department tickets via other channels](../task/autocreate-ur-from-interactionrecord-WS.md)**  
Universal request is not automatically created when a fulfiller or employee creates a department ticket from channels other than the Service Portal or Virtual Agent topics. Create universal request automatically by adding the business rule to the specific service table, such as an Incident or a HR service.
-   **[Email notification preferences for your service](ur-customize-email-notifcations.md)**  
Customize email notifications to control which email notifications are sent to requesters when a universal request is created. This setting prevents employees from receiving duplicate or inconsistent email notifications.
-   **[Automatically create universal request from an inbound email](create-ur-from-inbound-email.md)**  
Universal requests can be automatically created from the information received by emails. The auto-creation of universal requests enables faster response time and quicker resolution for employees compared to the agents manually creating requests from emails.
-   **[Configure a catalog item or record producer to create a universal request](../../service-catalog-management/task/create-ur-recordproducer.md)**  
Create a universal request along with a requested item or task-based record to provide unified ticketing experience.

**Parent Topic:**[Configure service to use Universal Request](config-service-for-ur.md)

