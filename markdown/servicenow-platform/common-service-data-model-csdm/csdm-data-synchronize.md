---
title: Synchronizing group assignment attributes
description: To empower a particular user group to manage a collection of CIs or CI classes, set group assignment attributes through the technical service offering or the CI Class Manager. The operation synchronizes the group attribute data across all CIs that belong to the specified CI class or groups of CIs.
locale: en-US
release: xanadu
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Navigate, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Synchronizing group assignment attributes

To empower a particular user group to manage a collection of CIs or CI classes, set group assignment attributes through the technical service offering or the CI Class Manager. The operation synchronizes the group attribute data across all CIs that belong to the specified CI class or groups of CIs.

## Methods for synchronizing group assignment attributes

-   [Synchronize data using a technical service offering](../task/csdm-enable-tso.md): Directly set the **Support group**, **Change group**, or **Managed by group** attributes in a technology management offering. The settings are applied to CIs that are associated with the technology management offering.
-   [Set the group for a CI or an entire class of CIs](../task/csdm-data-synchronize-enable.md): Set the **Managed by group** attribute for a specific class in the CI Class Manager. All CIs within the class will have their **Managed by group** field populated based on the value specified in the CI Class Manager. With this method, the **Managed by group** setting is applied only to the CIs that aren’t associated with a technology management offering. For CIs that are managed by a technology management offering, the **Managed by group** field is first synchronized with its dynamic CI group. The field is then synchronized with the CIs in the dynamic CI group, overwriting the entry from the CI Class Manager.
-   Use Support Group and Change Group: By using dynamic CI groups, data synchronization enables you to manage data that cannot be discovered. The values in the **Support Group** and **Change Group** \(previously labeled **Assignment Group**\) fields in the cmdb\_ci table are synchronized with their related dynamic CI groups and with all the CIs that are contained as part of that dynamic CI group object.

## Team data synchronization

![Team data synchronization.](../image/csdm-team-data-sync.png)

-   **[Matching the usage of dynamic CI groups to service type](csdm-dynamic-ci-groups-by-service.md)**  
The type of service determines how you use dynamic CI groups.
-   **[Set the group for a CI or an entire class of CIs](../task/csdm-data-synchronize-enable.md)**  
Synchronize group assignment attributes on entire CI classes and individual CIs using the CI Class Manager.
-   **[Synchronize data using a technical service offering](../task/csdm-enable-tso.md)**  
Synchronize group assignment attributes on entire CI classes and individual CIs that use a technical service offering.

**Parent Topic:**[Managing the CSDM framework](csdm-content-frame-using.md)

**Related topics**  


[CI Class Manager](../../configuration-management/reference/ci-class-manager-landing-page.md)

