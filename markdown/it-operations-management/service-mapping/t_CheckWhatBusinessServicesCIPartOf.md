---
title: Check CI dependencies
description: You can see if a particular configuration item \(CI\) is part of other application services and check if it depends on other CIs.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Application service analysis and maintenance using classic Service Mapping, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Check CI dependencies

You can see if a particular configuration item \(CI\) is part of other application services and check if it depends on other CIs.

## Before you begin

Role required: admin, app\_service\_admin, app\_service\_user

## About this task

While Service Mapping shows position of a CI in a particular application service, your organization may also use the same CI in other application services. If you are planning to perform changes to this CI, make sure that the changes do not affect other application services.

## Procedure

1.  In the map, right-click the relevant CI and select **Open dependency views**.

    The Dependency Views page opens in the new tab showing the selected CI in the center.

2.  Click **Details**.

    ![The Details button on the Dependency Views page.](../image/DependencyViewDetailsbutton.png)

3.  Click the **Related Services** tab.

    The list of links to application services containing this CI appear on the **Related Services** tab.

4.  To view the map of another application service containing this CI, click the relevant link.


**Parent Topic:**[Application service analysis and maintenance using classic Service Mapping](../concept/c_SvcPlanningAndAnalysisUsingMaps.md)

**Related topics**  


[Service instances \(Application services\)](https://www.servicenow.com/docs/access?context=application-services&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

[Application service maps in classic Service Mapping](../concept/c_UndestandMaps.md)

[Dependency Views](https://www.servicenow.com/docs/access?context=c_BusinesssServiceManagementMaps&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

