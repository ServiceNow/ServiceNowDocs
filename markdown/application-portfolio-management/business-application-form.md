---
title: Business Application Form
description: Enterprise Architecture \(formerly APM\) helps system admins add any business application to assess and track its costs, usage, business value, functional fitment, and risks.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Reference, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Business Application Form

Enterprise Architecture \(formerly APM\) helps system admins add any business application to assess and track its costs, usage, business value, functional fitment, and risks.

## Business Application Form fields

<table id="table_umq_nqn_cs"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the business application.

</td></tr><tr><td>

Number

</td><td>

Unique, auto-generated identification number with a configurable prefix for the business application record.

</td></tr><tr><td>

Business process

</td><td>

Business process for which the application is used.

</td></tr><tr><td>

Portfolio

</td><td>

Name of the portfolio to which the application belongs.This field appears when you activate the PPM Standard \(com.snc.financial\_planning\_pmo\) plugin.

</td></tr><tr><td>

Application type

</td><td>

Type of application. This field indicates whether the application is custom or commercial.-   **Homegrown**: Application that is built in-house.
-   **End-user computing**: The application is used by end users to perform their daily tasks.
-   **Commercial off-the-shelf \(COTS\)**: Application is a commercial application purchased from another company.
-   **SaaS**: Application is a cloud application managed by third-party vendor.

</td></tr><tr><td>

Publisher

</td><td>

Name of the application publisher.

</td></tr><tr><td>

Architecture type

</td><td>

Type of application architecture.-   **Client Server**: Application structure that divides tasks between the service providers and service requesters.
-   **N-Tier**: A multi-layered architecture where presentation, processing, and data management exist as physically separate layers.
-   **Web-based**: Applications accessed over a network connection.
-   **Other**: Any other type of architecture.
-   **Platform Host**: Hardware or software that hosts the business application.
-   **Platform Application**: Application that runs on a platform and can be associated to a host.

In this case, the business application relies on the platform for standard operations such as development tools, execution services, and data services.


</td></tr><tr><td>

Platform Host

</td><td>

A hardware or software that hosts the business application.This field is required if you select the **Platform Application** value in **Architecture type** field.

</td></tr><tr><td>

Install type

</td><td>

Type of install. Use the following options:-   **On-Premises**
-   **Cloud**
-   **Hybrid**
-   **Third Party Hosted**

</td></tr><tr><td>

Platform

</td><td>

Applications hosted by platform.

</td></tr><tr><td>

Business Unit

</td><td>

Business unit that is associated with the selected business application.

</td></tr><tr><td>

Department

</td><td>

Department that is associated with the selected business application.

</td></tr><tr><td>

Installed

</td><td>

Date and time when the application was installed.

</td></tr><tr><td>

Status

</td><td>

Operational status of the application. Use the following options:-   Implementing
-   In Production
-   Pilot
-   Retired

Auditing is enabled. Thus, whenever a user updates the value in this field, the **Activities** field in the **Activities** tab displays the update.

</td></tr><tr><td>

Life-Cycle Stage

</td><td>

Life-cycle stage of the application. This field is auto-populated based on the value selected in the **Status** field. The data is fetched from the life-cycle mapping \[life\_cycle\_mapping\] table.

</td></tr><tr><td>

Life-Cycle Stage Status

</td><td>

Status of the life-cycle stage of the application. This field is auto-populated based on the value selected in the **Status** field. The data is fetched from the life-cycle mapping \[life\_cycle\_mapping\] table.

</td></tr><tr><td>

Application scoring profile

</td><td>

The profile used to calculate the application score for strategy.

</td></tr><tr><td>

Application category

</td><td>

The application purpose and function. Use this information to rationalize or consolidate applications.

</td></tr><tr><td>

Application family

</td><td>

A set of related applications that have a common platform or vendor.

</td></tr><tr><td>

Technology stack

</td><td>

Technology stack on which the application was built.

</td></tr><tr><td>

User base

</td><td>

Number of users using the applications.Auditing is enabled. Thus, whenever a user updates the record in this field, the **Activities** field in the **Activities** tab displays the update.

</td></tr><tr><td>

Active user count

</td><td>

Number of active users out of the overall user base. Auditing is enabled for the field.

</td></tr><tr><td>

Last change applied date

</td><td>

Date on which the application was last updated. Auditing is enabled for the field.

</td></tr><tr><td>

Accessibility level

</td><td>

Accessibility level of the business application. Use the following options:-   A \(lowest\)
-   AA \(mid-range\)
-   AAA \(highest\)

</td></tr><tr><td>

Age in months

</td><td>

Age of the business application in months. This field is auto-populated when the date and time is entered in the **Installed** field.

</td></tr><tr><td>

Description

</td><td>

Unique description of the application.

</td></tr><tr><td>

Model ID

</td><td>

Product model ID of the business application.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Vendor|Vendor details of the application.|
|Support vendor|Vendor who currently supports the application.|
|Contract end date|Expiry date of the subscription contract or the support contract. Auditing is enabled for the field.|

<table id="table_gmk_4bt_ncc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Planned Disposition

</td><td>

Planned disposition of a business application. Use the following options:-   Invest
-   Sustain
-   Migrate
-   Retire

</td></tr><tr><td>

Migration Strategy

</td><td>

Migration strategy for the business application. This field appears only when **Migrate** is selected from the **Planned Disposition** field. Use the following options:-   Rehost
-   Replatform
-   Repurchase
-   Refactor

</td></tr><tr><td>

Target Business Application

</td><td>

Name of the business application for which you’re adding the planned disposition. This field appears only when **Migrate** is selected from the **Planned Disposition** field.

</td></tr><tr><td>

Reasoning

</td><td>

Reason for the planned disposition decision.

</td></tr></tbody>
</table><table id="table_xf5_dct_ncc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Portfolio manager

</td><td>

Owner of the portfolio, typically from IT.This field appears when you activate the PPM Standard plugin \(com.snc.financial\_planning\_pmo\).

</td></tr><tr><td>

Business owner

</td><td>

Person who owns the application from the business side. Every application should have an assigned business owner.

</td></tr><tr><td>

Managed by

</td><td>

User managing the business application.

</td></tr><tr><td>

Managed by group

</td><td>

User group managing the business application.

</td></tr><tr><td>

IT Application owner

</td><td>

Person who owns the application from the IT side.The business application must have an owner assigned to it.

If you’re designated as the IT Application owner, then you can view all the applications for which you’re the owner in the **My Applications** menu.

</td></tr><tr><td>

Last updated by

</td><td>

Person who last updated the application record.

</td></tr><tr><td>

Supported by

</td><td>

User supporting the business application.

</td></tr><tr><td>

Support group

</td><td>

User group supporting the business application.

</td></tr></tbody>
</table><table id="table_isz_kct_ncc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Business criticality

</td><td>

How critical the application is to the business. Auditing is enabled for the field.

</td></tr><tr><td>

Emergency tier

</td><td>

Actions or plans executed for the application in an emergency situation.

</td></tr><tr><td>

Data classification

</td><td>

Security level for the data in the application. This attribute determines which Governance, Risk, and Compliance \(GRC\) policies are applicable to the application.Category of data. The base system provides Internal, Public, Confidential, and Highly Sensitive categories.

Auditing is enabled for the field.

</td></tr><tr><td>

Certified

</td><td>

Status of the application that it meets requirements or complies with the policies of your organization.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Work notes|Work notes entered by you.|

**Parent Topic:**[Enterprise Architecture \(formerly Application Portfolio Management\) reference](apm-reference.md)

**Related topics**  


[Add or edit a business application - Legacy](../task/manage-business-appln.md)

