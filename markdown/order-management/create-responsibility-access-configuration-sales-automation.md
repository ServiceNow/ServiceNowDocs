---
title: Create a responsibility access configuration in Sales CRM
description: Grant a responsibility definition table-level access to leads, opportunities, and related entities by creating or updating a responsibility access configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/create-responsibility-access-configuration-sales-automation.html
release: australia
topic_type: task
last_updated: "2026-08-14"
reading_time_minutes: 4
breadcrumb: [Responsibility-based access to Sales CRM entities, Sales automation apps, Configure, Sales Customer Relationship Management]
---

# Create a responsibility access configuration in Sales CRM

Grant a responsibility definition table-level access to leads, opportunities, and related entities by creating or updating a responsibility access configuration.

## Before you begin

The responsibility definition that you want to grant access for already exists. This task configures access for an existing responsibility definition. It does not create one. For the responsibility definitions provided with Sales Common, see [Related parties, responsibilities, and access included with Sales Common](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/responsibilities-sales-automation.md).

Role required: admin

## About this task

A responsibility access configuration determines which records a responsibility can access. Each configuration maps a responsibility to an accessible table, access level, required role, and relationship table.

For example, you can configure the Account Executive responsibility so that users connected through the Opportunity Team Member \[sn\_opty\_mgmt\_core\_opportunity\_team\_member\] table can read and write Opportunity records and work with related Quote records. For more information about how the responsibility framework uses these records to grant access to leads, opportunities, accounts, contacts, or CRM Touchpoints, see [Responsibility-based access to Sales CRM entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/responsibility-based-access-crm-touchpoints.md).

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Responsibility Definitions**.

2.  Select the responsibility definition that you want to configure access for.

    Solution Sales Executive

3.  Set the application scope to the application containing the accessible table.

    For example, if you want to add a responsibility definition on any of the CRM Touchpoints tables, set the application scope to CRM Touchpoints.

    You can change the application scope using the application picker \[Omitted image "globe-outline-24.svg"\] Alt text: in the Unified Navigation bar.

    **Note:** The Sales Common application scope must be set only for the following entities: Account, Consumer, and Contact.

4.  In the Responsibility Access Configurations related list, select an existing record to update it, or select **New** to create one.

    A responsibility definition can have multiple responsibility access configuration records. Each record grants access to one accessible table through one relationship path. For example, the Account Executive responsibility can have one configuration for Opportunity access, another for Quote access, and another for Account access.

5.  In the **Responsibility** field, confirm or select the responsibility definition that this configuration applies to.

6.  Define what this configuration grants access to, and who can use it.

    1.  In the **Roles required** field, add the roles that a user must have for this configuration to apply.

        **sn\_sales\_common.sales\_restricted\_agent**

    2.  Select the **Active** check box so the configuration takes effect.

    3.  On the Grant access to tab, in the **Access levels** field, select the level of access to grant.

        The available options are:

        -   Read
        -   Write
        -   Create
        -   Full
        You can select more than one access level, such as Read and Write, depending on what the responsibility requires.

    4.  In the **Accessible table** field, select the table that this access level applies to.

        -   Opportunity
        -   Account
        -   Consumer
        -   Quote
        **Note:** Access levels apply to records in the accessible table. For example, if the accessible table is Quote and the selected access levels are Read, Write, and Create, matching users can read, update, and create quote records that are reachable through the configured relationship.

7.  In the **Accessible table filter** field, define the records within the accessible table that the configuration grants access to.

    This filter narrows the records within the accessible table that the access grant applies to.

    1.  Select **Add Filter Condition** and use the field picker to choose the field to filter on.

        Leave the filter empty only when the responsibility should apply to all reachable records in the accessible table. Add a filter when access should be limited to records that match specific conditions, such as type or state.

    2.  Add more filter conditions by selecting **Add OR Clause**.

8.  On the Through relationship tab, define the relationship where the selected responsibility will be used to grant access.

    -   Opportunity Team Member \[sn\_opty\_mgmt\_core\_opportunity\_team\_member\]
    -   Territory Membership Responsibility \[sn\_tp\_crm\_extn\_territory\_membership\_responsibility\]
9.  On the Using relationship association tab, define the association between the accessible and relationship tables.

    For more information, see [Creating a responsibility access configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/creating-responsibility-access-configuration.md).

10. Select **Submit**.


## Result

Users who have the required roles and are connected to a record through the responsibility's relationship table now have the access levels that this configuration grants to the accessible table.

**Note:** If existing access does not reflect your changes right away, use the Clear cached configurations or Run Point Scan related links on the responsibility access configuration record to refresh access.

**Related topics**  


[Components installed with Sales Territory Management​](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/components-installed-sales-territory-management.md)

[Components installed with Opportunity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/components-installed-opportunity-management.md)

[Components installed with CRM Touchpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/components-installed-crm-touchpoints.md)

[Components installed with Sales Common](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/components-installed-sales-common.md)

