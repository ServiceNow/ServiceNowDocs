---
title: Matching the usage of dynamic CI groups to service type
description: The type of service determines how you use dynamic CI groups.
locale: en-US
release: yokohama
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2025-06-25"
reading_time_minutes: 3
breadcrumb: [Navigate, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Matching the usage of dynamic CI groups to service type

The type of service determines how you use dynamic CI groups.

## Dynamic CI groups

-   A dynamic CI group is a user-defined collection of CIs that is used as a group Cl in the Cl field of the record for Incident Management, Problem Management, and Change Management.
-   You set up dynamic Cl groups based on common attributes or criteria.
-   A dynamic CI group cannot contain other groups.

## Dynamic CI groups for technology management services \(formerly Technical services\)

You can group up to 10,000 similar items that are associated with a technology management service and its associated technical service offering. In this usage, a dynamic CI group functions as a collection of CIs that are managed individually. Because the CIs aren't necessarily related to each other, service associations are not needed. Impact analysis \(through Incident Management, Problem Management, or Change Management\) is also not meaningful or expected for unrelated CIs. Here are some examples:

-   Servers with a particular operating system
-   Network gear based on location
-   Application servers based on a running process
-   CIs that make up a service instance
-   CIs that share a particular support group

The **Service Classification** attribute identifies the service as a technology management service. The ownership sync process assigns CI ownership through the technology management service, as described in [Synchronizing group assignment attributes](csdm-data-synchronize.md).

## Dynamic CI groups for service instances

For a service instance \(formerly application service\), impact analysis outcomes are expected because when any individual CI is impacted, the entire dynamic CI group is affected. All related business services or technology management services are also affected. Because of this interdependence, you must establish service associations and impact analysis is important.

The **Service Classification** attribute identifies the service as a service instance.

See [Populate an application service using the Dynamic CI Group method](../../configuration-management/task/populate-app-service-dynamic-group.md).

-   **[Synchronizing group assignment attributes](csdm-data-synchronize.md)**  
To empower a particular user group to manage a collection of CIs or CI classes, set group assignment attributes through the Technical service offering or the CI Class Manager. The operation synchronizes the group attribute data across all CIs that belong to the specified CI class or groups of CIs.
-   **[Set the group for a CI or an entire class of CIs](../task/csdm-data-synchronize-enable.md)**  
Synchronize group assignment attributes on entire CI classes and individual CIs using the CI Class Manager.
-   **[Synchronize user groups for a technology management offering](../task/csdm-enable-tso.md)**  
Synchronize group assignment attributes on entire CI classes and individual CIs in a technical service offering.

**Parent Topic:**[Managing the CSDM framework](csdm-content-frame-using.md)

