---
title: Create a service offering in Service Portfolio Management
description: Create service offerings to define services, document them, track performance against defined availability commitments, and relay the performance information in real time to your end users.
locale: en-US
release: australia
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Service offerings in Service Portfolio Management, Use, Service Portfolio Management, IT Service Management]
---

# Create a service offering in Service Portfolio Management

Create service offerings to define services, document them, track performance against defined availability commitments, and relay the performance information in real time to your end users.

## Before you begin

Role required: portfolio\_admin

## About this task

Often the data that's defined on a service and on its child offerings are identical. For example, the same person may own a service and its offerings, as defined in the **Owned by** field on the **Service** form. However, flexibility exists for defined data to be different between services and child offerings if the organization desires. For example, one person may own the service while another person owns the child offering.

Link service offerings to catalog items required to provision a service. Each service offering has commitments, which in turn, have service level agreements.

A service offering consists of a set of service commitments, which uniquely define the level of service in terms of availability, scope, and pricing. For example, an organization may offer two levels of Desktop Support in your organization. A Standard offering of upgrades and virus protection. And an Executive offering with the standard commitments plus some type of availability guarantee, such as 98% availability from 8-5 on weekdays.

When an offering is added to a service for the first time, some Offering form field values are inherited from the parent Service record. These form fields are: **Owned by**, **Business criticality**, **Delivery Manager**, and **Delegate**. When an offering is added and the parent Service record has empty field values, these fields are also empty on the Offering record. When you first insert an offering into a service, the parent Service record field values overwrite any existing values in the Offering record. You can update the fields after you’ve added the offering, if necessary.

You can also auto-create service offerings when creating a service portfolio. For more information, see [Create portfolios in Service Portfolio Management](create-or-modify-SPM2-portfolios.md).

## Procedure

1.  Navigate to **All** &gt; **Service Portfolio Management** &gt; **Service Offerings** and select **New**.

    Alternatively, to edit an existing service offering, select the name of the service offering to open the form. Change any of the form field data as needed. To delete an existing service, select the **Delete** button in the form header.

2.  Fill in the form fields.

<table id="table_tdm_5n2_4gb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name that reflects the nature of the service.

</td></tr><tr><td>

Parent

</td><td>

The parent service.

</td></tr><tr><td>

Phase

</td><td>

Phase that the service is in. Available values are: **Pipeline**, **Catalog**, and **Retired**.

</td></tr><tr><td>

Status

</td><td>

Status of the service per phase.

</td></tr><tr><td>

Short description

</td><td>

Brief details about the service portfolio.

</td></tr><tr><td>

Description

</td><td>

Comprehensive details about the service offering.

</td></tr><tr><td>

CSAT score

</td><td>

Customer satisfaction feedback score.

</td></tr><tr><td>

Total Subscribers

</td><td>

Number of subscriptions for this service offering. Total subscribers are calculated by a nightly script. **Note:** Only an admin can change the score, if necessary.

</td></tr><tr><td>

Owned by

</td><td>

Service owner responsible for this service in the organization.**Note:** This value is inherited from the parent Service record, but you can update.

</td></tr><tr><td>

Performance score**Note:** This field displays if you're using the deprecated Service Owner Workspace plugin. For more information on the deprecation of Service Owner Workspace, see .

</td><td>

Most recent performance score. Populated after the service is active. The performance score is calculated by a nightly script. **Note:** Only an admin can change the score, if necessary.

</td></tr></tbody>
</table>3.  Select the **General** tab to complete the General section of the form.

<table id="table_pkl_pg4_h4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Aliases

</td><td>

Other names used for this service.

</td></tr><tr><td>

Business criticality

</td><td>

Degree of how critical this service offering is to the business. You can base a demand response strategy off this value.**Note:** This value is inherited from the parent Service record, but you can update.

</td></tr><tr><td>

Consumer type

</td><td>

Type of consumer. Available values are: **Internal** and **External**.

</td></tr><tr><td>

Service classification

</td><td>

Type of service. Available values are: **Business Service**, **Technical Service**, and **Application Service**.

</td></tr><tr><td>

Version

</td><td>

Version of the service offering.

</td></tr><tr><td>

Start date

</td><td>

Date the service is available.

</td></tr><tr><td>

End date

</td><td>

Date the service is retired.

</td></tr><tr><td>

Location

</td><td>

Physical location of the service.

</td></tr><tr><td>

CSAT Survey Frequency

</td><td>

How often a customer survey is sent.

</td></tr><tr><td>

CSAT Survey Last Sent

</td><td>

Last time a customer satisfaction survey was sent.

</td></tr></tbody>
</table>4.  Select the **Team** tab to complete the Team section of the form.

    The Teams related list enables you to assign different group types to support a service offering. For more information, see [Teams related list](https://www.servicenow.com/docs/access?context=teams-related-list&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) and [Assign multiple teams to support a service offering](spm2-assign-teams.md).

<table id="table_lms_5h4_h4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Delivery Manager

</td><td>

The delivery manager for this service.**Note:** This value is inherited from the parent Service record, but you can update.

</td></tr><tr><td>

Delegate

</td><td>

Person authorized to manage the service along with the service owner. **Note:** This value is inherited from the parent Service record, but you can update.

</td></tr><tr><td>

Support group

</td><td>

Group managing the service. See [Assign multiple teams to support a service offering](spm2-assign-teams.md).

</td></tr><tr><td>

Vendor

</td><td>

The vendor providing this service.

</td></tr><tr><td>

Stakeholders

</td><td>

People with an interest or concern regarding this service.

</td></tr></tbody>
</table>5.  Select the **Price** tab to complete the Price section of the form.

<table id="table_knm_4m4_h4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Price model

</td><td>

Pricing structure for a service offering as defined in the parent service.The **Price model** field is read only. This value is set in the parent service.

</td></tr><tr><td>

Price unit

</td><td>

Short name of the unit for this service. Appears when **Per Unit** is chosen for the **Price Model** type in the parent service.The **Price unit** field is read only. This value is set in the parent service.

</td></tr><tr><td>

Price

</td><td>

Price and currency.

</td></tr><tr><td>

Unit Description

</td><td>

Longer description of a unit of this offering.

</td></tr></tbody>
</table>6.  Select the **Operations** tab to complete the Operations section of the form.

    |Field|Description|
    |-----|-----------|
    |Contract|Associated contract number.|
    |Maintenance schedule|Time during which maintenance is scheduled.|
    |Service level requirement|Field captures the requirements, which include the service level agreements and service level targets, for the service.|
    |Prerequisites|Prerequisites for this service offering.|
    |Compatibility dependencies|Compatibility dependencies for this service offering.|
    |Monitoring requirements|Requirements to monitor this service offering.|

7.  Select the **Estimated Spend** tab to view the Estimated Spend section.

    **Important:** This step and the next one are optional because they only apply if you're using the deprecated Service Owner Workspace plugin. For more information on the deprecation of Service Owner Workspace, see .

8.  Choose a value for the **Cost model** field.

    Choices include the default **None**, **Fixed**, and **Per unit**. View read-only data in the **Estimated spend** field.

9.  After completing the form, select and hold \(or right-click\) the header bar and select **Save** from the pop-up menu.

    The **Related Links** and related lists for the offering appear.

10. In **Related Links** you can create an offering improvement initiative, edit offering metric weights, and subscribe to the offering by selecting the associated link.

    **Important:** This step is optional because it only applies if you're using the deprecated Service Owner Workspace plugin. For more information on the deprecation of Service Owner Workspace, see .

11. View associated related lists and items.

    View associated or create new:

    -   Service Commitments
    -   Service Offerings I Depend On
    -   Service Offerings Dependent On Me
    -   Outages
    -   Incidents
    -   Problems
    -   Change Requests
    -   Other Tasks
    -   Knowledge Articles
    -   Catalog Items
    -   Subscribed by Group
    -   Subscribed by Location
    -   Subscribed by Department
    -   Subscribed by User
    -   Subscribed by Company
    -   Performance Metrics
    -   Improvement Initiatives
12. Select **Submit** to save your service offering or select **Update** after editing a service offering.


**Parent Topic:**[Service offerings in Service Portfolio Management](../concept/SPM2-service-offerings.md)

**Related topics**  


[Teams related list](https://www.servicenow.com/docs/access?context=teams-related-list&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

[Assign multiple teams to support a service offering](spm2-assign-teams.md)

