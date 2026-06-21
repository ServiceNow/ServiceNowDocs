---
title: Create a multi-data source list display in Entity View Action Mapper
description: Use EVAM to take in different datasources, configure views, and show them in a card display view.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/servicenow-platform/entity-view-action-mapper-evam/tutorial-create-evam.html
release: xanadu
product: Entity View Action Mapper \(EVAM\)
classification: entity-view-action-mapper-evam
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Entity View Action Mapper, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Create a multi-data source list display in Entity View Action Mapper

Use EVAM to take in different datasources, configure views, and show them in a card display view.

## Before you begin

Role required: admin or evam\_admin

## About this task

A typical scenario is showing user requests and incidents in a single display view. A user might want to see requests that can be made from a catalog, such as a computer order. They also might want to see open or closed incidents. These items come from different datasources, but need to display through a consistent standard that can be easily configured.

This tutorial runs through creating an EVAM definition with two datasources, a configuration bundle for each datasource which contains two view configurations, and associated actions and view templates. Many tasks are repeated, instead of repeating each step, the following table lists the unique configurations and definitions:

|EVAM Definition|Datasource \[Table\]|Configuration Bundle|Action|Configuration View|View Template|
|---------------|--------------------|--------------------|------|------------------|-------------|
|User Requests|Catalog Requests \[Requested Item\]|Catalog Request Bundle|Navigation|Open Requests|Open Request Template|
|Closed Requests|Closed Request Template|
|Incidents Submitted \[Incidents\]|Incidents Submitted Bundle|Open Incidents|Open Incidents Template|
|Closed Incidents|Closed Incidents Template|

## Procedure

1.  [Create an EVAM definition for user requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/entity-view-action-mapper-evam/define-composite-dataset.md).

    An EVAM definition houses datasources, configuration bundles with associated view configurations, data filters, actions, and templates. After you initially submit your EVAM definition, you will see the related lists to add datasources, configuration bundles, and data filters.

    \[Omitted image "user-request-tutorial.png"\] Alt text: Create a User Request EVAM definition

2.  [Define datasources for your EVAM definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/entity-view-action-mapper-evam/define-evam-datasource.md).

    Create and link each datasource to the User Request definition. The initial datasource is for catalog requests. You can also make one for incidents submitted.

    \[Omitted image "tutorial-create-datasource.png"\] Alt text: Create Catalog Requests datasource

3.  [Create and link a view configuration bundle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/entity-view-action-mapper-evam/define-view-configuration-bundle.md).

    You should create two configuration bundles, a catalog request bundle and an incidents submitted bundle.

    \[Omitted image "tutorial-new-bundle.png"\] Alt text: EVAM configuration bundle

4.  Use the Create and Link to add [create and add view configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/entity-view-action-mapper-evam/define-template-predicate.md).

    The first one view configuration will be for Open Requests.

    \[Omitted image "tutorial-new-view-config.png"\] Alt text: Create an Open Requests view configuration

5.  [Create an action definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/entity-view-action-mapper-evam/define-evam-action.md).

    You can use the create and link related list.

    \[Omitted image "tutorial-link-action-def.png"\] Alt text: Navigation action definition

6.  [Create view templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/entity-view-action-mapper-evam/define-evam-template.md) for requested items and associate with the view configuration.

    Here is the template info for the Requested Items Template:

    ```
    {
    	"component": "now-card-evam-record",
    	"staticValues": {
    		"highlightedHeaderIcon": {
    			"key": "clock-outline"
    		},
    		"highlightedHeaderBkgColor": {
    			"key": "positive"
    		},
    		"imageType": {
    			"key": "image"
            },
    		"detailLabelOne": {
    			"translatable": true,
    			"key": "created"
    		},
    		"detailLabelTwo": {
    			"translatable": true,
    			"key": "number"
            }
    	},
    	"mappings": {
    		"highlightedHeaderLabel": "state",
    		"titleLabel": "cat_item.name",
    		"imageURL": "cat_item.picture",
    		"subtitle": "cat_item.short_description",
    		"detailValueOne": "sys_created_on",
    		"detailValueTwo": "number"
    	},
    	"actionMappings": {
    		"clickAction": "navigation"
    	}
    }
    ```

7.  Repeat steps 3-5 to add another view configuration for closed requests.

    You created a configuration bundle with one view configuration. Add another configuration called Closed requests. This view configuration references the same datasource \[requested item\], but uses different conditions to show \(\).

8.  Associate view templates to view configurations, click **Update**.

9.  View your finished product.

    \[Omitted image "tutorial-card-list-display.png"\] Alt text: EVAM card list display


