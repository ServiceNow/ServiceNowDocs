---
title: Create a service in Service Portfolio Management
description: Create services that benefit and add value to your internal organization and external customers and users.
locale: en-US
release: xanadu
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using Service Portfolio Management, Service Portfolio Management, IT Service Management]
---

# Create a service in Service Portfolio Management

Create services that benefit and add value to your internal organization and external customers and users.

## Before you begin

Role required: portfolio\_admin or service\_editor

## About this task

All occurrences of the table and reference field label **Business Service** throughout the product have changed to **Service**. For example, the Business Service form has changed to Service form. This change is for new instances only and doesn't affect existing upgraded instances.

**Note:** You can also create and edit services and service offerings by using the Service Builder application. Service Builder provides a walk-through experience with contextual help along the way. For more information, see [Service Builder](../../service-builder/concept/service-builder.md).

## Procedure

1.  Navigate to **All** &gt; **Service Portfolio Management** &gt; **Services** and select **New**.

    Alternatively, to edit an existing service, select the name of the service to open the form. Change any of the form field data as needed. To delete an existing service, select the **Delete** button in the form header.

2.  On the form, fill in the fields.

<table id="table_tdm_5n2_4gb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique name that reflects the nature of the service.

</td></tr><tr><td>

Service portfolio

</td><td>

Service portfolio this service is associated with.

</td></tr><tr><td>

Taxonomy node

</td><td>

Taxonomy leaf node within a portfolio this service is associated with.

</td></tr><tr><td>

Phase

</td><td>

Phase that the service is in. Available values are: **Pipeline**, **Catalog**, and **Retired**.

</td></tr><tr><td>

Status

</td><td>

That status of the service phase.

</td></tr><tr><td>

Short Description

</td><td>

Type of service. Available values are: **Business Service**, **Technical Service**, and **Application Service**.

</td></tr><tr><td>

Owned by

</td><td>

The service owner responsible for this service in the organization.

</td></tr><tr><td>

Delivery manager

</td><td>

The delivery manager for the service.

</td></tr><tr><td>

Business relation manager

</td><td>

Relationship manager for this service.

</td></tr><tr><td colspan="2">

**Important:** The following two fields only appear if you're using the deprecated Service Owner Workspace plugin. For more information on the deprecation of Service Owner Workspace, see [Service Owner Workspace](../../service-owner-workspace/concept/SPM2-premium.md).

</td></tr><tr><td>

Performance score

</td><td>

Most recent performance score. Populated after the service is active. The performance score is calculated by a nightly script and can’t be changed.

</td></tr><tr><td>

CSAT score

</td><td>

Customer service feedback score.

</td></tr></tbody>
</table>3.  Select the **General** tab.

4.  On the form, fill in the fields.

<table id="table_z2x_pc4_h4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Automatically generated unique identification for a new service record. Its value consists of a 'BSN' string and a unique number. Other forms and scripts can reference this identification.The **Number** field is visible with the Service Portfolio form view.

**Note:** The **Number** field in service records that were created before the field was added, is null.

</td></tr><tr><td>

Version

</td><td>

Version of the service.

</td></tr><tr><td>

Aliases

</td><td>

Other names used for this service.

</td></tr><tr><td>

Service classification

</td><td>

Type of service. Available values are: **Business Service**, **Technical Service**, and **Application Service**.

</td></tr><tr><td>

Consumer type

</td><td>

Type of consumer. Available values are: **Internal**, **External**, and **Internal and External**.

</td></tr><tr><td>

Start date

</td><td>

Date the service is available.

</td></tr><tr><td>

End date

</td><td>

The date the service is retired.

</td></tr><tr><td>

Last review date

</td><td>

The date the service was last reviewed.

</td></tr></tbody>
</table>5.  Select the **Team** tab.

6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Delegate|A person authorized to manage the service on behalf of the service owner.|
    |Business contact|Person to contact for issues related to this service.|
    |Vendor|The vendor providing this service.|
    |Stakeholders|People with an interest or concern regarding this service.|

7.  Select the **Business Need** tab.

8.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Business need|Business need this service supports.|
    |Business criticality|Criticality level that defines the importance of the service in your organization.|

9.  After completing the form, select and hold \(or right-click\) the header bar and select **Save** from the pop-up menu.

    The related lists for the service appear. View associated or create the following:

    -   Offerings
    -   In Scope
    -   Out of Scope
    -   Services I depend On
    -   Services Dependent On Me
    -   Incidents
    -   Problems
    -   Change Requests
    -   Other tasks
    -   Knowledge Articles
    -   Service Offering Node Weights
    -   Improvement Initiatives
10. Select **Submit** to save your service or select **Update** after editing a service.


**Parent Topic:**[Using Service Portfolio Management](../concept/SPM2-using.md)

