---
title: Enable external customers to create requests
description: Enable your external customers to create and track requests from the Customer and Consumer Service Portals.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up CSM integration with IT Service Management, Integrating with IT Service Management, Integrating Customer Service Management with other applications, Customer Service Management]
---

# Enable external customers to create requests

Enable your external customers to create and track requests from the Customer and Consumer Service Portals.

## Before you begin

Role required: admin

## About this task

Each submitted request generates a case, with the request record associated to that case. Customer service agents can also create requests on behalf of contacts and consumers.

**Note:** This feature requires activation of the Customer Service with Request Management plugin \(com.sn\_cs\_sm\_request\).

## Procedure

-   Configure the Case form to display the **Initiated as request** field.

    When a request is created from the portal, the system creates a case for the request and sets this field to true.

    **Note:** The **Initiated as request** field is read-only for all users.


**Related topics**  


[Create a request on behalf of a customer or consumer](agent-create-request-for-customer.md)

[Request an item or service from the Customer Service Portal](customer-request-from-portal.md)

