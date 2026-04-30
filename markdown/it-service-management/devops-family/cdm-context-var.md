---
title: Contextual variables for config data
description: Contextual variables are out-of-the-box variables delivered by ServiceNow that enable you to use the context of a node to define a variable.
locale: en-US
release: yokohama
product: DevOps \(Family\)
classification: devops-family
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [CDM data model, Reference, DevOps Config, IT Service Management]
---

# Contextual variables for config data

Contextual variables are out-of-the-box variables delivered by ServiceNow that enable you to use the context of a node to define a variable.

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

For example: CollectionA has defined these variables:

-   "environment": "\(\#DEPLOYABLE.ENVIRONMENT\_TYPE\#\)"
-   "deployable": "\(\#DEPLOYABLE.NAME\#\)"

When you add the collection to a deployable, these variables are set to the values defined in the context, which would be the environment type and name of the deployable for CollectionA.

The available out-of-the-box contextual variables are:

|Variable|Description|
|--------|-----------|
|NAME|Name of the node.|
|APPLICATION.NAME|Name of the application.|
|DEPLOYABLE.NAME|Name of the deployable.|
|DEPLOYABLE.ENVIRONMENT\_TYPE|Environment type of the deployable.|
|COLLECTION.NAME|Name of the collection.|
|FULL\_PATH|The full file path of the collection.|
|RELATIVE\_PATH|The file path of the collection, relative to the deployable.|
|RELATIVE\_PARENT\_PATH|The file path of the parent to the node.|

**Parent Topic:**[CDM data model](cdm-data-model.md)

