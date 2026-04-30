---
title: Create a multi-data source list display in Entity View Action Mapper
description: Use EVAM to take in different datasources, configure views, and show them in a card display view.
locale: en-US
release: zurich
product: Entity View Action Mapper \(EVAM\)
classification: entity-view-action-mapper-evam
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Use EVAM, EVAM, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Create a multi-data source list display in Entity View Action Mapper

Use EVAM to take in different datasources, configure views, and show them in a card display view.

## Before you begin

Role required: admin or evam\_admin

## About this task

A typical scenario is showing user requests and incidents in a single display view. A user might want to see requests that can be made from a catalog, such as a computer order. They also might want to see open or closed incidents. These items come from different data sources, but need to display through a consistent standard that can be easily configured.

This tutorial runs through creating an EVAM definition with two data sources, a configuration bundle for each data source which contains two view configurations, and associated actions and view templates. Many tasks are repeated, instead of repeating each step, the following table lists the unique configurations and definitions:

|EVAM definition|Data source \[Table\]|Configuration bundle|Action|Configuration view|View template|
|---------------|---------------------|--------------------|------|------------------|-------------|
|User Requests|Catalog Requests \[Requested Item\]|Catalog Request Bundle|Navigation|Open Requests|Open Request Template|
|Closed Requests|Closed Request Template|
|Incidents Submitted \[Incidents\]|Incidents Submitted Bundle|Open Incidents|Open Incidents Template|
|Closed Incidents|Closed Incidents Template|

## Procedure

1.  [Create an EVAM definition for user requests](define-composite-dataset.md).

    An EVAM definition houses data sources, configuration bundles with associated view configurations, data filters, actions, and templates. After you initially submit your EVAM definition, you will see the related lists to add data sources, configuration bundles, and data filters.

    ![Create a User Request EVAM definition](../images/user-request-tutorial.png)

2.  [Define data sources for your EVAM definition](define-evam-datasource.md).

    Create and link each data source to the User Request definition. The initial data source is for catalog requests. You can also make one for incidents submitted.

    ![Create Catalog Requests data source](../images/tutorial-create-datasource.png)

3.  [Create and link a view configuration bundle](define-view-configuration-bundle.md).

    You should create two configuration bundles, a catalog request bundle and an incidents submitted bundle.

    ![EVAM configuration bundle](../images/tutorial-new-bundle.png)

4.  [Create an action definition](define-evam-action.md).

    You can use the create and link related list.

    ![Navigation action definition](../images/tutorial-link-action-def.png)

5.  [Create view templates](define-evam-template.md) for requested items and associate with the view configuration.

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

6.  Repeat steps 3-5 to add another view configuration for closed requests.

    You created a configuration bundle with one view configuration. Add another configuration called Closed requests. This view configuration references the same data source \[requested item\], but uses different conditions to show \(\).

7.  Associate view templates to view configurations, select **Update**.

8.  View your finished product.

    ![EVAM card list display](../images/tutorial-card-list-display.png)


**Parent Topic:**[Using Entity View Action Mapper](../concept/managing-entity-view-action-mapper.md)

