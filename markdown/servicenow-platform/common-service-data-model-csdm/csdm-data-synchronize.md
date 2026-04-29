---
title: Synchronizing group assignment attributes
description: To empower a particular user group to manage a collection of CIs or CI classes, set group assignment attributes through the Technology management offering or the CI Class Manager. The operation synchronizes the group attribute data across all CIs that belong to the specified CI class or groups of CIs.
locale: en-US
release: australia
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Dynamic CI group and service type, Implement, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Synchronizing group assignment attributes

To empower a particular user group to manage a collection of CIs or CI classes, set group assignment attributes through the Technology management offering or the CI Class Manager. The operation synchronizes the group attribute data across all CIs that belong to the specified CI class or groups of CIs.

## Methods for synchronizing group assignment attributes

**Note:** The **Managed by Group** setting identifies the group that manages a CI class \(ensuring that it is complete and correct\). It might or might not be the same group as repairs an individual CI.

-   [Synchronize user groups for a technology management offering](../task/csdm-enable-tso.md): Directly set the **Support group**, **Change group**, or **Managed by group** attributes in a Technology management offering. The settings are applied to all CIs that are associated with the Technology management offering.
-   [Set the group for a CI or an entire class of CIs](../task/csdm-data-synchronize-enable.md): Set the **Managed by group** attribute for a specific class in the CI Class Manager. All CIs within the class will have their **Managed by group** field populated based on the value specified in the CI Class Manager. With this method, the **Managed by group** setting is applied only to the CIs that aren’t associated with a Technology management offering. For CIs that are managed by a Technology management offering, the **Managed by group** field is first synchronized with its dynamic CI group. The field is then synchronized with the CIs in the dynamic CI group, overwriting the entry from the CI Class Manager. For instructions, see [Synchronize user groups for a technology management offering](../task/csdm-enable-tso.md).
-   Use Support Group and Change Group: By using dynamic CI groups, data synchronization enables you to manage data that cannot be discovered. The values in the **Support Group** and **Change Group** \(previously labeled **Assignment Group**\) fields in the cmdb\_ci table are synchronized with their related dynamic CI groups and with all the CIs that are contained as part of that dynamic CI group object.

## Team data synchronization

![Team data synchronization.](../image/csdm-team-data-sync.png)

**Parent Topic:**[Matching the usage of dynamic CI groups to service type](csdm-dynamic-ci-groups-by-service.md)

**Related topics**  


[CI Class Manager](../../configuration-management/reference/ci-class-manager-landing-page.md)

[Synchronize user groups for a technology management offering](../task/csdm-enable-tso.md)

