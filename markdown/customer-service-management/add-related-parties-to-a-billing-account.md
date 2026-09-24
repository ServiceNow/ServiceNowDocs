---
title: Add related parties to a billing account
description: Extend billing account access to additional customers or stakeholders by configuring billing account related parties. Related parties enable you to define relationships between billing accounts and other entities such as contacts, consumers, or accounts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/add-related-parties-to-a-billing-account.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
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

Billing account related parties use the customer access management \(CAM\) responsibility framework to extend record-level access to a billing account. A related party is one of two kinds:

-   **Authorized party** - an account, contact, or consumer that is granted access to the billing account through a responsibility. The base system delivers this access with responsibility access configurations \(RACs\) and CAM granular roles.
-   **Listed party** - an account, contact, or consumer that is recorded on the billing account for reference only, without access.

For how the responsibility framework, granular roles, and query rules work together, see [Granular roles and supported entities for customer access management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/granular-roles-and-supported-entities-CAM.md).

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** &gt; **Billing Accounts**.

2.  Select a billing account from the list.

    For more information on how to create billing account record, see [Install billing account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/install-billing-account.md).

3.  Select **New** from the Billing Account Related Party related list.

4.  On the form, fill in the fields.

<table id="table_fyv_dtr_bs"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Relationship type of the related party.Authorized types \(such as authorized account, authorized contact, and authorized consumer\) grant the party access to the billing account through a responsibility. Listed types record the party for reference only, without access.

</td></tr><tr><td>

Billing account

</td><td>

Billing Account to which this related party belongs.

</td></tr><tr><td>

Account

</td><td>

Customer account associated with the billing account

</td></tr><tr><td>

Contact

</td><td>

Customer contact associated with the billing account

</td></tr><tr><td>

Consumer

</td><td>

Consumer associated with the billing account

</td></tr><tr><td>

Order

</td><td>

Sequence or priority of the party.

</td></tr><tr><td>

Responsibility

</td><td>

Responsibility that grants the related party access to the billing account through the CAM responsibility framework.For authorized parties, the base system provides responsibilities such as billing authorized account, billing authorized contact, and billing authorized consumer. These responsibilities grant read access to the billing account and its addresses.

The **Responsibility** field is left empty for any listed party type, such as listed account, listed consumer, and more.

</td></tr></tbody>
</table>5.  Select **Submit** to create billing account related party record.


**Related topics**  


[Granular roles and entities for responsibility framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/granular-roles-and-supported-entities-CAM.md)

[Create a responsibility definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/t_CreateAResponsibilityDefinition.md)

[Creating a responsibility access configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/creating-responsibility-access-configuration.md)

[Configure access through the responsibility access configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/declarative-resposibility-framework.md)

