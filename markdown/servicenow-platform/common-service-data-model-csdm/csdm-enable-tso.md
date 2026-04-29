---
title: Synchronize user groups for a technology management offering
description: Synchronize group assignment attributes on entire CI classes and individual CIs by creating a dynamic CI group for use by a Technology management offering.
locale: en-US
release: australia
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Dynamic CI group and service type, Implement, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Synchronize user groups for a technology management offering

Synchronize group assignment attributes on entire CI classes and individual CIs by creating a dynamic CI group for use by a Technology management offering.

## Before you begin

Role required: itil and itil\_admin

## About this task

Directly set the **Support group**, **Change group**, or **Managed by group** attributes in a Technology management offering. The settings are applied to all CIs that are associated with the Technology management offering.

In addition to the method described in this procedure, you can use the CI Class Manager to set any CI property value. If the **Support group**, **Change group**, or **Managed by group** value is set in the Technology management offering, the value specified by the Technology management offering takes precedence. For more information, see [CI Class Manager](../../configuration-management/reference/ci-class-manager-landing-page.md).

**Note:** The **Managed by Group** setting identifies the group that manages a CI class \(ensuring that it is complete and correct\). It might or might not be the same group as repairs an individual CI.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CMDB Groups** and create a CMDB group.

    See [CMDB groups](../../configuration-management/concept/cmdb-groups.md#) for details.

2.  Navigate to **All** &gt; **Configuration** &gt; **Dynamic CI Groups**.

3.  Create a dynamic CI group and associate it with the CMDB group that you created.

    ![CMDB: Create a dynamic CI group.](../image/create-dynamic-group.png)

    See [Service Delivery domain in the CSDM model](../concept/manage-tech-servs-domain.md) for more information on dynamic CI groups.

4.  Navigate to **All** &gt; **CSDM** &gt; **Technical Service Offering** and create a Technology management offering.

    See [Service Delivery domain in the CSDM model](../concept/manage-tech-servs-domain.md) for more information on Technology management offerings.

5.  Navigate to the **CI Relationships** table, select **New**, and then enter the following values:

    -   **Parent**: Select the Technology management offering that you created.
    -   **Child**: Select the dynamic CI group that you created.
    ![Create the relationship between the Technology management offering and a dynamic CI group.](../image/create-ci-relationship.png)

6.  Select **Submit**.

    You have created a relationship between the Technology management offering and the dynamic CI group.

7.  Navigate to **All** &gt; **CSDM** &gt; **Technical Service Offering** and open the Technology management offering that you created.

8.  Enter values in the following fields:

    -   Support group
    -   Change group
    -   Managed by group
    ![Create a Technology management offering.](../image/create-tservice-offering.png)

9.  Select and hold \(or right-click\) the header and select **Save**.

    A message confirms that data synchronization has been enabled for the fields.

10. The values that you specified are applied to the related dynamic CI group and all associated CIs.

    **Note:** If a new CI is added to the class, the data will be synchronized only after the scheduled CSDM Data Synchronization job is completed. If you must synchronize the data immediately, navigate to **Scheduled Jobs** &gt; **CSDM Data Sync** and select **Execute**.


**Parent Topic:**[Matching the usage of dynamic CI groups to service type](../concept/csdm-dynamic-ci-groups-by-service.md)

**Related topics**  


[CI Class Manager](../../configuration-management/reference/ci-class-manager-landing-page.md)

