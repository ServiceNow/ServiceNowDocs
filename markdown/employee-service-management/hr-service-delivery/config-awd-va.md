---
title: Configure Virtual Agent topics for HR Service Delivery Advanced Integration with Workday
description: Complete the configuration steps to enable your employees place requests to the Workday system using the Now Assist for HRSD Virtual Agent topics in Employee Center.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-07-22"
reading_time_minutes: 1
breadcrumb: [Configuring, HR Service Delivery Advanced Integration with Workday, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configure Virtual Agent topics for HR Service Delivery Advanced Integration with Workday

Complete the configuration steps to enable your employees place requests to the Workday system using the Now Assist for HRSD Virtual Agent topics in Employee Center.

## Before you begin

Role required: flow\_designer, decision\_table\_admin, sn\_hr\_integr\_fw.admin, and sn\_hr\_core.admin

## Procedure

1.  Install the HR Service Delivery Advanced Integration with Workday, Now Assist for HRSD, and Enterprise Service Management Integrations Framework \(v3.6\) applications from ServiceNow Store.

2.  Configure the [Workday HR Spoke](https://www.servicenow.com/docs/access?context=workday-hr-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) to pull data from Workday system.

3.  Create subflows aligning with Template Integration Gateway.

    See [Create a subflow using Template Integration Gateway](configure-integration-gateway.md).

    **Note:** You can use the default subflows that have been created for Workday for the Request Time off and Get Time Off Balance Virtual Agent topics.

4.  [Configure Integration Provider Mapping \(Decision table\)](configure-integration-mapping.md) by adding input choices and configuring conditions on input choices and results.

5.  Create a Virtual Agent topic block:

    **Note:** The Virtual Agent topics are available by default with the Now Assist for HRSD scope.

    1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.
    2.  From the **LLM Assistant** list, select **Now Assist in Virtual Agent**.
    3.  Select a Virtual Agent topic.
        1.  Edit topic properties, make the necessary edits in the topic, such as update the node name, and response message.
        2.  In Integration Gateway, specify the appropriate feature, service name, user, and make the necessary edits.

## What to do next

When an Virtual Agent topic invokes the Integration Gateway subflow, the subflow reviews input values in Integration Provider Mapping \(Decision table\) to execute results.

