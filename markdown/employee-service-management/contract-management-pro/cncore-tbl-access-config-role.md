---
title: Provide permissions to configure default contract document information
description: As an administrator, enable a contract user to configure information placed in the contract document by assigning a contract configurator role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/contract-management-pro/cncore-tbl-access-config-role.html
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure contract request functionality, Configuring Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Provide permissions to configure default contract document information

As an administrator, enable a contract user to configure information placed in the contract document by assigning a contract configurator role.

## Before you begin

Role required: admin

## About this task

Template mappings automatically insert default values in the contract document. To configure template mappings, the contract user requires a contracts configurator \(sn\_cm\_core.contract\_config\) role. For more information on how to configure template mappings, see [Update contract template mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/cncore-template-mapping.md).

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  Search for and select the user.

3.  In the Roles related list, select **Edit**.

4.  Move the sn\_cm\_core.contract\_config role from the Available list to the Selected list.

5.  Select **Save**.

6.  Save the user record by selecting **Update**.


**Parent Topic:**[Add and configure contract request functionality into your workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/cncore-uptake-steps.md)

**Related topics**  


[Configure non-task tables for contract templates]()

[Add a workspace action button for initiating a contract request]()

[Add Contract requests tab to your workspace]()

[Add amendment tabs to contract repository record]()

[Display contract documents in a contract repository record]()

[Copy fields from parent request to contract request]()

[Group contract documents by contract type in the contract request form]()

[Add access to obligation management from contract repository records]()

[Configure the contract request form header for your workspace]()

[Provide access to contract request fields in condition builders]()

