---
title: Add related parties to a billing account
description: Extend billing account access to additional customers or stakeholders by configuring billing account related parties. Related parties enable you to define relationships between billing accounts and other entities such as contacts, consumers, or accounts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/add-related-parties-to-a-billing-account.html
release: zurich
topic_type: task
last_updated: "2026-09-22"
reading_time_minutes: 5
breadcrumb: [Configuring billing accounts, Billing accounts, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Add related parties to a billing account

Extend billing account access to additional customers or stakeholders by configuring billing account related parties. Related parties enable you to define relationships between billing accounts and other entities such as contacts, consumers, or accounts.

## Before you begin

Confirm that the following prerequisites are in place:

-   A billing account record exists
-   The contact, consumer, or account record you want to add as a related party exists

Role required: sn\_billing\_account.crm\_b2b\_writer or sn\_billing\_account.crm\_b2c\_writer, or a role that contains them \(sn\_billing\_account.crm\_data\_manager or sn\_billing\_account.crm\_admin\). The unrestricted billing account roles \(sn\_billing\_account.writer, sn\_billing\_account.data\_manager, sn\_billing\_account.admin\) also apply.

## About this task

Billing account related parties use the customer access management \(CAM\) responsibility framework to extend record-level access to a billing account. On a related party record, the type and the responsibility do different jobs:

-   **Type** is a label that describes the business relationship, such as authorized contact or listed consumer. The type doesn't grant access.
-   **Responsibility** determines the access. The responsibility on the related party record is matched against the responsibility access configuration \(RAC\) records for that responsibility. Those records define the accessible tables, the access levels, and the required role.

Access requires all three of the following. If any one of them is missing, the related party has no access to the billing account.

-   A related party record that links the account, contact, or consumer to the billing account and specifies a responsibility.
-   Active RAC records for that responsibility that point to the billing account tables.
-   The role that those RAC records require, held by the related party's user.

A related party with a listed type, or with an empty **Responsibility** field, is recorded on the billing account for reference only, without access.

The responsibilities provided with the base system — Billing Authorized Account, Billing Authorized Contact, and Billing Authorized Consumer — grant read access to the following tables:

-   Billing Account
-   Billing Account Address
-   Billing Account Payment Profile
-   Schedule
-   Schedule Entry
-   Location

To grant write or create access through the related party path, create additional RAC records. For more information, see [Creating a responsibility access configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/creating-responsibility-access-configuration.md).

For how the responsibility framework, granular roles, and query rules work together, see [Granular roles and supported entities for customer access management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/granular-roles-and-supported-entities-CAM.md).

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** &gt; **Billing Accounts**.

2.  Select a billing account from the list.

    For more information on how to create billing account record, see [Install billing account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/install-billing-account.md).

3.  Select **New** from the Billing Account Related Party related list.

4.  On the form, fill in the fields.

<table id="table_fyv_dtr_bs"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Label that describes the business relationship of the related party, such as authorized account, authorized contact, authorized consumer, or a custom type that you create. **Note:** The type doesn't grant access. When you select an authorized type, the Responsibility field is populated with the default responsibility for that type, and the responsibility grants the access.

For the types and default responsibilities provided with the base system, see [List of responsibilities provided with the base system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/list-of-reponsibilities-provided-with-base-system.md).

</td></tr><tr><td>

Billing account

</td><td>

Billing account to which this related party belongs.

</td></tr><tr><td>

Account

</td><td>

Customer account associated with the billing account.

</td></tr><tr><td>

Contact

</td><td>

Customer contact associated with the billing account.

</td></tr><tr><td>

Consumer

</td><td>

Consumer associated with the billing account.

</td></tr><tr><td>

Order

</td><td>

Priority of this related party among the related parties on the billing account. A lower number indicates a higher priority. This field is populated with the default order for the selected type. Set it when multiple related parties hold the same responsibility and the resolution order matters.

</td></tr><tr><td>

Responsibility

</td><td>

Responsibility that grants the related party access to the billing account through the CAM responsibility framework.For authorized parties, the base system provides responsibilities such as billing authorized account, billing authorized contact, and billing authorized consumer. These responsibilities grant read access to the billing account and its addresses.

The **Responsibility** field is left empty for any listed party type, such as listed account, listed consumer, and more.

**Note:** The responsibilities provided with the base system grant read access only. To grant write or create access, create additional responsibility access configuration records. For more information, see [Creating a responsibility access configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/creating-responsibility-access-configuration.md).

</td></tr></tbody>
</table>5.  Select **Submit** to create billing account related party record.


**Related topics**  


[Granular roles and supported entities for responsibility framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/granular-roles-and-supported-entities-CAM.md)

[Create a responsibility definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/t_CreateAResponsibilityDefinition.md)

[Creating a responsibility access configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/creating-responsibility-access-configuration.md)

[Configure access through the responsibility access configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/declarative-resposibility-framework.md)

[Grant write access to a billing account related party](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/grant-write-access-to-ba-related-party.md)

