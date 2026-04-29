---
title: Contextual variables for config data
description: Contextual variables are out-of-the-box variables delivered by ServiceNow that enable you to use the context of a node to define a variable.
locale: en-US
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CDM data model, DevOps Config reference, DevOps Config, IT Service Management]
---

# Contextual variables for config data

Contextual variables are out-of-the-box variables delivered by ServiceNow that enable you to use the context of a node to define a variable.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

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

