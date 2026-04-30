---
title: Synchronize data using a technical service offering
description: Synchronize group assignment attributes on entire CI classes and individual CIs that use a technical service offering.
locale: en-US
release: xanadu
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using dynamic CI groups, Navigate, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Synchronize data using a technical service offering

Synchronize group assignment attributes on entire CI classes and individual CIs that use a technical service offering.

## Before you begin

Role required: itil and itil\_admin

## About this task

Directly set the **Support group**, **Change group**, or **Managed by group** attributes in a technology management offering. The settings are applied to CIs that are associated with the technology management offering.

In addition to the method described in this procedure, you can use the CI Class Manager to set any CI property value. If the **Support group**, **Change group**, or **Managed by group** value is set in the technology management offering, the value specified by the technology management offering takes precedence. For more information, see [CI Class Manager](../../configuration-management/reference/ci-class-manager-landing-page.md).

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CMDB Groups** and create a new CMDB group.

    See [CMDB groups](../../../Chunk1817035602.md#) for details.

2.  Navigate to **All** &gt; **Configuration** &gt; **Dynamic CI Groups**.

3.  Create a new Dynamic CI group and associate it with the CMDB group that you created.

    ![CMDB: Create Dynamic CI group.](../image/create-dynamic-group.png)

    See [Manage Technical Services domain of the CSDM framework](../concept/manage-tech-servs-domain.md) for more information on Dynamic CI groups.

4.  Navigate to **All** &gt; **CSDM** &gt; **Technical Service Offering** and create a new technical service offering.

    See [Manage Technical Services domain of the CSDM framework](../concept/manage-tech-servs-domain.md) for more information on technical service offerings.

5.  Navigate to the **CI Relationships** table and select **New** and enter the following values:

    -   **Parent**: Select the technical service offering you created.
    -   **Child**: Select the Dynamic CI group you created.
    ![Create the relationship between the TSO and Dynamic CI group.](../image/create-ci-relationship.png)

6.  Select **Submit**.

    You have created a relationship between the technical service offering and the Dynamic CI group.

7.  Navigate to **All** &gt; **CSDM** &gt; **Technical Service Offering** and open the technical service offering that you created.

8.  Enter values in the following fields:

    -   Support group
    -   Change group
    -   Managed by group
    ![Create Technical Service Offering.](../image/create-tservice-offering.png)

9.  Right-click the header and select **Save**.

    A message confirms that data synchronization has been enabled for the fields.

10. The values that you specified are applied to the related Dynamic CI group and all associated CIs.

    If a new CI is added to the class, the data will be synchronized only after the scheduled CSDM Data Sync job is completed. If you need to synchronize the data immediately, navigate to **Scheduled Jobs** &gt; **CSDM Data Sync** and select **Execute**.


**Parent Topic:**[Synchronizing group assignment attributes](../concept/csdm-data-synchronize.md)

**Related topics**  


[CI Class Manager](../../configuration-management/reference/ci-class-manager-landing-page.md)

