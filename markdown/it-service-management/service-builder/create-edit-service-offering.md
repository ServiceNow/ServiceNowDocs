---
title: Create a service offering in Service Builder
description: Create a service offering to define and view the products or applications that make up your service in Service Builder.
locale: en-US
release: australia
product: Service Builder
classification: service-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Service Builder, IT Service Management]
---

# Create a service offering in Service Builder

Create a service offering to define and view the products or applications that make up your service in Service Builder.

## Before you begin

Role required: service\_author or service\_editor

## About this task

A service offering represents how a service is provided and who it is for. A service must have at least one offering to be published. The workflow guides you to create a service offering in a logical order:

1.  **Details**
2.  **Team**
3.  **Operations**
4.  **Financials**
5.  **Offering performance**

**Tip:** You can cancel out of creating a service anytime by selecting the **Cancel** button \(next to the **Save** button\). Also, to return to the home page at any time while creating or editing a service, select ![Home icon.](../../digital-portfolio-management/image/home-polaris-primary2x.png).

To create a service and service offering, you must be assigned the service\_author role. To edit \(not create\) a service or service offering, you must be assigned the service\_editor role.

## Procedure

1.  Navigate to **All** &gt; **Service Portfolio Management** &gt; **Service Builder**.

2.  To add or edit a service offering, select the service and then select the **Manage offerings** tab.

3.  To add a new service offering, select **New**.

4.  On the form, fill in the fields.

5.  <table id="table_dth_3zv_tqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Offering name

</td><td>

Unique name for the offering that associates with the parent service.

</td></tr><tr><td>

Consumer type

</td><td>

The consumer type determines if the service is provided internally to the business or to the employees, or externally to customers, or to both. The options are:

-   Internal
-   External
-   Internal and External


</td></tr><tr><td>

Business criticality

</td><td>

Signifies the importance of this offering to business operations. The value of this field could be used to trigger business logic. For example, your most critical offerings may warrant special treatment for disaster recovery.

</td></tr><tr><td>

Lifecycle status

</td><td>

The stage and status for the service that you're creating.

 If you have the CSDM Activation plugin installed \[com.snc.cmdb.csdm.activation\], then the CSDM compliant lifecycle fields display.

 If you don't have the plugin installed, then the legacy Service Portfolio Management phase and status fields display.

 For information on the different types of fields, see [Apply the CSDM guidelines to Digital Portfolio Management](../../digital-portfolio-management/reference/dpm-csdm.md).

</td></tr><tr><td>

Description

</td><td>

A concise description of the service offering to ensure that it makes sense to the end user or consumer of the service.

</td></tr><tr><td>

Prerequisites

</td><td>

Defines anything that is required to request or use this service offering.

</td></tr></tbody>
</table>6.  Select the **Team** tab or select **Continue to Team**.

7.  On the form, fill in the fields.

8.  <table id="table_epl_g1w_tqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Owned by

</td><td>

Person accountable for the service offering and can edit the service at any time. This person is the service owner. Service owners must have the service\_author role.

</td></tr><tr><td>

Managed by

</td><td>

Person responsible for the day-to-day management of this service.

</td></tr><tr><td>

Delegate

</td><td>

Person that can edit the service offering and who can act on behalf of the service owner. Delegates must be assigned the service\_editor role.

</td></tr><tr><td>

Delivery manager

</td><td>

Person responsible for the daily management and delivery of the service offering.

</td></tr><tr><td>

Support group

</td><td>

Group that provides expert support to the service offering. This group is usually a level 2 support team.

</td></tr><tr><td>

Change group

</td><td>

Team responsible for providing change management for the service offering.

</td></tr><tr><td>

Vendor

</td><td>

Vendor that may help deliver and support the service offering. This field helps show and track accountability for service offering delivery.

</td></tr><tr><td>

Department

</td><td>

Department that is accountable for the management of this service.

</td></tr><tr><td>

Company

</td><td>

Company that is accountable for the management and delivery of this service \(could be a vendor\).

</td></tr><tr><td>

Stakeholders

</td><td>

Individuals that have a vested interest in the service offering.

</td></tr></tbody>
</table>9.  Select the **Operations** tab or select **Continue to Operations**.

10. On the form, fill in the fields.

11. <table id="table_c1k_t1w_tqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Selected groups

</td><td>

Subscriber groups that have an interest in the service offering.

</td></tr><tr><td>

Selected departments

</td><td>

Departments that have an interest in the service offering.

</td></tr><tr><td>

Selected locations

</td><td>

Users by location.

</td></tr><tr><td>

Selected users

</td><td>

Individuals impacted by the service offering.

</td></tr><tr><td>

Selected companies

</td><td>

Individuals impacted by the service offering that are defined by the core company table. These individuals represent all users related to a given company.**Note:** You may need to scroll down to see the remaining fields on this form.

</td></tr><tr><td>

Selected commitments

</td><td>

Select commitments, for example, service level agreements and availability commitments. Commitments may be defined in a contract for the service offering or based on standards defined by your company.

</td></tr><tr><td>

Service level requirements

</td><td>

Service level requirements for the service offering.

</td></tr><tr><td>

Active contract

</td><td>

Active contract to maintain awareness of the service commitments.

</td></tr><tr><td>

Additional contracts

</td><td>

Supporting, secondary, or past contracts related to the service offering.

</td></tr><tr><td>

Selected catalog items

</td><td>

Catalog item to track the request activity for all catalog items associated with this offering. A single offering can have multiple catalog items.

</td></tr><tr><td>

Offerings I depend on

</td><td>

Other service offerings that your service offering depends on. For example, if another offering experiences an outage, your offering availability may be impacted or degraded as a result.

</td></tr><tr><td>

Service instance I depend on

</td><td>

Applies to business services. Service instances that the service offering depends on.

</td></tr></tbody>
</table>12. Select the **Financials** tab or select **Continue to Financials**.

13. On the form, fill in the fields.

14. A Service Offering **Cost unit** is a unit of measurement of the service offering. For example, let's say your service is Microsoft Suite. The cost unit would be the number of users. It could also be the API calls. A cost model that's **Per unit** refers to the price per unit. In this case, it would be the price per Microsoft Suite user or API call. The **Estimated Spend** for the Per unit cost model is determined by the price per unit and units per period. A cost model that's **Fixed** refers to a predetermined and agreed-upon total cost. For example, you set a specific price for your Microsoft Suite service and stick to it. The cost unit is still the same \(users or API calls\), but the **Estimated Spend** is determined by the agreed-upon price.

    |Field|Description|
    |-----|-----------|
    |Price model|How the service offering is to be priced. Your selection determines the next field to display.|
    |Price unit|If the price model is set to **Per Unit**, then enter the price unit in this field. For example, license or subscription.|
    |Price|If the price model is set to **Fixed**, then enter the price in this field. Be sure to enter the currency symbol as well \(for example, $ for United States dollar\).|
    |Unit description|If the price model is set to **Per Unit**, then use this field to describe what is included in the unit.|

15. Fill in the rest of the fields.

    The following fields appear conditionally according to the cost source selected in Service Portfolio Management. These fields are enabled as part of the financial optional plugin for Service Portfolio Management. For financial information, the required plugin is com.snc.financial\_management\_for\_spm. For estimate spend information, the required plugin is com.snc.spm.spend. Both plugins require ITSM Pro SKU.

16. |Field|Description|
|-----|-----------|
|Cost model|The cost model that determines how the estimated spend is calculated.|
|Offering cost|If the cost model is set to **Fixed**, then the cost should represent the estimated cost of the offering per time period.|
|Time period|Interval that you want to track the estimated spend \(**day**, **month**, **quarter**, **year**\).|
|Cost Unit|If the cost model is set to **Per unit**, the cost should represent the cost per unit.|
|Units per period|The number of units per period.|
|Estimated spend|The estimated spend for this item.|

17. Select the **Offering Performance** tab or select **Continue to Offering Performance**.

18. In the field, select the KPI group that you want to measure this service offering by.

19. Select **Save &amp; Close**.


