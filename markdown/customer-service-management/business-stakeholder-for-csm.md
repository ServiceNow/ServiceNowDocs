---
title: Business Stakeholder for Customer Service Management
description: Business Stakeholder for Customer Service Management includes plugins and roles that provide access to business stakeholder features.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Roles installed with Customer Service Management, Components installed with Customer Service Management, Customer Service Management reference, Customer Service Management]
---

# Business Stakeholder for Customer Service Management

Business Stakeholder for Customer Service Management includes plugins and roles that provide access to business stakeholder features.

Customers who have purchased the Customer Service Management Subscription product may provide Business Stakeholder users with the rights to the following actions:

-   Create cases on behalf of a customer or a service organization.
-   View cases, case tasks, and customer data.
-   View and drill through reports.
-   Approve requests.

## Roles for business stakeholder users

You can assign the following roles to any user who is a business stakeholder.

<table id="table_zms_lpx_znb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th><th>

Plugin

</th><th>

User type

</th></tr></thead><tbody><tr><td>

Account contributor\[sn\_customerservice.account\_contributor\]

</td><td>

This role enables users to create cases for any account.

</td><td>

sn\_customerservice.case\_contributor\_creator

</td><td>

CSM Contributor User \(com.snc.csm\_contributor\_user\)

</td><td>

Internal and external

</td></tr><tr><td>

Case authorized contributor\[sn\_customerservice.case\_authorized\_contributor\]

</td><td>

This role enables users, when added to an individual case as a related party, to: -   Add additional comments and attachments
-   Receive notifications on case updates
-   Update case tasks
-   Accept or reject a solution
-   Close a case

</td><td>

-   sn\_customerservice.case\_write\_granular
-   sn\_customerservice.case\_related\_party\_write\_granular

</td><td>

CSM Contributor User \(com.snc.csm\_contributor\_user\)

</td><td>

Internal

</td></tr><tr><td>

Consumer contributor \[sn\_customerservice.consumer\_contributor\]

</td><td>

This role enables users to create cases for any consumer.

</td><td>

sn\_customerservice.case\_contributor\_creator

</td><td>

CSM Contributor User \(com.snc.csm\_contributor\_user\)

</td><td>

Internal and external

</td></tr><tr><td>

Relationship contributor \[sn\_customerservice.relationship\_contributor\]

</td><td>

This role enables users to create cases for those customers with which they have an established relationship.

</td><td>

sn\_customerservice.case\_contributor\_creator

</td><td>

CSM Base Extension Entities \(com.snc.cs\_base\_extension\)

</td><td>

Internal and external

</td></tr><tr><td>

Location Relationship Manager \[sn\_bus\_loc.location\_relationship\_manager\]

</td><td>

This role enables users to view cases across all the external business locations where they have sn\_bus\_loc.location\_relationship\_manager responsibility.

</td><td>

sn\_customerservice.svc\_location\_manager\_contributor

</td><td>

Business Location \(com.snc.business\_location\)

</td><td>

Internal

</td></tr><tr><td>

Location Manager Contributor \[sn\_customerservice.svc\_location\_manager\_contributor\]

</td><td>

This role enables users to create, update, view, and approve cases. They can also register and remove staff across all business locations they manage. 

</td><td>

-   sn\_customerservice.consumer\_contributor
-   sn\_customerservice.svc\_location\_manager\_core
-   sn\_customerservice.service\_organization\_contributor
-   sn\_customerservice.account\_contributor

</td><td>

Business Location \(com.snc.business\_location\)

</td><td>

Internal and external

</td></tr></tbody>
</table><table id="table_gqb_rld_b4b"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Plugin

</th><th>

User type

</th></tr></thead><tbody><tr><td>

Proxy contact \[sn\_customerservice.proxy\_contact\]

</td><td>

This role enables employees to create cases for customer accounts and contacts.

</td><td>

CSM Extension for Proxy Contacts \(com.snc.csm\_proxy\_contacts\)

</td><td>

Internal

</td></tr></tbody>
</table>For more information about the proxy contact role, see [Create cases as a proxy contact](employee-create-case-for-customer.md).

<table id="table_xv4_rpx_znb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th><th>

Plugin

</th><th>

User type

</th></tr></thead><tbody><tr><td>

Service organization contributor\[sn\_customerservice.service\_organization\_contributor\]

</td><td>

This role enables users to create cases for their business location.

</td><td>

sn\_customerservice.case\_contributor\_creator

</td><td>

Business Location \(com.snc.business\_location\)

</td><td>

Internal and external

</td></tr></tbody>
</table><table id="table_cww_qz3_ktb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Plugin

</th><th>

User type

</th></tr></thead><tbody><tr><td>

Order approver\[sn\_csm\_om.order\_approver\]

</td><td>

Users with this role can view customer orders and product catalog data and can approve customer orders. They cannot create, update, or delete orders.**Note:** This requires subscription to Order Management.

</td><td>

Order Management \(com.sn\_csm\_order\_mgmt\)

</td><td>

Internal

</td></tr></tbody>
</table><table id="table_jwm_tpx_znb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Plugin

</th><th>

User type

</th></tr></thead><tbody><tr><td>

Account order viewer\[sn\_csm\_om.account\_order\_viewer\]

</td><td>

This role provides read-only access to orders, order lines, and order tasks.

</td><td>

Order Management \(com.sn\_csm\_order\_mgmt\)

</td><td>

Internal

</td></tr><tr><td>

Business location viewer\[sn\_bus\_loc.viewer\]

</td><td>

This role provides read-only access to business locations.**Note:** This role provides unrestricted access to view all business locations regardless of other access controls.

</td><td>

Business Location \(com.snc.business\_location\)

</td><td>

Internal

</td></tr><tr><td>

Case viewer\[sn\_customerservice.case\_viewer\]

</td><td>

This role provides read-only access to all cases.

</td><td>

 

</td><td>

Internal

</td></tr><tr><td>

Case task viewer \[sn\_customerservice.case\_task\_viewer\]

</td><td>

This role provides read-only access to all case tasks. **Note:** When combined with the case viewer role \(sn\_customerservice.case\_viewer\), a user can access all customer service cases and all case tasks.

</td><td>

 

</td><td>

Internal

</td></tr><tr><td>

Consumer order viewer\[sn\_csm\_om.consumer\_order\_viewer\]

</td><td>

This role provides read-only access to orders, order lines, and order tasks.

</td><td>

Order Management \(com.sn\_csm\_order\_mgmt\)

</td><td>

Internal

</td></tr><tr><td>

Customer data viewer\[sn\_customerservice.customer\_data\_viewer\]

</td><td>

This role provides read access to customer data, including account, consumer, and household data, and the information included in the related lists.

</td><td>

 

</td><td>

Internal

</td></tr><tr><td>

Household viewer\[sn\_csm\_household.viewer\]

</td><td>

This role provides read-only access to all households.**Note:** This role provides unrestricted access to view all households regardless of relationship or other access controls.

</td><td>

Customer Service Household \(com.snc.household\)

</td><td>

Internal

</td></tr><tr><td>

Service organization viewer\[sn\_service\_org.viewer\]

</td><td>

This role provides read-only access to service organizations.**Note:** This role provides unrestricted access to view all service organizations regardless of other access controls.

</td><td>

Service Organization \(com.snc.service\_organization\)

</td><td>

Internal

</td></tr></tbody>
</table><table id="table_e3y_5px_znb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

User type

</th></tr></thead><tbody><tr><td>

Performance Analytics viewer\[pa\_viewer\]

</td><td>

This role can:-   View Analytics Hub.
-   Create thresholds and targets for indicators.
-   Read, update, and delete the thresholds and targets that are created.
-   View text analytics widgets on dashboards.

</td><td>

Internal

</td></tr></tbody>
</table><table id="table_ktt_xxq_q5b"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th><th>

User type

</th></tr></thead><tbody><tr><td>

Project Stakeholder \[sn\_customerservice.projectstakeholder\]

</td><td>

This role can:-   View all projects.
-   View project information.
-   View project task information.

</td><td>

sn\_customerservice.projectstakeholder

</td><td>

Internal

</td></tr></tbody>
</table>**Parent Topic:**[Roles installed with Customer Service Management](../reference/r_RolesInstalledWithCustomerService.md)

**Related topics**  


[Business stakeholder role for PPM](https://www.servicenow.com/docs/access?context=business-stakeholder-role-ppm&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)

[Business stakeholder role for APM](https://www.servicenow.com/docs/access?context=business-stakeholder-role-apm&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US)

[Installed with Business Stakeholder](https://www.servicenow.com/docs/access?context=installed-with-business-stakeholder&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)

