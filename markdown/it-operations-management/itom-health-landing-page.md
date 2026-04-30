---
title: ITOM Health
description: The ServiceNow ITOM Health product includes the ServiceNow Event Management and ServiceNow Metric Intelligence applications, which help you track and maintain the health of services in your organization.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [IT Operations Management]
---

# ITOM Health

The ServiceNow® ITOM Health product includes the ServiceNow® Event Management and ServiceNow® Metric Intelligence applications, which help you track and maintain the health of services in your organization.

## Features of ITOM Health

-   **Event Management**

    Event Management gathers alerts from infrastructure events captured by third-party monitoring tools. Event Management uses IT-related information gathered by Discovery to map alerts to configuration items. Based on the collected information, Event Management then provides dashboards showing a consolidated view of all service-impact events.

-   **Agent Client Collector**

    Use the ServiceNow® Agent Client Collector application to monitor your service availability, examine the health and performance of your environment, and ensure that your infrastructure and its applications are running properly. You can also proactively analyze your IT infrastructure to spot issues and prevent service outages, using Metric Intelligence. Using advanced machine learning to analyze information about your IT infrastructure, the Metric Intelligence application automatically determines dynamic thresholds and identifies anomalies that may indicate potential service outages.

-   **Health Log Analytics**

    The ServiceNow® Health Log Analytics application predicts IT issues before they impact users. The application helps you solve problems faster by ingesting, understanding, and correlating machine-generated log data in real time. It notices any deviation from normal behavior when it happens and alerts you of possible business-impacting issues. Health Log Analytics receives and processes logs via the MID Server and sends events to the ServiceNow® Event Management application.

-   **Service Operations Workspace for ITOM**

    Service Operations Workspace for ITOM is a configurable workspace that provides a unified experience for multiple IT Operations Management workflows. Service Operations Workspace for ITOM enables you to manage the life cycle of alerts, including running actions to resolve alerts and identifying the underlying issue of an alert.


## ITOM Health licensing

The ServiceNow AI Platform® uses a licensing method where your organization is billed for using ITOM Health applications. ITOM Health and Health Log Analytics are available as separate licenses. The ServiceNow Product Documentation doesn't provide information on prices, packaging, or other details determined by your organization customer contract. For general information about licensing and subscriptions, see [ITOM/OT SU Licensing and subscriptions](itom-su-licensing-landing-page.md).

## Using guided setup to implement IT Operations Management applications

IT Operations Management Guided Setup provides a sequence of tasks that help you configure IT Operations Management applications on your ServiceNow instance. To open IT Operations Management guided setup, navigate to **Guided Setup** &gt; **ITOM Guided Setup**. For more information about using the guided setup interface, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) .

## Configure the MID Web Server extension

The MID Web Server is an extension that enables external clients to push metric data and events to the MID Server. Configure the MID Web Server extension to enable ITOM Health features \(Event Management, Agent Client Collector, and Health Log Analytics\).

