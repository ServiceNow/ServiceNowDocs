---
title: Roles installed with billing accounts
description: The Billing Account Core application installs granular roles across three families: platform, CRM, and customer access management. Users inherit these granular roles through the functional or persona roles assigned to them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/roles-installed-with-billing-accounts.html
release: zurich
topic_type: reference
last_updated: "2026-09-11"
reading_time_minutes: 3
breadcrumb: [Configuring billing accounts, Billing accounts, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Roles installed with billing accounts

The Billing Account Core application installs granular roles across three families: platform, CRM, and customer access management. Users inherit these granular roles through the functional or persona roles assigned to them.

## How billing account roles are used

The platform and CRM billing account roles are granular roles that act as the role condition on the application's ACLs. You don't assign these granular roles to a user directly. Instead, a functional or persona role that is enabled for the responsibility framework contains the granular roles, and users inherit them. On its own, a platform or CRM granular role has no effect.

The customer access management roles work differently. The `sn_billing_account.authorized_contact` and `sn_billing_account.authorized_consumer` roles are the roles that the responsibility access configuration \(RAC\) records for billing accounts require, so the related party's user must hold one of them. You can assign the role to the user directly, or include it in a persona role such as Consumer \(`sn_customerservice.consumer`\) so that all consumers hold it.

Holding the role doesn't grant access on its own. The user gets access only where a related party record on the billing account gives them a responsibility whose RAC records require that role. For more information, see [Add related parties to a billing account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/add-related-parties-to-a-billing-account.md).

## Platform granular roles

Platform granular roles provide access to the base billing account data.

|Role|Role name|
|----|---------|
|Billing Account Viewer|sn\_billing\_account.viewer|
|Billing Account Writer|sn\_billing\_account.writer|
|Billing Account Data Manager|sn\_billing\_account.data\_manager|
|Billing Account Administrator|sn\_billing\_account.admin|
|Billing Account API Integration|sn\_billing\_account.ws\_integration|
|Billing Account Schedule Viewer|sn\_billing\_account.schedule\_viewer|
|Billing Account Schedule Writer|sn\_billing\_account.schedule\_writer|

## CRM granular roles

CRM granular roles provide access to CRM billing account data and are inherited by CRM persona roles.

|Role|Role name|
|----|---------|
|CRM Billing Account B2B Viewer|sn\_billing\_account.crm\_b2b\_viewer|
|CRM Billing Account B2C Viewer|sn\_billing\_account.crm\_b2c\_viewer|
|CRM Billing Account B2B Writer|sn\_billing\_account.crm\_b2b\_writer|
|CRM Billing Account B2C Writer|sn\_billing\_account.crm\_b2c\_writer|
|CRM Billing Account Data Manager|sn\_billing\_account.crm\_data\_manager|
|CRM Billing Account Administrator|sn\_billing\_account.crm\_admin|

## Customer access management granular roles

Customer access management roles grant related parties access to billing accounts through the responsibility framework. Each authorized role contains the granular roles that provide access to the billing account, case, and customer data entities.

<table id="table_ba_cam_roles"><thead><tr><th>

Role

</th><th>

Role name

</th><th>

Contain roles

</th></tr></thead><tbody><tr><td>

Billing Responsibility Granular

</td><td>

sn\_billing\_account.resp\_granular

</td><td>

 

</td></tr><tr><td>

Billing Authorized Contact

</td><td>

sn\_billing\_account.authorized\_contact

</td><td>

-   sn\_billing\_account.resp\_granular
-   sn\_customerservice.case\_mgmt\_resp\_granular
-   sn\_customerservice.cust\_data\_resp\_granular

</td></tr><tr><td>

Billing Authorized Consumer

</td><td>

sn\_billing\_account.authorized\_consumer

</td><td>

-   sn\_billing\_account.resp\_granular
-   sn\_customerservice.case\_mgmt\_resp\_granular
-   sn\_customerservice.cust\_data\_resp\_granular

</td></tr></tbody>
</table>**Related topics**  


[Granular roles and supported entities for responsibility framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/granular-roles-and-supported-entities-CAM.md)

[Billing accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/configuring-billing-accounts.md)

[Add related parties to a billing account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/add-related-parties-to-a-billing-account.md)

[Create a responsibility definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/t_CreateAResponsibilityDefinition.md)

[Creating a responsibility access configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/creating-responsibility-access-configuration.md)

[Grant write access to a billing account related party](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/grant-write-access-to-ba-related-party.md)

