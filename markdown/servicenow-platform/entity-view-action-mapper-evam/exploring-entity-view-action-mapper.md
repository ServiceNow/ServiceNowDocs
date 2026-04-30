---
title: Exploring Entity View Action Mapper
description: The Entity View Action Mapper \(EVAM\) is an application that standardizes how different data sources display in cards and lists.
locale: en-US
release: zurich
product: Entity View Action Mapper \(EVAM\)
classification: entity-view-action-mapper-evam
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [EVAM, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Exploring Entity View Action Mapper

The Entity View Action Mapper \(EVAM\) is an application that standardizes how different data sources display in cards and lists.

## EVAM overview

EVAM enables you to show information as a card grid view or as a list of information in a list view. Users can page through large data sets of search results and see different views based on filtering.

Prior to EVAM, lists were restricted to a single type of data source. If there were more data sources, you would have to write a custom implementation. EVAM enables you ingest multiple lists from different data sources, and then configure specific views without the need for customization.

![Platform card displays](../images/card-dispaly-legacy.png)

## Features of EVAM

-   **Use multiple data sources for a single list view**

    EVAM can accept multiple disparate data sources and configure the data through sorting and filtering to return the data as a single list.

-   **Define view templates**

    Map the data source output to a UX component view by using view templates. You can configure multiple view templates per data source based on a condition to customize how data displays for users.

-   **Create view configurations to combine conditions, database fields, and declarative actions**

    Create a view configuration to combine conditions, database fields, and declarative actions with an associated view template. You can also group view configurations together to create configuration bundles.

-   **Enable user interactions to trigger actions**

    EVAM enables user interactions to trigger a server script or UXF client action.


## EVAM users

|User|Description|
|----|-----------|
|Service desk agents|Service desk agents need a streamlined way to view and manage incidents, requests, and tasks across different tables. EVAM allows them to filter, sort, and take action on records quickly.|
|IT support staff|IT teams use EVAM to monitor and manage IT assets, service requests, and incidents by consolidating information into a structured, actionable interface.|
|Managers and team leads|Supervisors overseeing teams or operations benefit from EVAM's ability to present key performance indicators and open tasks and team workloads in an easy-to-navigate format.|
|Customer service representatives|Customer support teams interact with cases, accounts, and customer information efficiently, improving response times and service quality through EVAM.|
|Business analysts and process owners|Analysts use EVAM to configure views that bring together data from multiple sources, enabling better decision-making and process optimization.|
|Developers and admins|Developers and system administrators configure EVAM to create custom views, ensuring the right data is surfaced to the right users for improved usability.|

## EVAM workflow

EVAM consists of the following:

-   Entity \(data source\) - The entity that has associated data that you intend to display. For example, a community post or a user.
-   View – A view is how a card displays data and actions.
-   Actions – An entity can have an action that performs on the card. For example, you can activate a user into your system.
-   Map – The mapping process maps the data source data to component properties that display on the card. You can also associate actions that trigger from the card view.

![EVAM workflow overview](../images/evam-mapping-overview.png "EVAM workflow")

1.  Entity: examples include a community post or sys\_user
2.  Mapping: fields found in an entity
3.  View/Action: locations or actions that entity fields are mapped to

In this workflow:

1.  The first record to set up is an EVAM definition. Additional records will branch off from this record to define the definition.
2.  The next record to set up is the EVAM View Config Bundle. The Related List record is the EVAM View Config record. Additional conditions, the view, and the action are configured or linked here. Pay attention to where the View Template and the Action are located.
3.  The third record to set up is the EVAM Configuration Bundle. Linked to the EVAM Configuration Bundle record, an EVAM action definition record defines what is triggered when a user interacts with the interface. A server script or UXF client action can be executed. Examples of an action can be to make a request, call a number, link to an external URL, or navigate within the platform.
4.  The mapping step of EVAM is accomplished with the View Template. The JavaScript Objection Notation \(JSON\) Template on the form makes the connection from the data to the component that will display the data.

## EVAM benefits

-   Configure multiple view templates per data source based on conditions to customize how data displays for users. The view template maps fields from the view configuration to component.
-   Use EVAM to take in different data sources, configure views, and show them in a card display view.
-   Define the list of data sources to render. The EVAM definition is the main record for an EVAM configuration.

## What to explore next

To learn more about configuring and using EVAM, see:

-   [Configuring Entity View Action Mapper](configuring-entity-view-action-mapper.md)
-   [Using Entity View Action Mapper](managing-entity-view-action-mapper.md)
-   [Entity View Action Mapper reference](entity-view-action-mapper-reference.md)

