---
title: Relate business capabilities to view in Digital Portfolio Management
description: You can relate business capabilities for a service or for a business application to see them in the Digital Portfolio Management \(DPM\) Workspace.
locale: en-US
release: xanadu
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Digital Portfolio Management, Digital Portfolio Management, IT Service Management]
---

# Relate business capabilities to view in Digital Portfolio Management

You can relate business capabilities for a service or for a business application to see them in the Digital Portfolio Management \(DPM\) Workspace.

## Before you begin

Role required: sn\_dpm.dpm\_admin

## About this task

There are two conditions to create a CI relationship in DPM.

1.  The business capability must be created.
2.  The business capability must be related to a service.

You can create a business capability by navigating to **All** &gt; **CSDM** &gt; **Design** &gt; **Business Capability**. For information about configuration item \(CI\) relationships, see [Create or edit a CI relationship](https://www.servicenow.com/docs/access?context=t_CreateCIRelationship&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## Procedure

1.  Confirm the business capability name and the solution name that you want to relate.

2.  Create the CI relationship.

    1.  Enter `cmdb_rel_ci.list` in the filter navigator, and then press **Enter**.

    2.  Select **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Parent|The business capability that is to be related to the service or business application. Use the search icon \(![Search icon.](../../site-reliability-ops/image/icon-search.png)\) to select the business capability.|
        |Type|The type of CI relationship. Use the search icon \(![Search icon.](../../site-reliability-ops/image/icon-search.png)\) to select **Provided By:: Provides**.|
        |Child|The service or business application to be related to the business capability. Use the search icon \(![Search icon.](../../site-reliability-ops/image/icon-search.png)\).|

    4.  **Submit**.

3.  Confirm the CI relationship.

    You can confirm the CI relationship in one of two ways:

    -   On the business capability record, in the Related Items section.
    -   In the DPM Workspace, on the Info tab of a service or business application.

**Parent Topic:**[Configuring Digital Portfolio Management](../concept/dpm-configure-cfw.md)

**Related topics**  


[View service and service offering details](../concept/dpm-service-details.md)

[View business application details](../concept/dpm-business-apps-details.md)

