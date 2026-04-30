---
title: Entity View Action Mapper
description: Entity View Action Mapper \(EVAM\) is an application that standardizes how different data sources display in cards and lists.
locale: en-US
release: xanadu
product: Entity View Action Mapper \(EVAM\)
classification: entity-view-action-mapper-evam
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Entity View Action Mapper

Entity View Action Mapper \(EVAM\) is an application that standardizes how different data sources display in cards and lists.

EVAM enables you to show information as a card grid view or as a list of information in a list view. Users can page through large data sets of search results and see different views based on filtering.

Prior to EVAM, lists were restricted to a single type of data source. If there were more data sources, you would have to write a custom implementation. EVAM enables you ingest multiple lists from different data sources, and then configure specific views without the need for customization.

![Different Platform card displays](../images/card-dispaly-legacy.png)

## EVAM flow

EVAM consists of the following:

-   Entity \(datasource\) - The entity that has associated data that you intend to display. For example, a community post or a user.
-   Map – The mapping process maps the datasource data to component properties that display on the card. You can also associate actions that trigger from the card view.
-   View – A view is how a card displays data and actions.
-   Actions – An entity can have an action that performs on the card. For example, you can activate a user into your system.

![EVAM overview](../images/evam-mapping-overview.png)

## Features of EVAM

-   **Use multiple datasources for a single list view**

    EVAM can accept multiple disparate datasources and configure the data through sorting and filtering to return the data as a single list.

-   **Define view templates**

    Map the datasource output to a UX component view by using view templates. You can configure multiple view templates per datasource based on a condition to customize how data displays for users.

-   **Create view configurations to combine conditions, database fields, and declarative actions**

    Create a view configuration to combine conditions, database fields, and declarative actions with an associated view template. You can also group view configurations together to create configuration bundles.

-   **Enable user interactions to trigger actions**

    EVAM enables user interactions to trigger a server script or UXF client action.


## What to do

-   [Define a datasource](../task/define-evam-datasource.md)
-   [Create an EVAM definition](../task/define-composite-dataset.md)
-   [Associate a view configuration, view template, and action.](use-configuration-bundle.md)

## Activation information

EVAM is a ServiceNow AI Platform application that is active by default.

