---
title: View the list of CIs belonging to an application service
description: View a complete list of CIs that make up an application service, including CIs not shown on the application service map: tracked configuration files, endpoints, processes, and network devices.
locale: en-US
release: xanadu
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Application service analysis and maintenance using classic Service Mapping, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# View the list of CIs belonging to an application service

View a complete list of CIs that make up an application service, including CIs not shown on the application service map: tracked configuration files, endpoints, processes, and network devices.

## Before you begin

Role required: service\_mapping\_admin or service\_mapping\_user

## About this task

By default, application service maps show application CIs and connections between them. The rest of the CIs behind applications and connections between them are hidden. The CI list displays the following additional CIs:

-   Servers that host applications.
-   Network devices like routers or switches.
-   Processes running on hosting servers. Processes are used for identification and classification of applications.
-   Tracked configuration files for applications that are part of the service.
-   Endpoints belonging to the applications. Endpoints contain information necessary for connecting to applications, like hosts and ports.
-   The application service CI for this application service.

The CI lists for empty application services, that do not contain any CIs contain only one CI: For the application service itself.

## Procedure

1.  Navigate to **All** &gt; **CSDM** &gt; **Manage Technical Services** &gt; **Service Instance**.

2.  Navigate to **Application Services** &gt; **View:csdm\_view** &gt; **View** &gt; **Default view**.

    ![Change application service to default view](../image/app-service-change-view.png)

3.  Click the name of the application service for which you want to view the list of CIs.

    The discovery state of the selected service must be **Done**.

4.  Click **List CIs** under Related Links.

    ![List CIs link under Related Links](../image/application-service-list-cis.png)

5.  View the complete list of CIs that are part of the selected application service.

6.  Click the back button on your browser to return to the Mapped Application Service page when you have finished reviewing the list of CIs.

7.  Select **View map** to navigate to the application service map.


**Parent Topic:**[Application service analysis and maintenance using classic Service Mapping](../concept/c_SvcPlanningAndAnalysisUsingMaps.md)

