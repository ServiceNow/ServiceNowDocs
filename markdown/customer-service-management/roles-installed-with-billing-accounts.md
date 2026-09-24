---
title: Roles installed with billing accounts
description: The Billing Account Core application installs granular roles across three families: platform, CRM, and customer access management. Users inherit these granular roles through the functional or persona roles assigned to them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/roles-installed-with-billing-accounts.html
release: brazil
topic_type: reference
last_updated: "2026-09-11"
reading_time_minutes: 2
breadcrumb: [Configuring billing accounts, Billing accounts, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Roles installed with billing accounts

The Billing Account Core application installs granular roles across three families: platform, CRM, and customer access management. Users inherit these granular roles through the functional or persona roles assigned to them.

## How billing account roles are used

The billing account roles are granular roles that act as the role condition on the application's ACLs. You don't assign a granular role to a user directly. Instead, a functional or persona role that is enabled for the responsibility framework contains the granular roles, and users inherit them. On its own, a granular role has no effect. The customer access management roles additionally drive related-party access through the declarative responsibility framework.

## Platform granular roles

Platform granular roles provide access to the base billing account data.

|Role|Role name|
|----|---------|
|Billing Account Viewer|`sn_billing_account.viewer`|
|Billing Account Writer|`sn_billing_account.writer`|
|Billing Account Data Manager|`sn_billing_account.data_manager`|
|Billing Account Administrator|`sn_billing_account.admin`|
|Billing Account API Integration|`sn_billing_account.ws_integration`|
|Billing Account Schedule Viewer|`sn_billing_account.schedule_viewer`|
|Billing Account Schedule Writer|`sn_billing_account.schedule_writer`|

## CRM granular roles

CRM granular roles provide access to CRM billing account data and are inherited by CRM persona roles.

|Role|Role name|
|----|---------|
|CRM Billing Account B2B Viewer|`sn_billing_account.crm_b2b_viewer`|
|CRM Billing Account B2C Viewer|`sn_billing_account.crm_b2c_viewer`|
|CRM Billing Account B2B Writer|`sn_billing_account.crm_b2b_writer`|
|CRM Billing Account B2C Writer|`sn_billing_account.crm_b2c_writer`|
|CRM Billing Account Data Manager|`sn_billing_account.crm_data_manager`|
|CRM Billing Account Administrator|`sn_billing_account.crm_admin`|

## Customer access management granular roles

Customer access management granular roles grant related parties access to billing accounts through the responsibility framework.

|Role|Role name|
|----|---------|
|Billing Responsibility Granular|`sn_billing_account.resp_granular`|
|Billing Authorized Contact|`sn_billing_account.authorized_contact`|
|Billing Authorized Consumer|`sn_billing_account.authorized_consumer`|

**Related topics**  


[Granular roles and entities for responsibility framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/granular-roles-and-supported-entities-CAM.md)

[Billing accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configuring-billing-accounts.md)

[Add related parties to a billing account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/add-related-parties-to-a-billing-account.md)

[Create a responsibility definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/t_CreateAResponsibilityDefinition.md)

[Creating a responsibility access configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/creating-responsibility-access-configuration.md)

