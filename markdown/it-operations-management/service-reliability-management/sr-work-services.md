---
title: Working with SRM services
description: A service represents a functional outcome like networking, payments, or HR services, that is owned by a team. To deliver that outcome, a service can contain one or more technical components like a user authentication service, or a piece of shared infrastructure like a database.
locale: en-US
release: zurich
product: Service Reliability Management
classification: service-reliability-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Using Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Working with SRM services

A service represents a functional outcome like networking, payments, or HR services, that is owned by a team. To deliver that outcome, a service can contain one or more technical components like a user authentication service, or a piece of shared infrastructure like a database.

Service Reliability Management \(SRM\) works with integrations to prioritize and route alerts to the relevant responders. It follows up with escalations until the alert is acknowledged and someone responds. When you create or add a service in SRM, it must reflect a service in your SRM infrastructure.

**Note:** You might want multiple tool integrations to monitor eachtechnology management service and receive events from those tools. See [Working with integrations in SRM](sr-work-integrations.md) for more information.

In addition, you can create reliability metrics for the service. See [Working with reliability metrics](../../slo-management/concept/sr-work-SLI-SLO.md).

Tying a team and policies to that service makes it easier to divide responsibilities and track technical outcomes. It also makes it easier to automate response routines and focus on who you notify and when.

The state of an exiting service is inherited. The state of a created service in SRM is **None**.

## Services Overview

![Services page showing the list of your services](../image/sr-services-landing-page.png "Information on the Overview tab")

The cards on the Overview tab display the following metrics. By default, the list view shows information related to the Your services card. Select a different card to view different information in the list view.

-   **Your services**: Count of all the services you or your team manages and monitors for reliability.
-   **Services with active incidents**: Services with open incidents sorted in the following order:
    -   Business criticality - most critical first.
    -   Number of active incidents - highest first.
    -   Percentage of error budget remaining - lowest first.
-   **Services with critical alerts**: Services with open alerts sorted in the following order:
    -   Business criticality - most critical first.
    -   Number of alerts - highest first.
    -   Percentage of error budget remaining - lowest first.
-   **Services with open changes**: All the services your team manages and monitors.
-   **Services with low error budget**: Services with less than 25% error budget remaining.

    The error budget metric is represented as the amount of service level objective \(SLO\) that you can spend over a specified time. It can be used to manage release velocity.


**Note:** To refresh the card and list values, select Refresh ![Refresh icon](../image/icon-sr-browser-refresh.png).

You can interact with the list in the following ways:

-   Group or filter columns to customize the view.
-   Edit, sort, or export the list as needed. See [Export list information to a file](../task/sr-export-to-file.md).

For more information about individual service details, see [Edit service details form](../reference/sr-edit-service-form.md).

## Services list view definitions

The columns include the following details:

-   **Service**: Name of the service.
-   **Class**: Service instance or technology management service.
-   **Business criticality**: Importance of the service to the business.
-   **Open alerts**: Number of open alerts assigned to the service.
-   **Open incidents**: Number of open incidents assigned to the service.
-   **Error budget remaining**: Percentage of error budget remaining for the service.

## Service reliability

The Service reliability tab is a customizable dashboard showing high-level service performance. For more information about the dashboard, see [Visualizations in the Service reliability dashboard](../reference/sr-service-dashboard-visualizations.md).

-   **[Add a service to SRM](../task/sr-add-service.md)**  
Add services to Service Reliability Management \(SRM\) to help your teams manage service health.
-   **[Edit service details in SRM](../task/sr-edit-service.md)**  
Edit an existing service owned by your team. For each service that you support in SRM provide general information about the service and the SRM team that supports it.
-   **[Remove a service from SRM](../task/sr-remove-service.md)**  
Remove a service from Service Reliability Management \(SRM\) when you no longer need to track or monitor its reliability.
-   **[Working with integrations in SRM](sr-work-integrations.md)**  
Connect your services to monitoring tools using the Integrations Launchpad . Integrations send information to Service Reliability Management \(SRM\), helping you track alerts, manage incidents, and maintain service health.

**Parent Topic:**[Using Service Reliability Management](using-service-reliability-management.md)

**Related topics**  


[Working with SRM teams](sr-work-teams.md)

[Working with SRM reliability tasks](../task/sr-work-reliability-tasks.md)

