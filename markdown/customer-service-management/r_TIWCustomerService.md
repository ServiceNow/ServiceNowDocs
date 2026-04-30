---
title: Tables installed with Customer Service Management
description: Tables are added to your instance with the activation of the Customer Service Management \(CSM\) application.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Components installed with Customer Service Management, Reference, Customer Service Management]
---

# Tables installed with Customer Service Management

Tables are added to your instance with the activation of the Customer Service Management \(CSM\) application.

## Tables added with the activation of the Customer Service Base Entities plugin

The following tables are added with the activation of the Customer Service Base Entities plugin. This plugin is activated automatically by the Customer Service plugin.

<table id="table_csm_base_entities"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account\[customer\_account\]

</td><td>

Stores the customer account and partner records.

</td></tr><tr><td>

Account Address\[account\_address\_relationship\]

</td><td>

Stores the associations between the locations \(addresses\) and accounts.

</td></tr><tr><td>

Account Access\[sn\_csm\_account\_access\]

</td><td>

Stores the records that restrict the contact access to CSM entities.

</td></tr><tr><td>

Account Relationship\[account\_relationship\]

</td><td>

Stores the records for the relationships that have been created between the two accounts.

</td></tr><tr><td>

Address Type\[cmn\_location\_type\]

</td><td>

Stores the address types for the CSM entities, such as Billing or Shipping. Address types are typically used with order cases.

</td></tr><tr><td>

Consumer\[csm\_consumer\]

</td><td>

Stores the consumer records.

</td></tr><tr><td>

Consumer User\[csm\_consumer\_user\]

</td><td>

Stores the consumer registration records that are created when the consumers complete the self-registration process from the Consumer Service Portal. This table extends the Users table \(sys\_user\).

</td></tr><tr><td>

Contact\[customer\_contact\]

</td><td>

Stores the customer contact records.

</td></tr><tr><td>

Contract Contact\[contract\_rel\_contact\]

</td><td>

Stores the relationships that are created between the contacts and contracts.

</td></tr><tr><td>

Household\[csm\_household\]

</td><td>

Stores the consumer household records.

</td></tr><tr><td>

Entitlement \[service\_entitlement\]

</td><td>

Stores the entitlement records.

</td></tr><tr><td>

Consumer Profile\[sn\_csm\_consumer\_profile\]

</td><td>

Stores the references to the consumer and can be expanded to support multiple profiles within and across industries, with each profile having its own set of attributes in the extended table.

</td></tr><tr><td>

Consumer Profile Location\[sn\_csm\_consumer\_profile\_location\]

</td><td>

Stores the relationships between the consumer profiles and locations \(addresses\).

</td></tr></tbody>
</table>## Tables added with the activation of Customer Service plugin

The following tables are added with the activation of the Customer Service plugin.

<table id="table_csm_main_plugin"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account Relationship Access\[sn\_customerservice\_account\_relationship\_access\]

</td><td>

Stores the type of access for the account relationships.

</td></tr><tr><td>

Account Relationship Type\[sn\_customerservice\_account\_relationship\_type\]

</td><td>

Stores the relationship types that are created for the bi-directional account relationships.

</td></tr><tr><td>

Account Team Member\[sn\_customerservice\_team\_member\]

</td><td>

Stores the team members that are assigned to the account teams.

</td></tr><tr><td>

Agent Token\[sn\_customerservice\_agent\_token\]

</td><td>

This table isn’t currently used.

</td></tr><tr><td>

Appointment\[sn\_customerservice\_appointment\]

</td><td>

Stores the appointments that have been created for the customer service cases.

</td></tr><tr><td>

Asset Contact\[sn\_customerservice\_m2m\_asset\_contact\]

</td><td>

Stores the asset contact relationship records.

</td></tr><tr><td>

Case\[sn\_customerservice\_case\]

</td><td>

Stores the customer service case records.

</td></tr><tr><td>

Case Entitlement\[sn\_customerservice\_case\_entitlement\]

</td><td>

Stores the entitlements associated with case records.Associated entitlements are available in the Entitlements related list on the case record. The [sn\_customerservice.advanced\_entitlements](r_PropInstallWcustServ.md#advanced-entitlements) system property controls the display of this related list.

</td></tr><tr><td>

Case Report\[sn\_customerservice\_case\_report\]

</td><td>

Stores the key performance indicators \(KPIs\) and metrics for the case records.

</td></tr><tr><td>

Channel Configurations\[sn\_customerservice\_channel\_config\]

</td><td>

Stores the customer service email channel configuration records.

</td></tr><tr><td>

Contact Relationship\[sn\_customerservice\_contact\_relationship\]

</td><td>

Stores the contact relationship records.

</td></tr><tr><td>

Customer Interaction\[sn\_customerservice\_customer\_interaction\]

</td><td>

Stores the interaction records for Customer Service Management \(CSM\).

</td></tr><tr><td>

Customer Service Case Flow\[sn\_customerservice\_sf\_case\]

</td><td>

Stores the customer service case state flows.

</td></tr><tr><td>

Escalation\[sn\_customerservice\_escalation\]

</td><td>

Stores the records created for escalated cases and accounts.

</td></tr><tr><td>

Escalation Severity\[sn\_customerservice\_escalation\_severity\]

</td><td>

Stores the escalation severity definition records.

</td></tr><tr><td>

Escalation Template\[sn\_customerservice\_escalation\_template\]

</td><td>

Stores the escalation template records.

</td></tr><tr><td>

Registration Request\[sn\_customerservice\_registration\]

</td><td>

Stores the self-registration requests for the Customer Service Portal.

</td></tr><tr><td>

Related Party\[sn\_customerservice\_related\_party\]

</td><td>

Stores the entities \(such as account, contact, or consumer\) that are related to the customer service cases and the responsibilities assigned to each of the entities.

</td></tr><tr><td>

Related Party Configuration\[sn\_customerservice\_related\_party\_configuration\]

</td><td>

Stores the related party type that provides a default responsibility definition.

</td></tr><tr><td>

Responsibility Definition\[sn\_customerservice\_responsibility\_def\]

</td><td>

Stores the responsibility definitions that are created to support the customer accounts.

</td></tr><tr><td>

Task\[sn\_customerservice\_task\]

</td><td>

Stores the tasks that have been created for the customer service cases.

</td></tr><tr><td>

Responsibility Access Configuration\[sn\_customerservice\_responsibility\_access\_config\]

</td><td>

Stores the metadata of the responsibility access configuration, which specifies the level of access and the entities that can be accessed by a particular responsibility.

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with Customer Service Management](r_InstalledWithCustomerService.md)

