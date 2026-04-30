---
title: Convert legacy manual services to dynamic application services
description: Unify the way that you manage services in your organization by converting legacy manual services into dynamic application services. Conversion lets you streamline the different types of services in your organization, leverage ITOM capabilities, and align with the Common Service Data Model \(CSDM\).
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Application services, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Convert legacy manual services to dynamic application services

Unify the way that you manage services in your organization by converting legacy manual services into dynamic application services. Conversion lets you streamline the different types of services in your organization, leverage ITOM capabilities, and align with the Common Service Data Model \(CSDM\).

## Before you begin

Role required: app\_service\_admin

## About this task

**Note:** Converting a legacy manual service to a dynamic application service is irreversible. Once converted, you can’t revert it back to a legacy manual service. However, you can convert a dynamic application service to a manual application service.

You can't edit a dynamic application service directly. If you remove a CI from the map, it reappears once the service is recalculated. To ensure permanent changes, update the CI relationships in the CMDB CI Relationship \[cmdb\_rel\_ci\] table.

During conversion, the following changes and processes occur:

-   A change to the record class moves the service record from the Service \[cmdb\_ci\_service\] or the Manual Service \[cmdb\_ci\_service\_manual\] table to the \[cmdb\_ci\_service\_calculated\] table.
-   The dynamic application service is configured with all the original attributes of the legacy manual service such as name, owner, and operational status.
-   Related items from the legacy manual service are added to the converted dynamic application service, up to three levels by default.
-   All connections created between CIs in the dynamic application service are endpoint CIs with the relationship **uses**, **implement**, or **application flow**.
-   Event Management, if activated, applies CI impact rules to CIs that are associated with alerts and that are part of the application service. Event Management deploys CI impact rules for alert monitoring.

A conversion might involve adding non-compliant CIs, which can’t be added to an application service:

-   NAT \[cmdb\_ci\_translation\_rule\]
-   Endpoint \[cmdb\_ci\_endpoint\]
-   Qualifier \[cmdb\_ci\_qualifier\]
-   Application cluster \[cmdb\_ci\_application\_cluster\]

If the original manual service contains related items belonging to these CI types, then these CIs or connections coming from them aren’t added to the dynamic service. If necessary, you can prevent other CI types from being added to application services by modifying the Manual CI Inclusions/Exclusions \[svc\_manual\_ci\_exclusions\_inclusions.list\] table.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Application Services** &gt; **Application Services**.

2.  Confirm that the view is set to the default view.

    1.  Select the List controls icon for the list view.

    2.  Select **View** and then select **Default view**.

3.  Open the legacy manual service that you want to convert to a dynamic application service.

4.  In the Related Links section on the service form, select **Convert to Dynamic Service**.


