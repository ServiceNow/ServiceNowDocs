---
title: Manually update an application service with changes from the CMDB
description: Ensure that an service instance is up-to-date and reflects all the latest changes to its configuration items \(CIs\). Regularly update application services to reflect any changes to CIs and their relationships in the CMDB.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Application services, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Manually update an application service with changes from the CMDB

Ensure that an service instance is up-to-date and reflects all the latest changes to its configuration items \(CIs\). Regularly update application services to reflect any changes to CIs and their relationships in the CMDB.

## Before you begin

Role required: app\_service\_admin

## About this task

There is no mechanism or an API that automatically updates application services that were created manually. Also, you may need to manually update application services discovered by Service Mapping, if they contain manually added CIs. You can only update application services which contain manually created entry points and which are not discovered by Service Mapping.

An example of a change is deleting CIs from the CMDB or connecting two CIs one of which is part of an application service. In the first case, your application service may show a CI that no longer exists. In the second case, on the contrary, the application service omits a CI.

An update might involve adding CIs of the following CI types, which cannot be added to an application service:

-   NAT \[cmdb\_ci\_translation\_rule\]
-   Endpoint \[cmdb\_ci\_endpoint\]
-   Qualifier \[cmdb\_ci\_qualifier\]
-   Application cluster \[cmdb\_ci\_application\_cluster\]

There are system records in the Manual CI Exclusions/Inclusions \[svc\_manual\_ci\_exclusions\_inclusions\] table. See [Components installed with application services](../../configuration-management/reference/components-installed-app-services.md#manual-ci-inclusion-exclusion-list) for more information.

**Note:** The Manual CI Exclusions/Inclusions \[svc\_manual\_ci\_exclusions\_inclusions\] table doesn't include CIs added using traversal rules.

Also, the system can connect a CI from the service instance only to actual CIs that exist in the CMDB, not a visualization of other items on the map like clusters or boundaries.

The maximum number of CI connections added to application services during this operation is controlled by the [sa.service.max\_ci\_service\_population](../../configuration-management/reference/components-installed-app-services.md) property. By default, the value is 1,000 \(one thousand connections\). Increasing the number of CI connections may cause performance issues. To adjust the maximum number of added CI connections, add the sa.service.max\_ci\_service\_population property, as described in [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

In environments with domain separation, only CIs belonging to the same domain as the service instance are added into the service instance. If there is a domain hierarchy, CIs must belong to the same child domain.

You can also update application services by using [APIs](../../configuration-management/concept/use-app-services-api.md).

## Procedure

1.  Navigate to **All** &gt; **CSDM** &gt; **Manage Technology Management Services** &gt; **Application Service**.

2.  On the Application Services list view, select the service instance that you want to update.

3.  Click **Advanced** and then click **Advanced Configurations**.

4.  On the Additional Info page, click the **Update with changes from CMDB** related link.

5.  Select a number in the **Up to** list to limit the number of levels of related items to be updated.

    If the specified number is higher than the number of levels of related items that already exist in the service instance, then the system adds the missing CIs and their connections.

    **Warning:** Specifying a lower number than the number of levels that already exist in the service instance, does not result in the removal of CIs from the service instance.

6.  Click **OK**.


## Result

-   The system updates the service instance with the changes from the CMDB and shows them on the map.
-   After the update process is complete, the service instance form opens.

