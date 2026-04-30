---
title: Populate an application service using the Dynamic Service method
description: The Dynamic Service method for populating an application service generates a dynamic application service. A dynamic application service automatically updates to reflect any changes to CI relationships in the CMDB CI Relationship \[cmdb\_rel\_ci\] table.
locale: en-US
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create an application service, Application services, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Populate an application service using the Dynamic Service method

The Dynamic Service method for populating an application service generates a dynamic application service. A dynamic application service automatically updates to reflect any changes to CI relationships in the CMDB CI Relationship \[cmdb\_rel\_ci\] table.

## Before you begin

The Dynamic Service is one of several methods for populating an application service with CIs. Choosing a method for populating an application service, is only one step of the generic procedure for creating an application service. Ensure that you have completed the initial steps as described in [Create an application service](../../service-mapping/task/create-it-services.md). The procedure described here is incomplete by itself as it complements that generic procedure.

New dynamic application services initially don't contain any CIs \(unless they were converted from legacy business services or legacy manual services\). Dynamic application services are automatically populated when CIs that are contained in the service, get connected to other CIs by CMDB relationships. Entry points are automatically created when a relationship between a dynamic application service CI and other CIs is created.

For information about the different types of application services and the different methods you can use to populate application services, including Dynamic Service, see [Application services](../concept/application-services.md).

Role required: app\_service\_admin

## Procedure

1.  In the Choose a Method page, select **Dynamic Service** as the **Service Population Method**.

2.  Fill out the fields that appear, which are specific to the Dynamic Service service population method.

    |Field|Description|
    |-----|-----------|
    |Service Population Method|The method used for populating the application service with CIs. Set to **Dynamic Service**.|
    |CMDB Table|Notes the Calculated Application Services \[cmdb\_ci\_service\_calculated\] table, in which application services created by the Dynamic Service method, are stored.|
    |Levels|The number of levels of related CIs to include in the application service.|

3.  Click **Save**.


## What to do next

Complete the generic procedure [Create an application service](../../service-mapping/task/create-it-services.md).

