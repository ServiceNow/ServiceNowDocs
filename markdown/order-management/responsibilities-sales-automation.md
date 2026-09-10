---
title: Related parties, responsibilities, and access included with Sales Common
description: Default related party configurations, responsibilities, and access levels included with the Sales Common app.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/responsibilities-sales-automation.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Responsibility-based access to Sales CRM entities, Sales automation apps, Configure, Sales Customer Relationship Management]
---

# Related parties, responsibilities, and access included with Sales Common

Default related party configurations, responsibilities, and access levels included with the Sales Common app.

## Default related parties and responsibilities

The following related parties and responsibilities are available with the Sales Common \(sn\_sales\_common\) app.

<table id="table_related_party_config"><thead><tr><th>

Related party configuration

</th><th>

Applies to

</th><th>

Default responsibility

</th></tr></thead><tbody><tr><td>

Account Executive

</td><td>

-   Territory \[sn\_tp\_territory\]
-   Opportunity \[sn\_opty\_mgmt\_core\_opportunity\]

</td><td>

Account Executive

</td></tr><tr><td>

Price Band Approver

</td><td>

-   Territory \[sn\_tp\_territory\]
-   Opportunity \[sn\_opty\_mgmt\_core\_opportunity\]

</td><td>

Price Band Approver

</td></tr><tr><td>

Solution Sales Executive

</td><td>

-   Territory \[sn\_tp\_territory\]
-   Opportunity \[sn\_opty\_mgmt\_core\_opportunity\]

</td><td>

Solution Sales Executive

</td></tr></tbody>
</table>The entity type for every related party configuration listed here is User \[sys\_user\].

## Responsibility Access Configuration fields

Use responsibility access configurations to define what each responsibility can access. For the list of Responsibility Access Configuration form fields, see [Configure access through the responsibility access configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/declarative-resposibility-framework.md).

## Responsibility access summary

The following table summarizes how the default responsibilities are used for responsibility-based access. Access is granted only when the user has the required role and is connected to a record through the configured relationship table.

|Responsibility|Used through relationship|Required role|Typical access intent|
|--------------|-------------------------|-------------|---------------------|
|Account Executive|Opportunity Team Member or Territory Membership Responsibility|sales restricted agent \[sn\_sales\_common.sales\_restricted\_agent\]|Grants working access to opportunities and related CRM records, such as accounts, contacts, quotes, and opportunity allocations.|
|Solution Sales Executive|Opportunity Team Member or Territory Membership Responsibility|sales restricted agent \[sn\_sales\_common.sales\_restricted\_agent\]|Grants access to opportunities and related CRM records for solution selling responsibilities.|
|Price Band Approver|Opportunity Team Member or Territory Membership Responsibility|sales restricted agent \[sn\_sales\_common.sales\_restricted\_agent\]|Grants visibility to opportunities and related records that require price band review or approval.|

**Note:** The Sales Territory Management​ plugin must be installed on your instance to configure or use Territory Membership Responsibility.

Each of the following responsibility uses the sales restricted agent \(sn\_sales\_common.sales\_restricted\_agent\) role and is active by default, through either relationship table:

-   Opportunity Team Member \[sn\_opty\_mgmt\_core\_opportunity\_team\_member\]
-   Territory Membership Responsibility \[sn\_tp\_crm\_extn\_territory\_membership\_responsibility\]

-   **Account Executive**

    The Account Executive gets the following access:

    -   Read and write access to Account and Consumer.
    -   Read, write, create, and full access to Account Address, Account Team Member, Contact, and Quote.
    Access to Opportunity and Opportunity Allocation depends on the relationship table, listed in the following table.

    |Accessible table|Via Opportunity Team Member|Via Territory Membership Responsibility|
    |----------------|---------------------------|---------------------------------------|
    |Opportunity|Read, write|Read, write, create, full|
    |Opportunity Allocation|Read|Read, write, create, full|

-   **Solution Sales Executive**

    The Solution Sales Executive gets read access to Account, Account Address, Account Team Member, Consumer, Contact, and Opportunity Allocation, and read, write, create, and full access to Quote, through either relationship table. Access to Opportunity depends on the relationship table, listed in the following table.

    |Accessible table|Via Opportunity Team Member|Via Territory Membership Responsibility|
    |----------------|---------------------------|---------------------------------------|
    |Opportunity|Read, write|Read, write, create, full|

-   **Price Band Approver**

    Price Band Approver gets read-only access to Account, Account Address, Account Team Member, Consumer, Contact, Opportunity, Opportunity Allocation, and Quote, through either relationship table.


## Custom responsibility access configurations

You can use the default configurations provided with Sales Common or create additional responsibility access configurations based on your organization's access requirements. For more information, see:

-   [Create a responsibility definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/t_CreateAResponsibilityDefinition.md)
-   [Creating a responsibility access configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/creating-responsibility-access-configuration.md)
-   [Create related party configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/adding-related-party-config-to-case.md)

