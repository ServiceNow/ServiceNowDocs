---
title: Create service specific UI actions
description: Create a UI action or modify an existing one to enable your service to create department tickets under a universal request.
locale: en-US
release: australia
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure service to use Universal Request, Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Create service specific UI actions

Create a UI action or modify an existing one to enable your service to create department tickets under a universal request.

## Before you begin

Role required: admin

Administrators and users with the ui\_action\_admin role can define UI actions.

## About this task

For example, consider a scenario when a Tier 1 agent of a service department receives a universal request, and is not able to resolve it. The agent escalates the request to another department or to an agent within the same department. In this case, the Tier 1 agent uses the **Create case** or similarly labeled action to create a new case within the service \(department\). This case can then be routed to the appropriate assignment group for resolution.

To perform this action, you must create a UI action for your service.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **UI Actions**.

    A list of all UI actions specific to Universal Request table appears.

2.  Click **New** or open an existing record.

    **Note:** For a new UI action, ensure that you always select the Universal Request table.

3.  On the form, fill in the fields to define the UI action.

    For more information, see [Create a UI action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_EditingAUIAction.md).


**Parent Topic:**[Configure service to use Universal Request](../concept/config-service-for-ur.md)

