---
title: Responsibility-based access to Sales CRM entities
description: Responsibility-based access grants Sales CRM users access to records based on the responsibility they hold for an opportunity, account, or sales territory. Instead of giving users broad access to every lead, opportunity, account, contact, quote, or CRM Touchpoints, the responsibility framework scopes access to records connected to the user's opportunity team or sales territory membership.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/responsibility-based-access-crm-touchpoints.html
release: australia
topic_type: concept
last_updated: "2026-08-14"
reading_time_minutes: 6
breadcrumb: [Sales automation apps, Configure, Sales Customer Relationship Management]
---

# Responsibility-based access to Sales CRM entities

Responsibility-based access grants Sales CRM users access to records based on the responsibility they hold for an opportunity, account, or sales territory. Instead of giving users broad access to every lead, opportunity, account, contact, quote, or CRM Touchpoints, the responsibility framework scopes access to records connected to the user's opportunity team or sales territory membership.

## How users get access to Sales CRM records

Sales CRM supports the following access patterns:

-   Blanket access: Users with broad roles, such as the lead writer \[sn\_lead\_mgmt\_core.lead\_writer\] or CRM touchpoint writer \[sn\_crm\_touchpoint.touchpoint\_writer\] role, can view or work with every record of that type, regardless of the opportunity, account, or sales territory that the record is associated with. Use this access pattern for users who need broad visibility across sales records.
-   Responsibility-based access: Users get access based on the responsibility they hold in a sales territory or on an opportunity team. For example, users can be added as Account Executives, Solution Sales Executives, or Price Band Approvers. The responsibility framework uses those memberships to grant access only to the records that are connected to the user's responsibility. Multiple users can hold different responsibilities within the same territory. Different users can join an opportunity team, such as an overlay sales representative or a Solution Sales Executive from outside the opportunity's territory.

Users with the sales restricted agent \[sn\_sales\_common.sales\_restricted\_agent\] role can see and manage only the CRM records that are connected to what they are responsible for.

## How responsibility-based access works

Responsibility-based access uses multiple configuration layers to determine whether a user can access a record.

<table id="table_jzr_fzr_fkc"><thead><tr><th>

Configuration element

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Related party configuration

</td><td>

Defines the business relationship that a user can have with a CRM record.

</td><td>

Account Executive, Solution Sales Executive, Price Band Approver

</td></tr><tr><td>

Relationship table

</td><td>

Stores the record that connects the user to an opportunity or sales territory.

</td><td>

-   Opportunity Team Member \[sn\_opty\_mgmt\_core\_opportunity\_team\_member\] table
-   Territory Membership Responsibility \[sn\_tp\_crm\_extn\_territory\_membership\_responsibility\] table

</td></tr><tr><td>

Responsibility definition

</td><td>

Defines the responsibility assigned to the user through the relationship.

</td><td>

Account Executive

</td></tr><tr><td>

Responsibility access configuration

</td><td>

Defines which tables the responsibility can access, the access level for each table, the required role, and the relationship path.

</td><td>

Account Executive can read and write Opportunity records

</td></tr><tr><td>

Required role

</td><td>

Confirms that the user has the necessary role required for the configuration to apply.

</td><td>

Sales restricted agent \[sn\_sales\_common.sales\_restricted\_agent\] role

</td></tr></tbody>
</table>When these conditions match, the user receives the configured access to records in the accessible table.

## Relationship between related party and responsibility

A related party describes the user's business relationship to a record. A responsibility determines what access the user can receive because of that relationship.

For example, when a user is added to an opportunity as an Account Executive, the record on the Opportunity Team Member \[sn\_opty\_mgmt\_core\_opportunity\_team\_member\] table connects the user to the opportunity. The Account Executive responsibility then determines which related CRM records the user can access, such as the opportunity, account, contact, quote, or CRM Touchpoints records.

The responsibility name alone does not grant access. Access is granted only when a responsibility access configuration maps the responsibility to an accessible table, access level, required role, and relationship table.

\[Omitted image "related-access-configuration-sales-crm.png"\] Alt text: The default related party configurations available with the Sales Common application.

## Example: Account Executive access

The Account Executive responsibility can have multiple responsibility access configuration records. Each configuration grants access to one accessible table through a specific relationship table.

\[Omitted image "sales-crm-responsibility-access-config.png"\] Alt text: Responsibility definition for Account Executive role showing list of responsibility access configuration.

For example, if a user is connected to an opportunity through the Opportunity Team Member \[sn\_opty\_mgmt\_core\_opportunity\_team\_member\] table and has the Account Executive responsibility, the responsibility access configuration can grant the user read and write access to the Opportunity tables. Other configuration rows can grant access to related tables, such as Account, Contact, Quote, Account Address, Consumer, and Opportunity Allocation.

Access levels apply to records in the accessible table, not to the responsibility or relationship table. For example, if the accessible table is Leads and the access levels are Read, Write, and Create, users with the matching responsibility and required role can read, update, and create quote records that are reachable through the configured relationship.

## Relationship tables

The relationship table identifies where the user's responsibility is recorded. In Sales CRM, responsibility-based access typically uses one of these relationship paths:

|Relationship path|When it applies|
|-----------------|---------------|
|Opportunity Team Member \[sn\_opty\_mgmt\_core\_opportunity\_team\_member\]|Grants access based on a user's responsibility on an opportunity team.|
|Territory Membership Responsibility \[sn\_tp\_crm\_extn\_territory\_membership\_responsibility\]|Grants access based on a user's responsibility in a sales territory.|

For example, opportunity-based access uses the Opportunity Team Member relationship path to determine whether a user is connected to the opportunity. Territory-based access uses the Sales Territory Member relationship path to determine whether a user is connected to the territory.

## Accessible tables

The accessible table is the table on which access is being granted. A single responsibility can have multiple responsibility access configuration records, each for a different accessible table. For example, the Account Executive responsibility can grant different levels of access to these accessible tables:

-   Opportunity
-   Account
-   Account Team Member
-   Account Address
-   Contact
-   Consumer
-   Quote
-   Opportunity Allocation
-   CRM Touchpoints

Each accessible table can have its own access level and optional filter. This lets administrators grant broader access to some records and more limited access to others.

## CRM Touchpoints access through the responsibility framework

The sales restricted agent \[sn\_sales\_common.sales\_restricted\_agent\] role inherits the lead and opportunity responsibility granular roles by default. Therefore, the responsibility framework can evaluate access to lead and opportunity records. Other CRM entities need their own granular roles added before the framework can evaluate access to them. For example, on CRM Touchpoints, the following granular roles make CRM Touchpoints available to the framework:

-   CRM touchpoint responsibility read granular \[sn\_crm\_touchpoint.touchpoint\_responsibility\_read\_granular\]: Provides read access to CRM Touchpoints through the responsibility framework.
-   CRM touchpoint responsibility write granular \[sn\_crm\_touchpoint.touchpoint\_responsibility\_write\_granular\]: Provides write access to CRM Touchpoints through the responsibility framework. This role includes the read granular role.

To extend CRM Touchpoints access to a responsibility definition, such as Account Executive or Solution Sales Executive, an administrator updates or creates a responsibility access configuration for that responsibility. The administrator selects CRM Touchpoints \[sn\_crm\_touchpoint\_touchpoint\] as the accessible table, selects the access levels, and optionally adds an accessible table filter to limit access by type, state, or another condition. For more information, see [Create a responsibility access configuration in Sales CRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-responsibility-access-configuration-sales-automation.md).

For example, an administrator can configure the Solution Sales Executive responsibility so that users can edit only CRM Touchpoints of type Solution review while other CRM Touchpoints types remain read-only.

**Note:** Administrators who assign persona roles such as Solution Sales Executive or Account Executive must also ensure that sales restricted agent \[sn\_sales\_common.sales\_restricted\_agent\] role includes the CRM touchpoint responsibility write granular \[sn\_crm\_touchpoint.touchpoint\_responsibility\_write\_granular\] role for the intended access.

**Related topics**  


[Components installed with Sales Common](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/components-installed-sales-common.md)

[Components installed with CRM Touchpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/components-installed-crm-touchpoints.md)

[Related parties, responsibilities, and access included with Sales Common](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/responsibilities-sales-automation.md)

