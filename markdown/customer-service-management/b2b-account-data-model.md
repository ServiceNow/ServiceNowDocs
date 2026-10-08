---
title: B2B - Account data model
description: Reference the tables and relationships that store business-to-business \(B2B\) customer accounts, contacts, account hierarchies, account relationships, and account teams.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/b2b-account-data-model.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Customer Data Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# B2B - Account data model

Reference the tables and relationships that store business-to-business \(B2B\) customer accounts, contacts, account hierarchies, account relationships, and account teams.

## Overview of account data model

The B2B account data model captures the structures used when the customer is another business. It defines the account and contact entities that represent the customer organization and its individuals. It also defines the relationships, addresses, and team memberships that describe how the customer is served. The model extends platform foundations sys\_user, core\_company, cmn\_location, and CSM tables. Industry solutions build on it for B2B scenarios, such as insurance carriers modeling brokers, financial services modeling institutional clients, and healthcare payers modeling provider organizations.

## B2B - Account data model diagram

\[Omitted image "refarch-b2b-account-data-model.png"\] Alt text: Architecture diagram displaying the account data model and its related tables.

In the B2B account data model diagram, the accounts and contacts \(with partner variants\) are mapped to a user. These are connected to account relationship, contact relationship, account team member, and account address. The responsibility and responsibility access configuration entities govern these access. Each entity refers to a shared reference and transaction data.

## Tables in the B2B account data model

<table id="table_k1p_cvx_zjc"><thead><tr><th>

Label

</th><th>

Table name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account

</td><td>

customer\_account

</td><td>

B2B customer or partner organization. Extends `core_company`. One table stores both customer and partner accounts, distinguished by the **Account type** field.

</td></tr><tr><td>

Contact

</td><td>

customer\_contact

</td><td>

Individual at a B2B account. Extends `sys_user`. Both contact and partner contact use this table. **Note:** Starting with the Brazil release, a new field **External ID** is added to the contact table that acts as an identifier for this contact in an external system.

</td></tr><tr><td>

Account relationship

</td><td>

 

</td><td>

Bi-directional link between two accounts, such as partner-customer or supplier-buyer. References account relationship type.

</td></tr><tr><td>

Account relationship type

</td><td>

 

</td><td>

Named relationship type, such as a partner.

</td></tr><tr><td>

Contact relationship

</td><td>

sn\_customerservice\_contact\_relationship

</td><td>

Bi-directional link between two contacts, such as co-signers, authorized representatives, or buying-group members.

</td></tr><tr><td>

Account team member

</td><td>

sn\_customerservice\_team\_member

</td><td>

Internal employee assigned to an account in a named role. Roles use responsibility entities from customer relationships and access management.

</td></tr></tbody>
</table>**Related topics**  


[Configure accounts and contacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configure-csm-accounts-contacts.md)

[Create customer relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/c_CustomerServiceRelationships.md)

[Account hierarchy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/c_AccountHierarchy.md)

[Bi-directional account relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/c_AccountRelationships.md)

[Contact relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/c_ContactRelationships.md)

[Creating an account team member](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configure-csm-account-teams.md)

