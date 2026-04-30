---
title: Working with SRM services
description: A service represents a functional outcome like networking, payments, or HR services, that is owned by a team. To deliver that outcome, a service can contain one or more technical components like a user authentication service, or a piece of shared infrastructure like a database.
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using Service Reliability Management, Service Reliability Management, ITOM Health, IT Operations Management]
---

# Working with SRM services

A service represents a functional outcome like networking, payments, or HR services, that is owned by a team. To deliver that outcome, a service can contain one or more technical components like a user authentication service, or a piece of shared infrastructure like a database.

SRM works with integrations to prioritize and route alerts to the right responders and follow up with escalation until the alert is acknowledged and you know that someone is responding. When you create or add a service in SRM, it must reflect a service in your SRM infrastructure.

**Note:**

You might want multiple tool integrations to monitor each technical service and receive events from those tools. Add an integration to SRM using the Services ![Services icon](../image/icon-sr-services.png) module. See [Working with SRM integrations](sr-work-integrations.md).

In addition, you can create reliability metrics for the service. See [Working with Reliability metrics](../../slo-management/concept/sr-work-SLI-SLO.md)

Tying a team and policies to that service makes it easier to divide responsibilities and track technical outcomes. It also makes it easier to automate response routines and focus on who you notify and when.

The state of an exiting service is inherited. The state of a created service in SRM is **None**.

## Services

![Services page showing the list of your services](../image/sr-services-landing-page.png "Services landing page")

The services cards display metrics for:

-   **Your Services**: Count of all the services you or your team manages and monitors for reliability.
-   **Services with active incidents**: Services with one or more open incidents, sorted first by business criticality, most critical at the top; then sorted by number of active incidents, highest number at the top; and finally sorted by % of error budget remaining, lowest at the top.
-   **Services with critical alerts**: Services with open alerts, sorted first by business criticality, most critical at the top; then sorted by number of alerts, highest number at the top; and finally sorted by % of error budget remaining, lowest at the top.
-   **Services with open changes**: All the services your team manages and monitors.
-   **Services with low error budget**: Services with error budget remaining &lt; 25%

    The error budget metric is represented as the amount of SLO that you can spend over a specified time. It can be used to manage release velocity.


**Note:** To refresh the card values, as well as the lists they represent, use the browser Refresh ![Refresh icon](../image/icon-sr-browser-refresh.png) button.

The list view varies depending on the Services card selected.

**Note:** **Your services** is the default selection for the landing page.

Each column in the list can be grouped or filtered.

Each list can be edited, sorted or [exported](../task/sr-export-to-file.md).

For more detailed information on individual service details, see [Edit service details form](../reference/sr-edit-service-form.md).

## Services list view metric definitions

**Service level objectives** section

-   **Service**: Name of the service.
-   **Class**: Application or Technical service.
-   **Business criticality**: How important this service is the business.

    Choices are:

    -   1 - most critical \(default\)
    -   2 - somewhat critical
    -   3 - less critical
    -   4 - not critical
-   **Open alerts**: Number of open alerts assigned to the service.
-   **Open incidents**: Number of open incidents assigned to the service.
-   **Error budget remaining**: Percentage of error budget remaining for the service.

-   **[Add a service to SRM](../task/sr-add-service.md)**  
Create or add an existing service to your instance so that alerts and incidents on that service are available to your teams within SRM.
-   **[Edit SRM service details](../task/sr-edit-service.md)**  
Edit an existing service owned by your team. For each service that you support in SRM provide general information about the service and the SRM team that supports it.

**Parent Topic:**[Using Service Reliability Management](using-service-reliability-management.md)

**Previous topic:**[Using Service Reliability Management](using-service-reliability-management.md)

**Next topic:**[Add a service to SRM](../task/sr-add-service.md)

