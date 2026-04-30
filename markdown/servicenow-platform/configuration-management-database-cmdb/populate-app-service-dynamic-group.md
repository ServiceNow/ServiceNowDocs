---
title: Populate an application service using the Dynamic CI Group method
description: The Dynamic CI Group method for populating an application service, automatically generates a dynamic CI group. The members of the CMDB group that the dynamic CI group is based on, populates the application service. The application service continuously synchronizes with the CMDB group to reflect any changes in membership in the CMDB group.
locale: en-US
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create an application service, Application services, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Populate an application service using the Dynamic CI Group method

The Dynamic CI Group method for populating an application service, automatically generates a dynamic CI group. The members of the CMDB group that the dynamic CI group is based on, populates the application service. The application service continuously synchronizes with the CMDB group to reflect any changes in membership in the CMDB group.

## Before you begin

The Dynamic CI Group is one of several methods for populating an application service with CIs. Choosing a method for populating an application service, is only one step of the generic procedure for creating an application service. Ensure that you have completed the initial steps as described in [Create an application service](../../service-mapping/task/create-it-services.md). The procedure described here is incomplete by itself as it complements that generic procedure.

**Note:**

-   The number of CIs in an application service that is populated by the Dynamic CI Group method, is limited to 10,000, even if the associated CMDB group has more than 10,000 CIs.
-   A CMDB group can be used to populate only a single application service. For more information about populating and using CMDB groups, see [CMDB groups](../../../Chunk1292530847.md#).
-   A dynamic CI group contains CIs but can't contain other groups.

For information about the different types of application services and the different methods you can use to populate application services, including Dynamic CI Group, see [Application services](../concept/application-services.md).

Role required: app\_service\_admin

## Procedure

1.  In the Choose a Method page, select **Dynamic CI Group** as the **Service Population Method**.

2.  Fill out the fields that appear, which are specific to the Dynamic CI Group service population method.

<table id="table_spq_2cx_blb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Population Method

</td><td>

The method used for populating the application service with CIs. Set to **Dynamic CI Group**.

</td></tr><tr><td>

CMDB Table

</td><td>

Notes the Dynamic CI Group \[cmdb\_ci\_query\_based\_service\] table, in which application services created by the Dynamic CI Group method, are stored.

</td></tr><tr><td>

Group Name

</td><td>

The CMDB group whose members become members the application service.**Note:** CIs from a class that extends the **cmdb\_ci\_service** class \(Services\), are automatically filtered out and are not added to the application service.

</td></tr></tbody>
</table>3.  Select **Save**.


## Result

The alert impact on dynamic CI groups is calculated on the following CIs:

-   All CIs that are part of the dynamic CI's CMDB group.
-   Children of current CIs with a relationship of: **Runs on::Runs**
-   CIs related to either the current CIs or their children, with a relationship of: **Virtualized by::Virtualizes**

For more information, see [alert impact calculation](https://www.servicenow.com/docs/access?context=c_EMImpactCalculation&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

## What to do next

Complete the generic procedure [Create an application service](../../service-mapping/task/create-it-services.md).

