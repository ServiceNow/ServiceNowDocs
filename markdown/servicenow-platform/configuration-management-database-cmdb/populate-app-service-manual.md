---
title: Populate an application service using the Manual method
description: The Manual method for populating an application service, is based on selecting an entry point CI, which lets users access the application service. To populate the application service, you then manually add CIs to the new application service.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create an application service, Application services, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Populate an application service using the Manual method

The Manual method for populating an application service, is based on selecting an entry point CI, which lets users access the application service. To populate the application service, you then manually add CIs to the new application service.

## Before you begin

Role required: app\_service\_admin

## About this task

Manual is one of several methods for populating an application service with CIs. Choosing a method for populating an application service, is only one step of the generic procedure for creating an application service. Ensure that you have completed the initial steps as described in [Create an application service](../../service-mapping/task/create-it-services.md). The procedure described here is incomplete by itself as it complements that generic procedure.

For information about the different types of application services and the different methods you can use to populate application services, including Manual, see [Application services](../concept/application-services.md).

## Procedure

1.  In the Choose a Method page, select **Manual** as the **Service Population Method**.

2.  Fill out the fields that appear, which are specific to the Manual service population method.

<table id="table_ez2_f5q_5lb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Population Method

</td><td>

Manual

</td></tr><tr><td>

CMDB Table

</td><td>

Notes the Mapped Application Service \[cmdb\_ci\_service\_discovered\] table, in which application services, created by the Manual service population method, are stored.

</td></tr><tr><td>

Class

</td><td>

The class from which to choose the entry point **CI** for the application service.

</td></tr><tr><td>

CI

</td><td>

The CI from the specified **Class**, to be the entry point for the application service.**Note:** To eliminate the possibility of delayed results when searching for a specific CI, make your search as specific as possible. A search with \*&lt;name&gt; might take a long time and return a large data set.

</td></tr></tbody>
</table>3.  Click **Save**.


## What to do next

1.  Complete the generic procedure [Create an application service](../../service-mapping/task/create-it-services.md).
2.  [Manually add CIs](https://www.servicenow.com/docs/access?context=manually-add-ci-to-business-service&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) to populate the application service.

