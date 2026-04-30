---
title: Business application form
description: Using the business application form, you can add any business application to assess and track its costs, usage, business value, functional fitment, and risks.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Reference, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Business application form

Using the business application form, you can add any business application to assess and track its costs, usage, business value, functional fitment, and risks.

<table id="table_i2h_bpp_yyb"><thead><tr><th>

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

A unique, auto-generated identification number with a configurable prefix for the business application record.

</td></tr><tr><td>

Business process

</td><td>

Business process that the application is used for.

</td></tr><tr><td>

Application type

</td><td>

Type of application. This field indicates whether the application is custom or commercial.

-   **Homegrown**: The application is built in-house.
-   **End-user computing \(EUC\)**: The application is used by end users to perform their daily tasks.
-   **Commercial off-the-shelf \(COTS\)**: The application is a commercial application purchased from another company.
-   **SaaS**: The application is a cloud application managed by a third-party vendor.

</td></tr><tr><td>

Publisher

</td><td>

Name of the application publisher.

</td></tr><tr><td>

Architecture type

</td><td>

Type of application architecture.

-   **Client Server**: Application structure that divides tasks between the service providers and service requesters.
-   **N-Tier**: A multi-layered architecture where presentation, processing, and data management exist as physically separate layers.
-   **Web-based**: Applications that are accessed over a network connection.
-   **Other**: Any other type of architecture.
-   **Platform Host**: Hardware or software that hosts the business application.
-   **Platform Application**: Application that runs on a platform and can be associated to a host. In this case, the business application relies on the platform for standard operations such as development tools, execution services, and data services.

</td></tr><tr><td>

Platform host

</td><td>

A hardware or software that hosts the business application.

 This field is required if you select the **Platform Application** value in the **Architecture type** field.

</td></tr><tr><td>

Install type

</td><td>

Type of install. Use the following options:

 -   **On Premise**
-   **Cloud**
-   **Hybrid**
-   **Third Party Hosted**

</td></tr><tr><td>

Platform

</td><td>

Applications hosted by platform.

</td></tr><tr><td>

Business unit

</td><td>

Business unit that is associated with the selected business application.

</td></tr><tr><td>

Department

</td><td>

Department that is associated with the selected business application.

</td></tr><tr><td>

Installed

</td><td>

Date when the business application is installed.

</td></tr><tr><td>

Status

</td><td>

Operational status of the application. Use the following options:

-   **Implementing**
-   **In Production**
-   **Pilot**
-   **Retired**
-   **Under Evaluation**

Auditing is enabled for this field. Thus, whenever you update the value in this field, the **Activities** field on the **Activities** tab displays the update.

</td></tr><tr><td>

Life cycle stage

</td><td>

Life-cycle stage of the application. This field is auto-populated based on the value selected in the **Status** field. The data is fetched from the life-cycle mapping \[life\_cycle\_mapping\] table.

</td></tr><tr><td>

Life cycle stage status

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

Number of users that are using the applications.

 Auditing is enabled for this field. Thus, whenever you update the record in this field, the **Activities** field on the **Activities** tab displays the update.

</td></tr><tr><td>

Active user count

</td><td>

Number of active users out of the overall user base. Auditing is enabled for this field.

</td></tr><tr><td>

Last change applied date

</td><td>

Date on which the application was last updated. Auditing is enabled for this field.

</td></tr><tr><td>

Accessibility level

</td><td>

Accessibility level of the business application. Use the following options:

-   **A \(lowest\)**
-   **AA \(mid-range\)**
-   **AAA \(highest\)**

</td></tr><tr><td>

Age in months

</td><td>

Age of the business application, in months. This field is auto-populated when the date and time are entered in the **Installed** field.

</td></tr><tr><td>

Retired

</td><td>

Date when the business application is going to be retired.

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

<table id="table_qls_kvt_ncc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Planned disposition

</td><td>

Planned disposition of a business application. Use the following options:

 -   **Invest**-Business Application is targeted for additional investment. Useful especially once you bring SPM into the fold to drive decision making on demands, projects, and programs.
-   **Sustain**-Business Application is slated for continued operation, but investment is only at a level to keep it operational. No new growth plans targeted for it at this time.
-   **Migrate**-Business Application has been targeted for migration off it, based on strategic or other decisions. Users or stakeholders are migrated to a new or different application providing same or similar capabilities. Sometimes precedes Retire, but may also be used for Business Applications migrating from on-prem to cloud or vice a versa.
-   **Retire**-Business Application is due to retire. Users have either already migrated off the application, or business is divesting out of capabilities it provides, with no replacement planned.

</td></tr><tr><td>

Target date

</td><td>

Target date for the planned disposition. The target date must be the current date or a future date.

</td></tr><tr><td>

Migration Strategy

</td><td>

Migration strategy for the business application. This field appears only when **Migrate** is selected from the **Planned Disposition** field. Use the following options:-   **Rehost**-Typical lift &amp; shift – moving the application as-is to a new host.
-   **Replatform**-Also known as Drop end shop generally used for migration to cloud while abandoning classic licenses and re-purchasing cloud-based licenses.
-   **Repurchase**- Similar to lift &amp; shift, but also involves minor changes of apps to optimize use of cloud or on-premise or hybrid capabilities.
-   **Refactor**-Re-architecting the application as part of the migration process. Significant changes planned to it.

</td></tr><tr><td>

Target Business Application

</td><td>

Name of the business application for which you’re adding the planned disposition. This field appears only when **Migrate** is selected from the **Planned Disposition** field.

</td></tr><tr><td>

Reasoning

</td><td>

Reason for the planned disposition decision.

</td></tr></tbody>
</table><table id="table_arr_x5t_ncc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Portfolio manager

</td><td>

Owner of the portfolio, typically from IT. This field appears when you activate the PPM Standard plugin \(com.snc.financial\_planning\_pmo\).

</td></tr><tr><td>

Business owner

</td><td>

Person who owns the application from the business side. Every application should have an assigned business owner.

</td></tr><tr><td>

Managed by

</td><td>

User responsible for overall management of the business application, including maintenance, upgrades, and lifecycle decisions.

</td></tr><tr><td>

Managed by group

</td><td>

Group responsible for overall management of the business application, including maintenance, upgrades, and lifecycle decisions.

</td></tr><tr><td>

IT application owner

</td><td>

Person who owns the application from the IT side.

 The business application must have an owner assigned to it.

</td></tr><tr><td>

Last updated by

</td><td>

Person who last updated the application record.

</td></tr><tr><td>

Supported by

</td><td>

User responsible for providing day‑to‑day support for the business application.

</td></tr><tr><td>

Support group

</td><td>

Group responsible for providing day‑to‑day support for the business application, such as incident resolution and user assistance. For example, for a HR application where employees raise access or usability issues, the HR IT Support group is selected as the support group.

</td></tr></tbody>
</table><table id="table_e5x_z5t_ncc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Business criticality

</td><td>

Determines how critical the application is to the business. Auditing is enabled for this field.

</td></tr><tr><td>

Emergency tier

</td><td>

Actions or plans executed for the application in an emergency situation.

</td></tr><tr><td>

Data classification

</td><td>

Security level for the data in the application. This attribute determines which Governance, Risk, and Compliance \(GRC\) policies are applicable to the application. Use the following options:

 -   **Confidential**
-   **Highly Sensitive**
-   **Internal**
-   **Public**

 Auditing is enabled for the field.

</td></tr><tr><td>

Certified

</td><td>

Status of the application that meets your requirements or complies with the policies of your organization.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Work notes|Work notes entered by you.|

**Parent Topic:**[Enterprise Architecture Workspace reference](eaw-reference.md)

**Related topics**  


[Edit business application details](../../task/eaw-task/eaw-edit-business-application-details.md)

